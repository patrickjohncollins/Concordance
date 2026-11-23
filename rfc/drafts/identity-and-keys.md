# Identity and keys

```
RFC:        (assigned on agreement)
Slug:       identity-and-keys
Title:      Identity and keys
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

A member is a key, not an account. Devices act for the member through delegated keys, so losing a phone never means losing membership.

- **Member key (Ed25519):** created on the member's first device. It signs only rare, high-trust acts: authorizing or revoking devices, joining or leaving a circle, signing a charter version. Kept in the device's secure hardware where available.
- **Device keys:** each phone, laptop and hearth has its own key, which is also its Iroh endpoint address. The member key signs a delegation certificate for it, with the device's role (phone, hearth) and optional expiry.
- **Revocation:** a signed revocation record, gossiped to the circle. Peers reject anything the device signs after the revocation time.
- **Recovery, two routes:**
  1. A 24-word recovery phrase, written on paper at setup.
  2. Social recovery: the member key is split with Shamir secret sharing among trusted members chosen by the member (default 3 of 5). Shares are encrypted to each guardian's key; no guardian can use their share alone.
- **Key rotation:** a recovered or compromised member key is replaced by a new one, linked to the old by a signed succession record so the member's history stays theirs.
- **Paper members:** a member without a device gets a member key held by a chosen steward, who signs on their behalf only with recorded consent. The member can take the key over later.
