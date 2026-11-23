# Build native Git hosting, borrowing Radicle's ideas

Status: Accepted (stewards' circle of one, 2026-11-22)

## Context

Concordance must host its own complete definition. Radicle provides peer-to-peer Git but is changing transport.

## Decision

Build native Git hosting on gitoxide: Git packs synced over Iroh, branches as signed records, canonical refs defined by stewards' signatures, a git-remote-concordance helper, hearths as seeds.

## Consequences

Outside security review of peer authentication and ref validation before reliance.
