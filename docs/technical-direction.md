# Technical direction

Nothing here has been built or tested. This is specified direction, not validated engineering.

## The governing rule

Technology remains subordinate to the sculptural relationship.

A sensor, motor, microcontroller, light or actuator should exist **only** when it helps make interdependence physically perceptible.

## Design test

Apply to every proposed component:

> Does this make interdependence physically perceptible, or is it merely adding technology or decoration?

## System logic

```
ENVIRONMENT / VISITOR
        ↓
BODY A SENSES OR RECEIVES
        ↓
PHYSICAL / TACTILE / ELECTRONIC CONNECTION
        ↓
BODY B RESPONDS
        ↓
TENSION / MOVEMENT / SIGNAL PROPAGATES
        ↓
COLLECTIVE CONFIGURATION CHANGES
        ↓
THE DANCE EMERGES
```

No response needs to be identical every time. Variation can arise mechanically — from material, weather, position, tension and human interaction — without requiring opaque computation.

## Material systems

- Weather-resistant textile or mesh skins
- Soft stuffed or inflated volumes
- Flexible armatures
- Braided lines or cords
- Articulated or compliant joints
- Removable mechanical connections
- Tactile surfaces

## Electronic systems

- Protected low-voltage electronics
- Sensors
- Vibration elements
- LEDs or diffused illumination
- Soft-robotic or mechanical actuation only where functionally necessary

## Deliberately excluded

**No artificial intelligence. No LLM. No autonomous decision-making.**

This is an artistic position, not a gap awaiting a solution. The central behavior of the work — consequence traveling between bodies — is achieved through sensing, mechanics, tension, haptics and light. Adding a model that decides things would replace a legible physical relationship with an opaque computational one, which is the opposite of the project's argument.

Anyone proposing to add AI to this work should re-read `docs/project-logic.md` §12 and §15.

## Two paths for connection

The mechanism by which consequence travels between bodies is the central unresolved problem. Two approaches, not mutually exclusive:

**Physical.** Tension lines, braided cord, shared armature. Wind or touch moves one body; the connection physically transmits that to another. No power required, fails gracefully, immediately legible to a visitor — they can see the cord. Limited in range and in the kinds of response possible.

**Electronic.** Sensor in one body, actuator or light or vibration motor in another, low-voltage link between. Broader range of response, allows non-obvious pairings. Requires power, weatherproofing, and careful design to stay legible — a visitor who cannot see the connection may not perceive the relationship at all.

The physical path is more consistent with the project's principles and should be the default. Electronic augmentation earns its place only where it makes a relationship perceptible that mechanics alone cannot.

## Open problems

1. **Connection mechanism.** Specified conceptually, unresolved mechanically. This is the critical path.
2. **Outdoor power.** No strategy. Battery, solar, and mains all carry consequences for placement, safety and maintenance across a two-month exhibition.
3. **Weatherproofing.** Textile skins plus electronics plus a full spring outdoors. Untested.
4. **Structural stability at scale.** Bodies that lean on one another must not fall over — and must fail safely if one is disturbed.
5. **Public contact durability.** Touchable surfaces subject to repeated unsupervised handling.
6. **Maintenance load.** What can be serviced in situ, how often, by whom.

## Prototyping sequence

Ordered so that failure happens early and cheaply.

1. Two-body tension test at small scale — can movement in one visibly change the other, mechanically?
2. Same test at increasing scale until structural limits appear.
3. Cowrie node construction — tactile surface, LED diffusion, connection point.
4. Textile skin weather exposure test.
5. Multi-body configuration — does consequence propagate past the second body?
6. Public-contact durability test.
