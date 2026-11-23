# Overview and design principles

```
RFC:        (assigned on agreement)
Slug:       overview
Title:      Overview and design principles
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

The Concordance app is a local-first, peer-to-peer tool that carries the Concordance Charter: each member holds their own keys, every record is signed, and circles store and sync their data on members' phones and home hearths, with no central server. It is built spec first: every behavior is defined in a checkable specification before any code is written.

## Design principles

Every architectural choice traces back to a promise in the charter. If a design can't keep the promise, the design changes, not the charter.

| Charter promise | Engineering constraint |
| --- | --- |
| Open to all: anyone may join, and leave with their history | Keys live only on the member's devices; full export in an open format at any time; no barrier beyond a welcome from a member |
| Local rules: those affected decide | Rules are data the circle edits, not code; every peer enforces the current version |
| Freely given | No prices, balances owed or counts of giving in the data model |
| Need first | Allocation rules put need first; tests check worst-off outcomes, not only averages |
| Our own: our information and our network; what's private stays private | No central server or account; any peer can be replaced; private records encrypted end to end; open source |
| Equals together | Circles are independent units; federation is a signed agreement between circles, never a shared database |
| Held in trust | Land-trust accords make "never sold" a rule no vote can change |
| Bigger things need agreement everyone can live with | Every charter and accord version is content-addressed and signed; history is append-only |
| Anyone can take part without our tools | Works offline; a paper path for members without devices; plain language, large type, voice |
| Thank generously; everyone's gifts count | No scores, rankings or leaderboards anywhere in the data model or the interface |

## Architecture at a glance

```
  Your phone  <-- Iroh, direct by key -->  Your hearth  <-->  Other members
  (app, works offline)                   (always on,         (their phones
       :                                  full copy,          and hearths)
       :  fallback only                   encrypted)
  Community relays

  Inside every device, the same Rust core:
    Interface  Tauri app on phones and laptops; headless on hearths
    Rules      every peer checks every record the same way
    Records    signed, hash-chained logs; charter and accord versions by hash
    Sync       Iroh connections, gossip, blobs, Automerge drafts
    Identity   member key, delegated device keys, recovery
```

Phones, laptops and hearths are all equal peers running the same core; hearths add availability, and relays only help two peers find a path when home routers block a direct connection.
