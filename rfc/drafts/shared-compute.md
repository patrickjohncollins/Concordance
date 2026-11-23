# Shared compute

```
RFC:        (assigned on agreement)
Slug:       shared-compute
Title:      Shared compute
Status:     Draft
Intended:   Experimental
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

AI, translation, builds and storage will need far more than one small hearth per home. Compute is treated as a commons, governed like any other scarce resource.

**Sources, nearest first**

1. **Pooled hearths:** many small tasks spread across idle hearths (translation, matching, search, small models).
2. **Community compute hearths:** larger machines with graphics processors, hosted where communities gather (libraries, makerspaces, co-ops, schools) and shared by a federation.
3. **Members' idle computers:** contributed with consent when unused, following volunteer-computing precedents such as Folding@home and Petals.
4. **Partners at the boundary:** universities, public research computing and nonprofits, for heavy jobs such as training a base model.
5. **Using less:** small specialized models, retrieval instead of bigger models, and work scheduled only when useful.

**Allocation:** need first (crisis translation and safety messages), then turns. A host's own use always comes first, and hosts set how much they share, when and for which circles. Heavy work runs when renewable power is available.

**Rules**

- Private content is processed only on the member's own or their circle's hearths. Volunteer machines and partners handle only public, commons or encrypted work.
- Every task runs in a sandbox (WebAssembly or containers) with no access to the host's files.
- Results from untrusted machines are verified, for example by running the same work on two machines, before anyone relies on them.

**Phasing:** v0 needs no shared compute; v1 adds pooled hearths and a few community compute hearths; v2 adds a compute-sharing protocol across federations and volunteer machines.
