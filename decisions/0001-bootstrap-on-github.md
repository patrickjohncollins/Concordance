# Bootstrap the repository on GitHub

Status: Accepted (stewards' circle of one, 2026-11-22)

## Context

Concordance will host its own repository through native Git hosting, which does not exist yet. A conventional host is needed until then.

## Decision

Host the repository on GitHub, on a personal account, as a temporary bootstrap. Keep everything important in plain Git and Markdown; record decisions in `decisions/`, not in GitHub issues or discussions; use no GitHub-only features for anything that must move.

## Consequences

Move the repository, with full history, to Concordance once native Git hosting passes its gate. GitHub then becomes a mirror or is retired.
