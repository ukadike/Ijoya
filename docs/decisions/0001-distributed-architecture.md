# 0001 — Distributed architecture, no master sculpture

**Status:** Accepted (mandated by the project directive)

## Context

Ìjóyà is about interdependence — no body functions alone, and each body
should possess only part of the overall capability (sensing, movement,
vibration, pressure, environmental awareness, communication, support,
response). A centralized controller would make coordination technically
simpler, but it would also let any one body's behavior be explained by "the
controller told it to," which erases the thing the installation exists to
show: that dependency is real and physical, not orchestrated from above.

## Decision

Never design a master sculpture or central controller. Each body holds only
part of the overall capability set. Coordination happens through the shared
[behavioral language](../behavioral-language.md) passed directly between
bodies (ESP-NOW, LAN, serial, I²C, or OSC as appropriate), not through a
central process that dispatches instructions.

## Consequences

- Harder: debugging is distributed — there is no single log of "what the
  installation is doing," only what each body did and what it sent/received.
- Harder: behaviors that would be trivial with a central scheduler (e.g.
  precise synchronized timing) must instead emerge from local
  sensing/messaging — and per the directive, near-synchrony should be
  avoided anyway ("avoid synchronized animatronics").
- Easier: any single body can fail without taking down the installation's
  legibility — the remaining bodies still behave, just with less to respond
  to.
- Required: every new behavior must be checked against this — if it only
  works because one body "knows everything," it violates this decision and
  should not be merged.
