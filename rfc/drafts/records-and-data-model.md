# Records and data model

```
RFC:        (assigned on agreement)
Slug:       records-and-data-model
Title:      Records and data model
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

Each member keeps one signed, append-only log per circle. The circle's state (who belongs, which charter is current, what's been offered) is not stored anywhere as a master copy: every peer derives it by replaying the members' logs under the circle's rules.

**Every record carries:** author member key, signing device key, circle id, sequence number, hash of the author's previous record, timestamp, record type, body, signature. The hash chain makes a member's history tamper-evident: a gap or a fork in one author's log is itself evidence.

**v0 record types**

| Record | Signed by | Body | Visible to |
| --- | --- | --- | --- |
| `circle.founded` | Founding members | Circle name, first charter hash, visibility level | Circle |
| `device.authorized` / `device.revoked` | Member key | Device key, role, expiry | Circle |
| `member.introduced` | Newcomer | Introduction text, one offer | Circle |
| `member.welcomed` | An existing member | Newcomer's key | Circle |
| `accord.signed` | Member key | Version hash of the Charter or an accord | Circle |
| `member.left` | Member key | Optional note | Circle |
| `proposal.opened` | Any member | Draft document id, reason | Circle |
| `proposal.comment` | Any member | Text, optional concern flag | Circle |
| `proposal.agreed` | Facilitator, co-signed by members present | Proposal id, resulting accord version hash | Circle |
| `need.posted` / `offer.posted` | Any member | Text, optional expiry | Circle or named members |
| `thanks.given` | Any member | Recipient, text, visibility chosen by recipient | Recipient decides |
| `vouch.given` / `vouch.withdrawn` | Any member | Recipient, scope ("tools", "hosting") | Circle |
| `steward.recorded` | Steward | Paper member's act, consent note | Circle |
| `recovery.guardians` | Member key | Encrypted shares, guardian keys | Guardians only |

**Charter versions** are not records but content-addressed documents (BLAKE3 hash). Records point to them by hash, so "which version did you sign?" has one exact answer. The same holds for every accord (see Accords below).

**Deliberately absent:** counts of gifts, scores, follower lists, read receipts, location history.
