# Jock's Quest — Level One 3D (Three.js 2.5D rebuild)

## Hypothesis Being Tested

Does Level One's proven design hold up in true 2.5D — real-time 3D stylised
characters and environments on a side-scrolling camera — as the original
design guide intended? Does 3D read better than the painterly 2D build
(`prototypes/jocks-quest-level1/`)?

## What's In It

Same complete game as the 2D Level One (all gameplay logic ported: movement,
rope swings, Benji command AI, camper enemies, gate puzzle, roo chase, boss
fight, checkpoints, mushrooms, voice clips, HUD) rendered with Three.js:
low-poly terrain ribbon from the level heightmap, 3D pines/gums, articulated
primitive-built characters, region-graded sun/fog (morning camp → sunset
arena), campfire point lights.

## How to Run

Open `index.html` in any browser — fully self-contained (Three.js bundled,
voice clips base64-embedded).

Controls: A/D move · Space jump · S slide · E throw · Q Benji · R respawn ·
M mute. Touch: stick + ⤒ 🌰 🐾 buttons.

## Current Status

**In-progress — build agent's polish pass was interrupted mid-run** (stopped
deliberately to pause the session). The build boots and plays cleanly
(verified: no console errors, physics working, full HUD). Known outstanding:
the agent was fixing roo tail geometry and had not finished its final
screenshot-review iteration or its own README. Resume by relaunching the
polish/verification pass against this file.

## Findings

- (pending playtest; 2D vs 3D comparison pending Glen's verdict)
