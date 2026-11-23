# Security and privacy

```
RFC:        (assigned on agreement)
Slug:       security-and-privacy
Title:      Security and privacy
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

The people most likely to need a circle (survivors, the isolated, people under pressure from those around them) are also the most at risk if it leaks. Privacy is the default; openness is a choice.

| Threat | Protection |
| --- | --- |
| Lost or stolen phone or hearth | Device revocation; encrypted storage; member key in secure hardware |
| Lost member key | Recovery phrase or 3-of-5 guardian recovery; signed succession to a new key |
| Impersonation or fake members | Joining needs a welcome from an existing member; vouches are scoped and withdrawable |
| A member rewriting their past | Hash-chained logs: a changed or forked history is detectable by every peer |
| Eavesdropping on the network | All traffic encrypted by QUIC; private records encrypted end to end to named recipients |
| A curious hearth host | Private material reaches hearths only in encrypted form |
| Hiding a circle's existence | Private circles use unguessable topic ids and never appear in any directory |
| Malicious software update | Releases signed by multiple maintainers; hearths verify before installing |
| Someone harming a child or vulnerable adult | The charter's safety rule: concerns go to the chosen safety person; care roles need the checks the law requires |

**Metadata matters too.** Relays see which devices connect, not what they say. Circles that need more protection can run their own relay, or connect only peer to peer.

**Anonymity, as an explicit promise.** Recovery groups and other peer-support circles need stronger anonymity than most, and Concordance promises it:

- **Pseudonyms are first-class.** A member key needs no real name; a member can use a different name in each circle, and nothing links them unless the member chooses.
- **Private circles are invisible** to anyone outside them: no directory entry, no discoverable topic, no federation listing unless the circle opts in.
- **No record reveals who attends what,** even to a hearth host: membership and attendance in private circles are encrypted to members only.
- **No contact discovery.** The app never uploads address books or suggests people from outside the circle.

**Legal duties.** Encryption and data laws vary by country, and some governments are debating message scanning. The design keeps content end-to-end encrypted and gives circles no central point a court can compel.
