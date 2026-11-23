# Self-hosting, native Git and governance

```
RFC:        (assigned on agreement)
Slug:       native-git-and-governance
Title:      Self-hosting, native Git and governance
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

Concordance hosts its own complete definition, and the project is governed by its own charter. The first real circle on Concordance is the stewards' circle that builds it.

**The complete definition** is everything needed to understand, rebuild and verify Concordance with nothing else: the charter and its history, the design principles, the protocol and behavior specs, conformance vectors, all source code, a reproducible build recipe, decision records, accords and translations.

**Native Git hosting, borrowing Radicle's ideas.** Concordance already has signed records, content-addressed blobs, a peer network and hearths, so Git is a thin layer on top. Radicle's MIT/Apache licence lets us borrow its ideas and code where useful.

- **Git objects:** an ordinary local repository on each device, using gitoxide; commits and files sync between peers as Git packs over Iroh.
- **Branches as signed records:** `repo.ref.updated` says which commit a branch points to, signed by whoever moved it, and every peer checks it against the circle's rules.
- **Who can move main:** a rule in the stewards' circle's rule book, e.g. "main moves only for an agreed proposal, signed by two stewards." The canonical version is defined by named stewards' signatures, not by whoever runs a server (Radicle's best idea).
- **Changes and reviews:** a code change is a proposal pointing at commits; reviews are proposal comments.
- **Plain Git for developers:** a `git-remote-concordance` helper so `git push` and `git pull` work as usual.
- **Hearths as seeds:** hearths hold repositories alongside their circles' records.

**One governance for everything.** A code change, a spec change and a charter change follow the same path: proposal, listening, agreement, signed record. A release is a signed record from several stewards, and hearths install only releases signed under the stewards' circle's rules. Anyone can fork, so no group of stewards can capture the project.

**Stewards are trusted servants; they do not govern.** The phrase comes from Alcoholics Anonymous's Twelve Traditions, which have held a worldwide voluntary network together for decades without anyone in charge. Anyone may contribute without permission. Stewards grow into the role through contribution, are agreed by the stewards' circle, look after one scoped area, rotate, and follow the same gentle steps as everyone else. Release signing is the one firm rule: every release needs more than one signer, ideally in different homes and countries, with keys on dedicated hardware. The founder starts as the first steward and shares signing as soon as a second trustworthy signer exists.

**Bootstrapping**

1. Start the repository in ordinary Git, with a read-only mirror on a nonprofit host such as Codeberg so newcomers can find it.
2. Run the stewards' circle by the charter from day one, recording decisions in the repository.
3. Once native Git hosting works, move the repository, decisions and releases onto Concordance.
4. From then on, every hearth can rebuild and verify the software it runs.

**Where the care goes:** peer authentication and ref validation get an outside security review before anyone relies on them (Radicle's 2026 vulnerabilities were in exactly this area); rejected pushes, conflicting ref updates and revoked stewards get explicit rules and conformance tests.
