# RFC 0: The Concordance RFC process

```
RFC:        0
Slug:       process
Title:      The Concordance RFC process
Status:     Draft
Intended:   Process
Authors:    Patrick Collins
Created:    2026-11-22
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

Concordance's technology is specified in a series of Requests for Comments. The name follows the internet's RFC tradition, begun in 1969 and chosen to sound tentative and invite others in. RFCs bind implementations of Concordance, never people.

## Naming and numbering

Sequence numbers assigned by many peers can collide, so an RFC has three names:

1. **Identity:** the BLAKE3 hash of each version, over a canonical form. Records and signatures point to this.
2. **Working name:** a descriptive slug, such as `accord-format`. When two drafts share a slug, they are shown with the author's short key until one is renamed or they merge.
3. **Number:** assigned only on agreement, by the **RFC editor** of the standards circle (a rotating role, so there is a single writer and no collisions). Each standards circle numbers its own series, for example `protocol-6`. The number is a convenience for people; the hash remains the identity.

Drafts live in `rfc/drafts/<slug>.md`. On agreement, an RFC moves to `rfc/<series>/<number>-<slug>.md`.

## Statuses

| Status | Meaning |
| --- | --- |
| Draft | Open for comment; freely changed |
| Experimental | Agreed for trying out; may change |
| Standard | Agreed, with at least two independent implementations working together and conformance tests published |
| Informational | Guidance and context, not rules |
| Process | How Concordance makes decisions about its technology |
| Historic | Replaced or retired, kept for the record |

## How an RFC is agreed

1. Anyone writes a draft and shares it for comment.
2. Comments are recorded, and the draft records how each was addressed.
3. The standards circle agrees in the Charter's way: listening first, then agreement everyone taking part can live with.
4. For Standard status: running code from two independent implementations, and published conformance tests ("rough consensus and running code").
5. The RFC editor assigns a number; the agreed version is fixed, fingerprinted and signed.

## Changing an agreed RFC

Agreed RFCs are never edited. A change is a new RFC that states which RFC it **updates** or **replaces**, so the history of every decision stays readable.

## Kinds of tests in an RFC

Each normative requirement states its kind of test:

- **Binary:** must always pass (signatures, revocation, determinism, privacy).
- **Graded:** score, threshold and comparison with the last version (translation quality, drafted provisions).
- **Statistical:** distribution, confidence and worst-case bound (simulator claims).
- **Human review:** who judges, and how (wording, respectfulness).

## First drafts

The drafts in `rfc/drafts/` were split from the design document of 2026-11-22; the current design is `design/design-2026-11-23.md`, and `selewa-meaning-layer.md` was added from it. Each carries an intended status.
