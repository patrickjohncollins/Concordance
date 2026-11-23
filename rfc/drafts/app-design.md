# App design

```
RFC:        (assigned on agreement)
Slug:       app-design
Title:      App design
Status:     Draft
Intended:   Informational
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

The app should feel like a quiet notice board for people who know each other, not a social network. Nothing in it competes for attention.

**Built with:** Tauri 2, one codebase for Android, iOS, Windows, macOS and Linux. A Rust core holds Iroh, Automerge, the record log and validation; a small web interface sits on top. The same core runs headless on hearths.

**v0 screens**

| Screen | What it does |
| --- | --- |
| Welcome | Create your key, write down the recovery phrase, choose guardians later |
| Join a circle | Scan an invitation code, read the charter, introduce yourself, sign |
| Circle home | This week's needs and offers, upcoming gathering, people who may want a check-in |
| Needs and offers | Post, answer, and mark done; replies go privately to the poster by default |
| Charter | Current version, history of versions with what changed and who signed |
| Proposals | Open a change, edit the draft together, comment, record agreement |
| People | Members, welcomes and vouches; no counts or rankings |
| Me | My devices, my guardians, my thanks (shown or private), export everything |
| Hearth | Pair a hearth by scanning its code; see that it's healthy |

**Interface principles**

- **No feed, no badges, no infinite scroll.** Lists end. Notifications are a gentle daily summary unless something is urgent.
- **Gentle prompts instead of rules:** "Ana asked for a lift yesterday and hasn't had a reply"; "You haven't heard from Joseph in a while."
- **Plain words:** "sign," "welcome," "leave"; never "keys," "hashes" or "nodes" on the main screens.
- **Accessible from the start:** large text, screen readers, high contrast, translation of the interface and of the charter.
- **The paper path:** a steward screen to record a paper member's agreement or request, with their consent noted.
