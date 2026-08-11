# Behavioral Language

Status: **DRAFT** — awaiting artist review.

Per the project directive, bodies communicate through semantic messages, not
raw actuator values. This keeps behavior explainable and keeps any one body
from depending on another's internal implementation — only on the meaning of
the message it sends or receives.

A message describes *intent*, not a device state. The receiving body decides
how to physically interpret it (which chamber inflates, which motor turns,
how much tension changes) — that mapping is repairable/tunable per body
without changing what the message means to the rest of the installation.

## Message vocabulary

| Message | Sent when | Typical receiving response |
|---|---|---|
| `REQUEST_SUPPORT` | A body senses it needs help holding a posture, pressure, or position it cannot sustain alone. | A neighboring body moves toward `SUPPORTING`. |
| `SUPPORT` | A body is actively lending structure, pressure, or air to another. | Receiving body's posture stabilizes; may transition out of `REQUESTING_SUPPORT`. |
| `TOUCH` | A body senses contact (visitor or another body). | Receiver may transition to `LISTENING` or `RESPONDING`. |
| `RESPOND` | A body reacts to a prior `TOUCH` or `CALL`. | Physical response appropriate to that body's capability (movement, vibration, sound). |
| `WAIT` | A body has sensed something but is holding before acting, e.g. waiting on another body's `ANSWER`. | Receiver understands not to expect immediate follow-through. |
| `REST` | A body is settling back to baseline. | Neighboring bodies may ease their own tension in response. |
| `RECOVER` | A body is returning from an active or strained state to baseline. | Should be visibly slower/gentler than `REST` — signals depletion, not just idleness. |
| `FOLLOW` | A body invites another to mirror or continue a movement. | Receiver echoes or continues the motion, propagating it further. |
| `RELEASE` | A body is releasing tension, pressure, or air it was holding for another. | Receiving body's supported state ends; it should transition toward `RECOVERING` or `RESTING`, not snap. |
| `TENSION` | A body is holding or increasing structural tension. | Connected bodies may feel a pull or posture change — this is where "borrowed function" becomes physically visible. |
| `BREATH` | A cyclical, ongoing signal representing a body's baseline living rhythm. | Other bodies may synchronize partially, never in lockstep (avoid "synchronized animatronics"). |
| `CALL` | A body reaches out for another body's attention or presence. | Receiver may `RESPOND`, `ANSWER`, or hold in `WAIT`. |
| `ANSWER` | A direct reply to a `CALL`. | Confirms the calling body is not alone; closes the call/response pair. |

## Design constraints

- No message should map 1:1 to a raw actuator command (e.g. no
  `SET_SERVO_ANGLE`). If a new behavior seems to need one, it likely belongs
  in a body's local interpretation logic, not in the shared vocabulary.
- Messages should be meaningful without requiring the sender to know how the
  receiver will physically respond — this is what keeps bodies independent
  in *implementation* while dependent in *function*.
- New messages should only be added when an existing one cannot express the
  intent. Prefer reusing this vocabulary over growing it.

## Open questions

- Exact wire format / transport encoding (ESP-NOW payload layout, OSC
  address scheme, etc.) — **OPEN QUESTION**, to be resolved during
  Prototype 2 (first two-body message exchange).
- Timing/timeout semantics for `WAIT` and `CALL`/`ANSWER` pairs — **OPEN
  QUESTION**.
