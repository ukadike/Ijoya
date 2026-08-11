# Architecture Decision Records

ADRs capture significant, hard-to-reverse decisions and the reasoning behind
them, so future contributors (including the artist, returning after a gap)
don't have to reconstruct *why* without re-litigating it each time.

## When to write one

Per the project directive: "Document all significant architectural
decisions." Write an ADR when a decision is hard to reverse, affects more
than one body, or trades off against one of the design priorities
(artistic integrity, accessibility, interdependence, safety, reliability,
simplicity, performance).

Do not write one for routine implementation details that a normal commit
message already explains.

## Format

Each ADR is numbered sequentially (`0001-`, `0002-`, …) and contains:

- **Status:** Proposed / Accepted / Superseded (by ADR ####).
- **Context:** What prompted the decision.
- **Decision:** What was decided.
- **Consequences:** What this makes easier or harder, including any
  accessibility, safety, or interdependence trade-offs.

## Index

- [0001 — Distributed architecture, no master sculpture](./0001-distributed-architecture.md)
- [0002 — Local-only communication, no cloud dependency](./0002-local-only-communication.md)
