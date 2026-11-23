# Selewa and the meaning layer

```
RFC:        (assigned on agreement)
Slug:       selewa-meaning-layer
Title:      Selewa and the meaning layer
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-23
Updates:    accord-format, rules-and-validation, identity-and-keys, language-and-translation
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

Selewa's core is a meaning layer: roots and grammar identified by meaning, not by spelling or sound. Scripts and voices are surfaces over it. This lets one text be read in any script and spoken in any accent, and lets an accord's words and its provisions become the same text.

**Layers**

1. **Core:** roots defined in the semantic primes (about 65 meanings found in every language studied); each root is a signed `word.coined` record identified by its hash, so meanings never drift silently.
2. **Scripts:** Latin, Arabic, Devanagari, Hangul, Ge'ez, a native Selewa script and Braille, each a reversible mapping table.
3. **Voices:** regional pronunciations that keep the same sound distinctions.
4. **Signs:** a signed form on the same core.

Each becomes an accord: Selewa Core, plus script and voice accords that circles adopt as they use them.

**Sentences are trees.** A sentence is stored with explicit roles (who does what, to whom), so each voice may choose its own word order and the meaning stays the same.

**Two modes.** *Precise* Selewa, for commitments and accords: every role explicit, no ambiguity. *Open* Selewa, for song, story and prayer. Both use the same roots.

**Words become provisions.** A text in precise Selewa can be compiled into an accord's provisions, so the words people sign and the rules the app applies are one text. Accords are built from promises, not commands:

| Kind | What the tool does |
| --- | --- |
| We promise | Reminds, records, celebrates; never blocks |
| We can | Makes it easy |
| We ask | Shows the request; anyone may say no |
| We hope | Keeps it visible |
| Protection | Enforced, and only to protect people (privacy by encryption) |

Example, from Work Day: *"We promise: each season, we gather for one work day. Whoever can, comes. Whoever cannot, is not blamed."* compiles to a recurring event, an optional RSVP, thanks for those who came, and a protection: no record of absence.

**The circle decides what it means.** Open phrases such as "when we can" or "fairly" compile to a single instruction: the circle decides. If the tool's reading and the circle's understanding ever differ, the circle is right and the text is fixed. This is the reverse of "code is law."

**Signing meaning.** Members sign the hash of the canonical meaning tree; each language version is a view of what was signed. Rendering must be deterministic and checked by more than one independent renderer, so no one can show a gentle translation of a harsher meaning.

**Writing an accord becomes writing.** A member writes sentences in their own language; the app shows a paraphrase back ("Did you mean…?"); they confirm; it compiles, the simulator tries it, and the circle adopts it. Amendments show as changes in meaning. Conflicts with accords the circle already holds are flagged before adoption.

**The AI is never in the trust path.** It helps draft and suggests parses. A person confirms every parse, and after that only the deterministic compiler acts.

**New threats.** Ambiguity attacks (text crafted to parse differently than it reads) and rendering attacks (a translation that misrepresents what was signed). Defences: the paraphrase round trip, signing the canonical tree, and several independent parsers and renderers that must agree.

**Bootstrapping, as a compiler does.** Stage 0: the grammar written in English and other host languages, reviewed by native speakers of many languages so no single one leaks into the result. Stage 1: the Charter written in Selewa. Stage 2: the grammar and dictionary written in Selewa. Stage 3: someone who learned only from the Selewa grammar rewrites the Charter, and it matches. For accords: words and `accord.toml` written separately, then Selewa compiled into TOML, then the Selewa text is the accord and the TOML is generated.
