# Build the app with Tauri 2 and a Rust core

Status: Accepted (stewards' circle of one, 2026-11-22)

## Context

One codebase is needed for Android, iOS and desktop, with the same core on hearths.

## Decision

Tauri 2 for the app; a Rust core holding Iroh, Automerge, records and validation; the same core headless on hearths.

## Consequences

Open question: whether mobile background sync needs native code.
