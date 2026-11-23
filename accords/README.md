# Accords

The Charter is the root accord; every other accord grows from it or from another accord. A circle adopts the Charter first, then the accords that fit its purpose, and makes each one its own.

Each accord is a folder:

```
<accord>/
  accord.toml     name, version, grows-from, requires, licence, provisions
  words/en.md     the words members read and sign (one file per language)
```

Provisions are language-neutral and use only the building blocks defined in the accord-format RFC.

| Accord | Kind |
| --- | --- |
| `charter` | Root |
| `mutual-aid` | Everyday |
| `gifting` | Everyday |
| `work-day` | Everyday |
| `licensing` | Practice |
| `standards` | Practice |
| `pattern-sharing` | Practice |
| `selewa` | Practice (seed) |

The full accord tree is in `rfc/drafts/accord-format.md`.
