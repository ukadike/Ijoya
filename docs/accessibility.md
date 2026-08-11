# Accessibility

Status: **DRAFT** — awaiting artist review.

Accessibility is a first-class design principle for Ìjóyà, not an add-on.
Per the project directive, information must be expressible through more than
one modality, and no behavior should rely on vision alone.

## Available modalities

Movement, vibration, sound, touch, airflow, pressure, tension, texture,
light.

Every behavior should use at least two of these, chosen so that a visitor
missing one sense (e.g. sight or hearing) still experiences the behavior
fully.

## Support requirements

- Captions
- Transcripts
- Audio description
- Keyboard accessibility (for any software/interface component)
- High contrast (for any visual/display component)
- Plain language (in all documentation and any visitor-facing text)

## Design rules

- **No color-only meaning.** If light or color is used, pair it with a
  second channel (vibration, sound, texture) that carries the same meaning.
- **No hover-only meaning.** Any interaction that depends on proximity or
  touch must have a non-hover equivalent.
- **Reduced motion.** Physical movement should have a gentle default; any
  software/interface layer must respect reduced-motion preferences.
- **Safety and accessibility overlap.** Movement must remain safe around
  children, wheelchair users, cane users, walkers, guide dogs, and service
  animals — see the Safety section of the project directive. Low force,
  compliant motion, and safe recovery are accessibility requirements as much
  as safety ones.

## Per-behavior checklist

Every behavior documented in [`behaviors/`](./behaviors/) must state its
accessibility impact per the project directive's documentation standard.
Use this checklist when writing that section:

- [ ] Which modalities express this behavior's information (list at least two)?
- [ ] Does anything about this behavior rely on vision alone? If so, what's the alternative channel?
- [ ] Does anything rely on hover/proximity alone? If so, what's the alternative?
- [ ] Is there a caption/transcript/audio-description need, and is it met?
- [ ] Is the motion safe and low-force around the visitor groups listed above?
- [ ] Does the behavior respect a reduced-motion default?
