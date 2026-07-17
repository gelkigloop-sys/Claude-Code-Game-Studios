# Jock's Quest — Movement & Companion Prototype

## Hypothesis Being Tested

1. **Movement feel**: Jock's run/jump/slide (with coyote time and a slide-jump
   speed boost) is satisfying enough in isolation to carry a platformer.
2. **Companion feel**: Benji following Jock's *actual recorded path* on a
   ~0.7s delay (replaying his jumps at the spot they happened) reads as a
   believable companion rather than a sprite glued to the player.
3. **Voice tone**: Sparse, once-per-run recorded Jock voice lines (per the
   design guide's "selective, never repetitive" audio rule) land comedically
   and make the character feel like *him*.

## How to Run

Open `index.html` in any browser — fully self-contained, no server or build
step needed. Voice clips are base64-embedded (source files live in
`assets/audio/voice/jock/`).

**Controls**: ← → / A D move · Space jump · ↓ / S slide · R reset · M mute

**Voice triggers** (each line plays once per run, no overlapping):

| Clip | Trigger |
|---|---|
| `jock-1/2/3` (random) | First input of a run |
| `leave-my-mushrooms` | First mushroom collected |
| `lil-shit`, spare generics (35% chance) | Mid-run mushroom pickups |
| `get-fucked` | Collecting ALL mushrooms |
| `benji-if-i-start` | Standing idle ~10s with Benji nearby |
| `victory-speech` | Reaching camp with a 100% mushroom run |
| `win` | Reaching camp with a partial run |
| `end-audio-jock` | Outro, after either camp line finishes |

## Current Status

**In-progress** — awaiting feel feedback from Glen.

## Findings

- (pending playtest)
