# Spec-driven development

```
RFC:        (assigned on agreement)
Slug:       spec-driven-development
Title:      Spec-driven development
Status:     Draft
Intended:   Informational
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

The specification is the source of truth; code is one implementation of it. Any team, or any AI agent, should be able to build a compatible Concordance from the specs alone, and prove it by passing the conformance suite.

**Four layers of spec, each tracing to the one above**

1. **The charter:** what we promise each other.
2. **Design principles:** each promise as an engineering constraint (the table at the top of this doc).
3. **The protocol spec:** precise promises about how the software behaves, so that every app built for Concordance can talk to every other and keeps the charter's promises to members. It binds code, never people. It covers record formats, signatures, delegation, sync messages, validation steps, rule-book schema. Versioned; changes follow the same proposal process as the charter, among maintainers.
4. **Behavior specs:** scenarios in Given/When/Then form for every user-visible behavior, e.g. *Given a member has lost their phone, when three of five guardians approve, then the member's key is restored and their history is intact.*

**Checks that run on every change**

- **Conformance suite:** test vectors for every record type, signature and validation rule; any implementation must pass all of them.
- **Determinism tests:** replay the same records in random orders and from random partial states; every run must reach the same circle state.
- **Network simulation:** many simulated peers with partitions, offline phones and lost hearths; sync must converge without loss.
- **Fuzzing** of every parser and validator.
- **Traceability:** every test cites the spec clause it checks, and every spec clause cites the charter promise it serves. An untraced clause is questioned; an untested clause blocks release.

**How work flows**

1. A need is written as a behavior spec, in plain language, and reviewed by people from a circle, not only developers.
2. Protocol changes are proposed, discussed and agreed before any code.
3. Code is written by people or AI agents against the agreed specs, with a human reviewing every change.
4. The checks above gate every merge; architecture decisions are recorded as short decision records.

**Repository layout:** `charter/`, `spec/protocol/`, `spec/behavior/`, `spec/vectors/`, `decisions/`, `core/` (Rust), `app/` (Tauri), `hearth/` (image), `sim/` (network simulator).
