# Rules and validation

```
RFC:        (assigned on agreement)
Slug:       rules-and-validation
Title:      Rules and validation
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

There is no server to enforce rules, so every peer checks every record it receives, the same way, and drops what fails.

**Two layers of checks**

1. **System checks, fixed in the protocol:** valid signature; device authorized by the author at the time of signing and not revoked; sequence and previous-hash consistent; record type known; body matches its schema.
2. **Circle rules, set by the circle as data:** for example "a newcomer becomes a member when one member welcomes them," or "a proposal is agreed when no member present records a concern." Each rule is a small declarative entry in the circle's rule book, versioned and signed like the charter.

**Determinism.** A rule's result may depend only on the records it reads, never on the clock, the network or the device. Two honest peers with the same records always reach the same state.

**Spirit over thresholds.** The charter avoids hard numbers, so most v0 rules record and surface rather than block: the app shows that a request has gone unanswered or that a member has gone quiet, and leaves the response to people. Hard blocks exist only where safety or integrity needs them: unsigned records, revoked devices, care records opened by someone not named.

**Forks are allowed.** If members can't accept a change, they can start a new circle from any charter version. A fork is a new circle id with a `circle.founded` record that cites its parent; members' histories travel with them.

**Later:** a sandboxed rule engine (WebAssembly) so circles can share richer rules within their accords without anyone running untrusted code.
