# The hearth

```
RFC:        (assigned on agreement)
Slug:       hearth
Title:      The hearth
Status:     Draft
Intended:   Standards track
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

A hearth is a small, silent, always-on computer that a member plugs in at home. It's just another peer with the member's delegated key: it has no authority, only availability.

- **Hardware:** a low-power single-board computer or a recycled mini PC, with an SSD, no fan, and wired networking. A reference image targets one widely available board first; recycled hardware follows.
- **Software:** a minimal Linux image with the Concordance core running headless, a read-only system partition, and encrypted storage.
- **Pairing, no configuration:**
  1. Plug in power and the router.
  2. On first boot it creates its device key and shows a code (printed label or small screen).
  3. The member scans the code with the app; the member key signs a delegation with role "hearth".
  4. The hearth joins the member's circles and starts syncing.
- **Updates:** signed releases, verified by the hearth before installing, with automatic rollback if the new version fails to start. A circle can choose a slower update channel.
- **What it does in v0:** keeps every log and blob for its circles; relays for phones that are asleep; holds encrypted guardian shares.
- **Later:** erasure-coded storage across hearths (v1); sandboxed shared compute such as local translation, needs-and-offers matching and a local AI model (v2).
- **When a hearth is lost or stolen:** the member revokes it from the app. Everything on it is encrypted or replicated elsewhere, so nothing is lost and nothing is exposed.
