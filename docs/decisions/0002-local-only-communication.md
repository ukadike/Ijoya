# 0002 — Local-only communication, no cloud dependency

**Status:** Accepted (mandated by the project directive)

## Context

The installation is a physical artwork situated in a garden. If any part of
its core behavior depended on an internet connection or a cloud service, it
would fail in ways unrelated to the art (network outage, service
deprecation, connectivity cost in a garden setting) and would introduce a
dependency the artwork's own concept doesn't call for — the bodies depend on
each other, not on a remote service.

## Decision

Use local communication only: ESP-NOW, Wi-Fi LAN, serial, I²C, or OSC where
appropriate. The installation must function fully without internet access.
No AI/ML service, cloud API, or remote dependency is part of the operation
of the installation (see also the project directive's AI Policy — emergence
comes from distributed communication, environmental sensing, physical
interaction, and state transitions, not machine learning).

## Consequences

- Harder: no remote monitoring/logging dashboard without deliberately
  building one as a separate, non-critical add-on that the installation
  does not depend on to function.
- Easier: the installation is repairable and operable in a garden with no
  reliable connectivity, and won't degrade or stop working if an external
  service changes or is discontinued.
- Required: any future feature proposal that needs a cloud service or an
  ML model to operate should be rejected per this decision and the
  directive's AI Policy, unless it is explicitly non-critical tooling kept
  outside the installation's operation.
