# Plan

Working plan for Concordance, carried over from the design doc of 2026-11-22.

## Planning checklist

These steps come before any code, in this order.

- [x] Choose the licence for code, specs and charter. (Decision 0005: AGPL-3.0-or-later for code, CC-BY-SA-4.0 for documents.)
- [ ] Form the stewards' circle: who starts it, how stewards join and leave, and how many signatures a release needs.
- [ ] Adapt the charter for the stewards' circle, adding how code changes and releases are agreed and signed.
- [x] Set up the repository with the agreed layout (github.com/patrickjohncollins/Concordance, 2026-11-23).
- [ ] Set up a read-only mirror.
- [x] Write decision records for the big choices: Iroh, Tauri, gitoxide and native Git hosting, the licence (decisions 0002 to 0005).
- [ ] Write the first protocol specs: identity, device delegation, records, charter signing.
- [ ] Write behavior specs for joining a circle and signing the charter.
- [ ] Write conformance vectors for those specs.
- [ ] Write the protocol spec for native Git hosting: ref records, validation rules, pack sync.
- [ ] Review the plan with at least one person from a potential pilot group and one outside developer.

## v0 scope and the spike

v0 does exactly what the charter needs and nothing more: identity, joining, signing, proposals, needs and offers, export, and one hearth per circle. v0 ships the Charter and three everyday accords: Mutual Aid, Gifting and Work Day. Each step below has a gate that must pass before the next begins.

1. **Specs first:** protocol spec for identity, delegation, records and validation; behavior specs for the v0 screens; first conformance vectors. *Gate:* a second developer can explain the protocol from the spec alone.
2. **The spike:** two phones and one hearth. Create member and device keys; connect across different networks; publish a charter version, sign it on one device, verify it on another; sync after one device was offline; recover a key from 3 of 5 guardians. *Gate:* all five work, and the determinism tests pass.
3. **Core library:** the Rust core with logs, validation, sync and rules as data. *Gate:* conformance suite and network simulation green.
4. **Native Git hosting:** signed ref records, pack sync over Iroh, the `git-remote-concordance` helper, and hearths seeding repositories. *Gate:* the stewards' circle moves the Concordance repository onto Concordance, and an outside reviewer has checked peer authentication and ref validation.
5. **App v0:** the nine screens, in English first, with large-text and screen-reader support. *Gate:* someone who has never used it joins a circle and signs the charter unaided.
6. **Hearth image:** reference board, zero-configuration pairing, signed updates with rollback. *Gate:* a non-technical member plugs one in and pairs it in under a coffee break.
7. **Pilot:** three different local groups use v0 for three months. *Gate:* each group decides to keep using it.

**Not in v0:** resources and scarcity rules, federation, care-circle records, erasure coding, shared compute, translations beyond English. Each waits until real circles ask for it.

**Locked in now, so Selewa can follow later.** v0 accords use a canonical, hash-identified encoding, so signatures can later move onto meaning trees, and their provisions are already grouped as promise, can, ask, hope and protection.

**After v0: Selewa milestones**

1. **Selewa seed and compiler:** the seed reviewed from many host languages, and the Work Day accord written in precise Selewa and compiled to provisions. *Gate:* the compiled provisions match the hand-written `accord.toml`, and a circle confirms the paraphrase says what they mean.
2. **Accords written in Selewa:** new accords written as Selewa text, with TOML generated. *Gate:* a member with no programming background writes a working accord that a circle adopts.

## Open questions

- [ ] Does Tauri 2 on mobile give reliable background sync, or do phones need native code for that part?
- [ ] Which reference board for the first hearth image, given availability and price in different countries?
- [ ] Who maintains the community relay list, and how are relays added or removed?
- [ ] How do maintainers sign releases, and how does that group change over time?
- [x] Which open licence? Resolved by decision 0005.
- [ ] How do circles find each other for federation without a central directory?
- [ ] How does a steward's role for paper members stay accountable?
- [ ] Which first languages after English, and who translates?
- [ ] Which formal semantics should the Selewa meaning layer use?
- [ ] Who confirms a parse on behalf of a whole circle?
- [ ] How are "the circle decides" decisions recorded?
- [ ] Can every script mapping be made fully reversible?
- [ ] How is the signed form of Selewa encoded?
