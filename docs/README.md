# Ìjóyà Documentation

This is the documentation index for *Ìjóyà: Borrowed Function in the Garden*.
It exists to keep the artistic concept, the accessibility commitments, and the
distributed-systems design legible as the installation grows — see the
project directive at [`/CLAUDE.md`](../CLAUDE.md) for the governing rules.

Status markers used throughout these docs:

- **DRAFT** — a working proposal, not yet confirmed by the artist.
- **CONFIRMED** — reviewed and accepted as the working reference.
- **OPEN QUESTION** — a decision that has not been made yet.

## Contents

- [`behavioral-language.md`](./behavioral-language.md) — the semantic message
  vocabulary bodies use to communicate (`REQUEST_SUPPORT`, `SUPPORT`, `TOUCH`, …).
- [`state-model.md`](./state-model.md) — the interpretable states each
  sculptural body can be in (`RESTING`, `LISTENING`, `SUPPORTING`, …).
- [`prototype-roadmap.md`](./prototype-roadmap.md) — tracks progress through
  Prototypes 1–5 as defined in the project directive.
- [`accessibility.md`](./accessibility.md) — the accessibility principles and
  the checklist every behavior must satisfy.
- [`decisions/`](./decisions/) — architecture decision records (ADRs) for
  significant, hard-to-reverse choices.
- [`behaviors/`](./behaviors/) — one document per implemented behavior,
  following the documentation standard in the project directive.

Nothing here invents hardware, canon, or behavior that hasn't been decided.
Where a decision is still open, it is marked `OPEN QUESTION` rather than
guessed at.
