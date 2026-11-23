# Selewa and the Seed: Notes from 22 November 2026

These notes gather the ideas from today's conversation that are not yet in the Charter, the Design or the Story. They are working notes for review, not decisions.

## 1. A language of our own

Bahá'u'lláh (1817–1892), founder of the Bahá'í Faith, called for one auxiliary language and script to be taught in every school beside each people's mother tongue. "Auxiliary" is the key: the shared language sits beside every mother tongue and replaces none. That is the same rule Concordance follows: standard underneath, local on top.

Concordance can create an entirely new language: **Selewa**, "hearts together."

## Purity as fairness

In Concordance, a language is pure because it is fair, not because of where its words come from. The seven principles become seven tests:

1. **Open to all:** easy to learn from any mother tongue.
2. **Equals together:** no native speakers at the start, no built-in forms of rank.
3. **Need first:** the first words are the words for helping each other.
4. **Local rules:** a small fixed core, local words and accents on top.
5. **Freely given:** public domain from the first day.
6. **Our own:** anyone may coin a word; circles adopt it.
7. **Held in trust:** the core changes only by adoption.

Quality is judged by the learners who find it hardest.

## A first sketch

- **Sound:** five vowels (a e i o u) and about ten consonants common to nearly every language (p t k m n s l w y h); open syllables; fixed stress; easy to sing.
- **Grammar:** roots never change; meaning built by joining pieces; no gender, no irregular verbs, no ranked forms of address.
- **Script:** a new hand-drawn script whose shapes show how sounds are made, as in Hangul.

First roots:

| Root | Meaning |
|---|---|
| su | fire, hearth |
| mi | person |
| lo | give |
| na | need |
| wa | together |
| sele | heart |

Combined: **sumi**, "those who share this fire"; **Selewa**, "hearts together"; **Mi lo, mi na**, "I give, I need."

## The first works

The first works in Selewa are the founding texts:

- **The Charter** first. Its few hundred distinct words become the seed vocabulary, and the index of every word in it, a concordance, becomes the first dictionary.
- **The accords** next, adding the words of daily life. Language tag: `art-x-selewa`.
- **The manifesto**, "Hearts Together."
- **The book**, in a bilingual edition: Selewa on one page, the reader's language on the facing page. Each chapter title is a root.

## The grammar is an accord

The Selewa accord is a practice accord that grows from the Charter and the Standards accord:

- **Words:** the grammar described in plain language, in every translation.
- **Provisions:** sound rules, composition rules, and records (`word.coined`, `word.adopted`).
- **The grammar** is a frozen core, changed rarely by adoption of a new version.
- **The vocabulary** is a living layer, growing every day by coined and adopted words.
- In time the accord includes the grammar written in Selewa itself.

## 2. Bootstrapping, as a compiler does

A new programming language's first compiler is written in an existing language; once the language compiles, its compiler is rewritten in itself.

1. **Stage 0:** the grammar written in English and other languages.
2. **Stage 1:** the Charter written in Selewa using that grammar.
3. **Stage 2:** the grammar and dictionary rewritten in Selewa.
4. **Stage 3, the fixed point:** someone who learned only from the Selewa grammar rewrites the Charter, and it matches.

Ken Thompson showed that self-hosted compilers can carry hidden inherited flaws. The fix is David A. Wheeler's *diverse double-compiling*: write the stage 0 grammar from several host languages (for example Mandarin, Arabic, Swahili, Spanish, Hindi, English) and resolve every disagreement. What remains belongs to none of them.

The same arc runs through all of Concordance:

| Part | Built in a host first | Then hosts itself |
|---|---|---|
| Code | Repository on GitHub | Native Git inside Concordance |
| Rules | Design doc and RFCs in English | RFCs agreed by circles in the app |
| Language | Selewa grammar in English | Grammar and dictionary in Selewa |
| Story | Book written in English | Book written in Selewa, translated outward |

## 3. The seed

Concordance is a seed: a complete description of itself plus the means to rebuild itself.

- **Why:** the story and the book.
- **What:** the Charter.
- **How:** the accords.
- **Tool:** the code.
- **Medium:** Selewa.

Ramifications:

- **It can outlive its hosts.** Any circle with a copy can regrow the whole.
- **It can travel through time.** It explains itself, so it stays understandable.
- **It can be copied freely, and branch.** The seven-principle core keeps the branches able to recognize each other.
- **It can become a people without territory**, open to anyone.
- **Its foundations are hard to change**, so the seed must be small, plain and checked across cultures.
- **It shapes thought.** What is easy to say becomes easy to do.

The tension to design for is whole, but open. The most important thing to build is the smallest complete seed.

**Seed, meme, tree, frequency.** The seed is how it lasts. The meme is how it travels: fidelity, fecundity and longevity, a mutualist memeplex that spreads by making its hosts' lives better. The tree is how it grows: seed, sapling, tree, and a forest joined at the roots. The frequency is how it finds its people. In music, a concord is notes that sound well together; a string tuned to a note sings when that note is played nearby. Concordance does not push. It sounds, and those already tuned to it answer.

**At the heart: turning toward another.** One person notices another and responds. *I see you. You are not alone.* It has two halves, giving and needing (*Mi lo, mi na*), and everyone is both, which is why it is a circle and not a ladder. In one word: *sele*, heart.

## 4. Many scripts, many voices, one meaning

Selewa can be written in any script and pronounced differently around the world, because its core is a meaning layer.

1. **Core:** roots and grammar, identified by meaning.
2. **Scripts:** Latin, Arabic, Devanagari, Hangul, Ge'ez, a new native script and Braille, as reversible mapping tables.
3. **Voices:** regional pronunciations that keep the same distinctions.
4. **Signs:** a signed form built on the same core.

These become accords: Selewa Core, script accords and voice accords. Unity lives in meaning; diversity lives in the surface. Chinese characters, mathematics and Unicode are precedents. The shared core prevents the drift that split Latin into separate languages.

## 5. The meaning layer in detail

1. **Foundation:** about 65 semantic primes found in every studied language (Wierzbicka and Goddard): I, you, someone, good, bad, do, want, know, feel, say, live, die, not, can, because, if, like…
2. **Roots defined in primes.** *lo (give):* someone does something; because of this, something that was with this someone is now with someone else; this someone wants this. The dictionary is self-hosting from the start.
3. **Identity:** each root is a signed `word.coined` record, and its ID is the record's hash. A new sense means a new root; nothing drifts silently.
4. **Structure:** sentences are stored as trees with explicit roles, so each voice can choose its own word order.
5. **Grammar:** almost nothing is required; time, number, certainty and politeness are available when wanted. There are two words for "we": inclusive and exclusive.
6. **Two modes:** precise, for commitments and accords; open, for song, story and prayer.
7. **Growth:** compose first, coin last. Commons words from every tradition (ubuntu, minga, dugnad, langar) enter as roots, with their origin credited.

## 6. Words and provisions converge

A text in precise Selewa is readable by people and checkable by a machine, so one text could be both an accord's words and its provisions.

**Precedents:** Ricardian contracts (Ian Grigg), Catala (law as code), controlled natural languages. Cautionary tale: The DAO (2016), where "code is law" meant the code beat the people.

**Promises, not commands:**

- **We promise:** a commitment. The tool reminds, records and celebrates, and never blocks.
- **We can:** a freedom. The tool makes it easy.
- **We ask:** a request. Anyone may say no.
- **We hope:** an aspiration. The tool keeps it visible.
- **Protections:** the only things enforced, and only to protect people, such as privacy by encryption.

**Example, Work Day:** *We (all of us) promise: each season, we gather for one work day. Whoever can, comes. Whoever cannot, is not blamed.* This compiles to a recurring event, an optional RSVP, thanks recorded for those who came, and a protection: no record of absence.

**What becomes possible:**

- No gap between words and app.
- Anyone can write a working accord.
- Translations can be checked against each other.
- Conflicts surface before adoption.
- Changes show as changes in meaning.
- Every prompt can explain why.
- The simulator reads accords directly.

**Limits:**

- **Open texture:** phrases like "when we can" compile to *the circle decides*.
- **People over code:** if the machine's reading and the circle's understanding differ, the circle is right and the text is fixed.
- **Start small:** map only the existing provision vocabulary at first.

**Bootstrap:** stage 0, words and `accord.toml` written separately; stage 1, Selewa compiles to TOML; stage 2, the Selewa text is the accord.

## 7. Changes to the design (proposed, not yet applied)

- **Principles:** add "Words are provisions" and "The circle decides what it means"; the promise vocabulary replaces every *must*.
- **Core:** a Selewa engine that parses, renders and compiles.
- **Signing:** sign the hash of the canonical meaning tree; what you see is what you sign, checked by multiple independent renderers.
- **Data:** new records `word.coined`, `word.adopted` and `root.defined`; accord bundles hold `accord.sel` plus generated language files.
- **Rules:** promises prompt, protections enforce, "the circle decides" creates a human decision; validation blocks only to keep a protection.
- **Accord writing:** write sentences, check a paraphrase, compile, simulate, adopt; amendments shown as meaning changes; conflicts flagged.
- **AI:** helps draft and suggests parses but is never in the trust path; a person confirms every parse.
- **Security:** guard against ambiguity attacks and rendering attacks.
- **Specs:** a new kind of test vector, sentence in and provisions out.
- **v0:** still ships `accord.toml`, but locks in canonical hash-identified encoding and groups provisions as promise, can, ask, hope and protect.
- **Milestones:** M5, the Selewa seed and compiler proven on Work Day; M6, accords written in Selewa.
- **Possible Charter line:** *"Our agreements mean what we understand them to mean, and when the words fall short, we fix the words."*
- **Open questions:** which formal semantics; who confirms parses for a circle; how open-texture decisions are recorded; whether every script mapping can be fully reversible; how to encode the signed form.

## 8. Other pending items

- A charter line on forgiveness, and the Repair and Release practices.
- The essay "Concordance: Hearts Together."
- The Charter's open items: shared things when a circle splits, and how the safety person is chosen.
- The simulator spec.
- A Bahá'í entry in the cooperative traditions, covering consultation and elections without candidates.
- Publishing the repository to a personal GitHub account.
