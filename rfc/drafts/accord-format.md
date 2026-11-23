# Accords: format, building blocks and evolution

```
RFC:        (assigned on agreement)
Slug:       accord-format
Title:      Accords: format, building blocks and evolution
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

## Accords

The Charter is the root accord; every other accord grows from it or from another accord. A circle adopts the Charter first, adds the accords that fit its purpose, and makes each one its own. New kinds of circle come from writing a new accord, not new software: the test that Concordance is a general commoning system.

**Three kinds of accord**

- **Purpose accords** say what a circle does (Care, Garden, Land Trust).
- **Practice accords** change how any circle works once adopted, and apply to everyone in it (Anonymity, Open Dispute Hour, Pattern Sharing).
- **Linking accords** work between circles (Federation, Crisis Response).

**The accord tree**

- **The Charter** (root accord)
  - **Everyday accords:** Mutual Aid, Gifting, Work Day
  - **Purpose accords**
    - **Care** (its safeguarding is inherited by all beneath it): New Parents, Childcare, Youth, Elders, Caregivers, Disability and Access, Farewell and Grief
    - **Health and healing:** Recovery and Peer Support (requires Anonymity), Listening, Living with Illness, Community First Aid
    - **Food and water:** Garden (with Seed Library), Community Kitchen, Water
    - **Land and shelter:** Land Trust (with Build and Housing, Nature Stewardship)
    - **Things, spaces and movement:** Tool Library (with Repair), Shared Space, Lifts and Transport
    - **Learning and culture:** Knowledge Commons (holds the accord library), Study Circle, Apprenticeship, Creative
    - **Livelihood:** Skill Share, Worker Cooperative, Open Source Project
    - **Infrastructure:** Energy, Connectivity, Compute
    - **Peace and justice:** Welcome, Rights (requires High Risk), Peacemaking
    - **Meaning:** Faith or Practice
    - **Resilience:** Preparedness
  - **Practice accords:** Open Dispute Hour, Anonymity (with High Risk), Bridge, Common Purse, Mentoring, Pattern Sharing (not available with Anonymity or High Risk)
  - **Linking accords:** Federation (with Crisis Response, which requires Preparedness; Seeding; Exchange)

Safety flows down the tree: every Care accord inherits safeguarding, and every Rights circle inherits High Risk. "Requires" links keep combinations sound. A new circle needs only the Charter, Mutual Aid, Gifting and Work Day; the rest grows when needed. Every accord passes the five tests, so there is no marketplace or ranking accord.

**Words and provisions** Each accord carries the same agreement in two forms, as Creative Commons licences do: the words members read and sign, and structured provisions the app reads. Provisions combine only a fixed vocabulary of building blocks (resources with uses, records, roles, declarative rules, privacy levels, prompts and standard views), so an accord can never run arbitrary code. When a circle adopts an accord, the app assembles its screens and rules from the provisions. Example, the Work Day accord:

```
grows-from: charter v2 or later
kind: everyday
resource: task slots (shared), tools and materials (offered)
records: workday.proposed, workday.joined, item.offered,
         workday.held, thanks.given
roles: host, task lead, meal lead, safety
rules: a household agrees before work on its home;
       safety briefing before tool use
prompts: reminder the day before; suggest the next one afterward
views: work day page, task board, meal list
privacy: circle (open to invited guests)
```

Words and provisions must match: when either changes, the app shows the provision change in plain language beside the wording, and members agree to both. An AI assistant may draft provisions from the words; people check and agree them. Provisions merge down the tree, and those from the Charter (safety, free exit, export) can't be switched off.

**Storage** An accord is a small bundle: `accord.toml` (name, version, grows-from range, requires, licence, change note, provisions) and `words/<language>.md` for each translation, all sharing one language-neutral set of provisions. Its BLAKE3 hash, over a canonical form, is the version's identity. The shared accord library is a Git repository in the Knowledge Commons, hosted on Concordance: each accord a folder, each agreed version a commit, adapted versions from different circles and cultures as branches. Phones keep the accords their circles use; hearths keep every version ever adopted. No version is deleted while anything points to it, and none is edited in place.

**Adoption and signing**

- **The Charter:** adopted at founding; every member signs it on joining.
- **Purpose accords:** the circle adopts by agreement; members who take part sign; others aren't bound and can't take part until they do.
- **Practice accords:** apply to the whole circle once agreed; members acknowledge them, and anyone can object before agreement.
- **Linking accords:** the circle signs as a whole, by agreement.
- **Roles** (safety lead, steward) are individual commitments the circle agrees to, where required checks are recorded.
- Records: `accord.adopted`, `accord.signed`, `accord.version.agreed`.

**Creating a new accord**

1. Notice a need, and look in the library first; adapt an existing accord if one fits.
2. Start from the nearest accord, which the new one grows from.
3. Write the words together, as an Automerge draft.
4. Draft provisions from the words, with AI help, checked by members.
5. Automatic checks: only known building blocks, nothing overriding the root, requirements met, the five tests passed.
6. Try it, if it's safe to try; adjust.
7. Agree, sign and adopt; then, if the circle wishes, share it to the library under an open licence. Library stewards review lightly, and carefully for anything touching care, children, safety or high-risk use.

Anyone can write an accord and use it in their own circle without permission. When an accord needs something the building blocks can't do, it becomes a behavior spec for the stewards' circle, and the new building block is released for everyone.

## How the charter and accords evolve

A charter that needed every circle's agreement to change would never change. So three things change in three different ways.

1. **A circle's own charter and accords** change whenever its members agree, by proposal, listening and agreement. Each version is fixed once agreed, which makes change visible rather than preventing it.
2. **The shared root accord in the library changes by adoption, not by vote.** Library stewards publish new versions, informed by what circles have adapted and learned; each circle chooses whether and when to adopt one. Old and new versions coexist, as Creative Commons licence versions do. Good changes spread because circles see them work.
3. **What circles share in order to federate is a small core,** the seven principles in any wording, not identical text. Circles on different charter versions federate freely; the principles themselves evolve slowly, by agreement among federated circles.

**Keeping the rest from locking it in**

- Accords declare a range ("grows from charter v2 or later"), not one exact version; a new root version flags only real conflicts.
- Signatures don't expire: members sign a newly adopted version when they next open the app; their signature on the old version stays valid for the time it applied, and not having signed yet is never grounds for removal.
- Each circle revisits its charter regularly; library stewards gather what circles have learned once a year.
- Forks are welcome: many versions side by side is healthy, not a failure.
