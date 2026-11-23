# Use Iroh for peer connections

Status: Accepted (stewards' circle of one, 2026-11-22)

## Context

Peers must connect directly by key, through home routers, without a central server.

## Decision

Use Iroh 1.0 (QUIC, dial by public key, hole-punching with relay fallback), with iroh-gossip and iroh-blobs.

## Consequences

Wire-protocol stability since 1.0; circles may run their own relays.
