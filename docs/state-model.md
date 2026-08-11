# State Model

Status: **DRAFT** — awaiting artist review.

Each sculptural body maintains one interpretable state at a time, per the
project directive. States must remain explainable to a visitor, a
maintainer, and an accessibility auditor without reference to source code.

## States

| State | Meaning |
|---|---|
| `RESTING` | Baseline. Not sensing anything requiring a response. |
| `LISTENING` | Attending to sensor input or an incoming message, not yet responding. |
| `RESPONDING` | Actively producing a physical response to touch, another body, or the environment. |
| `SUPPORTING` | Actively lending structure, pressure, or air to another body that sent `REQUEST_SUPPORT`. |
| `REQUESTING_SUPPORT` | Has sent `REQUEST_SUPPORT` and is waiting on / receiving help. |
| `RECOVERING` | Returning to baseline after an active or strained state; visibly slower than a simple return to `RESTING`. |

## Draft transitions

```
RESTING --(sense touch/message)--> LISTENING
LISTENING --(interpret)--> RESPONDING
LISTENING --(interpret)--> REQUESTING_SUPPORT
REQUESTING_SUPPORT --(receives SUPPORT)--> RESPONDING
RESPONDING --(neighbor sends SUPPORT)--> SUPPORTING
SUPPORTING --(RELEASE sent/received)--> RECOVERING
RESPONDING --(input ends)--> RECOVERING
RECOVERING --(settled)--> RESTING
```

This diagram is a starting proposal, not a locked spec — it should be
validated against Prototype 2 and Prototype 3 behavior, where the first real
two- and three-body interactions will show whether these transitions hold up
physically.

## Constraints

- No body should be able to reach every state in the model if its hardware
  cannot support the corresponding capability (e.g. a sensing-only body may
  never need `SUPPORTING`). Which states apply to which bodies is decided
  per body, once bodies are designed — **OPEN QUESTION** until then.
- State changes should be slow/soft enough to read as organic (breathing,
  leaning, yielding) rather than as a discrete machine-state jump. This is
  a physical design requirement, not just a software one.
- Every state should be expressible through at least one non-visual channel
  (vibration, sound, touch, airflow) per the accessibility principle — see
  [`accessibility.md`](./accessibility.md).
