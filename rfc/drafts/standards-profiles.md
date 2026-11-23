# Standards profiles

```
RFC:        (assigned on agreement)
Slug:       standards-profiles
Title:      Standards profiles
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

Concordance builds on existing standards, adopted by reference. This RFC states which standards Concordance uses and how.

## Principle: standard underneath, local on top

Records always use the protocol standards below. Each member sees values in their own conventions: units, calendars, languages and formats.

## Built into the protocol

| Area | Standard | Profile |
| --- | --- | --- |
| Text | Unicode, UTF-8 | All text in UTF-8 |
| Dates and times | ISO 8601 | Always UTC, to the second |
| Units | SI | All quantities in provisions and records in SI units |
| Languages | BCP 47 | Every translation tagged |
| Licences | SPDX identifiers | Used in accord and RFC headers |
| Signatures | Ed25519 | Member and device keys |
| Hashes | BLAKE3 | Identity of records, accords and RFC versions |
| Transport | QUIC (RFC 9000), via Iroh | All peer connections |

## Shown each member's way

- Units: stored in SI, shown in the member's preferred units.
- Calendars: stored as standard dates, shown in Gregorian, Hijri, Hebrew, Chinese, Hindu and other calendars members use.
- Language, number and date formats: the member's own conventions.

## Adopted by accords, by place

Accords that need external standards reference them by place, through the Standards accord: food hygiene (Community Kitchen), electrical codes (Energy), building codes (Build and Housing), safeguarding and background checks (Care, Youth), accessibility (WCAG, for the app itself).

## Shared between circles

- Crisis Response: the Common Alerting Protocol.
- Exchange: shared item categories.

## Path

Consume, profile, contribute to standards bodies, steward orphaned standards, host standards communities that choose to work on Concordance, and federate as a body of standards bodies. Standards set by law or treaty remain adopted by reference.
