# Jock's Quest — Level One: The Foothills (playable build)

## Hypothesis Being Tested

The full vertical-slice loop from the design guide is fun as one continuous
level: movement → exploration → enemy encounter → Jock+Benji puzzle → chase
sequence → character-driven boss → home. This build implements every element
the guide's "Development Priority" section asks for, in a single mobile-first
HTML5 file.

## What's In It

| Design guide requirement | Implementation |
|---|---|
| Jock's core movement | Run, variable-height jump (coyote time + buffering), slide with slide-jump boost, rope swings across creeks |
| Benji's companion abilities | Path-following AI, dig spots (buried rewards), tunnel crawl (gate puzzle), enemy distraction, drone takedown |
| One complete forest level | ~7600px foothills: camp hub → forest platforming → camper country → gate puzzle → roo chase → boss arena → home stretch |
| One enemy encounter | Mushroom-hunting campers with butterfly nets — patrol/chase AI; bounce on them, pinecone them, or have Benji distract them |
| One puzzle | Pressure plate holds the gate half-open; Benji crawls the tunnel to latch it |
| One chase sequence | An extremely cranky kangaroo; slide under low branches, ends with log-assisted comedy KO |
| One small boss fight | Brayden the influencer + camera drone. Multi-stage: dodge swoops + energy cans, ground the drone (Benji steal or 2 pinecones), bounce on him while tangled. Health bar is his follower count |
| Basic camp hub | Starting camp with tent + campfire; campfires double as checkpoints |
| Voice lines (sparse per audio doc) | All 10 of Glen's recorded clips, once-per-run triggers |

Also: 3 hearts + checkpoints, 18 mushrooms (16 placed + 2 buried), golden
mushroom boss reward, title/end screens with run stats, screen shake,
particles, parallax painterly environment, day-warm palette.

## How to Run

Open `index.html` in any browser — fully self-contained (voice audio is
base64-embedded; source clips in `assets/audio/voice/jock/`).

- **Mobile**: landscape orientation; on-screen stick (drag down to slide) +
  jump / 🌰 throw / 🐾 Benji buttons. The 🐾 button pulses when Benji can do
  something contextual.
- **Keyboard**: ←→/AD move · Space jump · ↓/S slide · E throw · Q Benji ·
  R respawn · M mute.

## Verification

Headless Node harness (browser stubbed, real game logic):
title→play, movement, full-level crawl, every set piece exercised, gate
puzzle solved, boss defeated, level completed, restart loop — 10/10 checks
plus a dedicated gate-puzzle test. Found and fixed one real deadlock this
way (drone hover-lerp fighting the swoop state).

## Current Status

**In-progress** — awaiting Glen's playtest.

## Findings

- (pending playtest)
