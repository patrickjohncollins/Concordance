# Sync and storage

```
RFC:        (assigned on agreement)
Slug:       sync-and-storage
Title:      Sync and storage
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

Every device works fully offline and catches up when it meets another peer. Hearths make sure there is almost always a peer awake.

- **Connections: Iroh 1.0.** Peers dial each other by device key over QUIC, with hole-punching through home routers and relay fallback. Circles may run their own relay; the default is a list of community relays, never a single operator.
- **Announcements: iroh-gossip.** Each circle has a gossip topic derived from its id. New records are announced there; members subscribe on joining.
- **Log sync:** on connection, two peers exchange the latest sequence number per author and fetch what's missing. Logs are small and sync fully to every member device.
- **Documents and files: iroh-blobs.** Charter versions, attachments and exports are content-addressed blobs, fetched on demand and verified by hash.
- **Drafts: Automerge.** A proposal's draft is an Automerge document so members can edit offline and merge automatically. When agreed, the draft is frozen into a charter version blob.
- **Hearth storage:** hearths hold a full copy of every log and blob for their circles. Private material (care records, guardian shares) is encrypted before it reaches a hearth, so a host can't read what lives in their home.
- **Replication target:** v0 aims for every record on at least three hearths in different homes. Erasure coding across hearths (any k of n rebuilds the data) is deferred to v1, once circles hold more than text.
- **Phones:** keep their own circle's logs in full, plus blobs they've opened; everything else is fetched from hearths when needed.
