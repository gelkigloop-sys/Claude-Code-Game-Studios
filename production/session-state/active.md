# Session State — Jock's Quest

Updated: 2026-07-17 (end of session — paused deliberately, resume tomorrow)

## Project Snapshot
- Stage: Concept (`production/stage.txt`), review mode: lean
- Game: **Jock's Quest** — comedy 2.5D action-platformer (Jock + dog Benji,
  Australian mountain wilderness, mushroom hunters). Glen's high-level design
  guide is in the first user message of session history — NOT yet formalized
  into `design/gdd/game-concept.md` (the /brainstorm flow was intentionally
  skipped in favour of prototype-first).

## What Exists (all committed on claude/game-development-bou0do)
1. `prototypes/jocks-quest-movement/` — first 2D feel test (concluded, superseded)
2. `prototypes/jocks-quest-level1/` — COMPLETE 2D Level One, v2 painterly +
   soundscape. Fully tested (headless harness 10/10 + gate test + screenshot
   verification). The reference implementation for all gameplay logic.
3. `prototypes/jocks-quest-3d/` — Three.js 2.5D rebuild. **WIP**: boots and
   plays cleanly (verified), but the build agent was stopped mid-polish
   (roo tail geometry fix + final screenshot-review iteration unfinished,
   agent-written README replaced by a stub). Build pipeline lives in
   scratchpad `build3d/` (src/main.js + esbuild + inject_voice.py) — NOTE:
   scratchpad is ephemeral; the committed index.html is the only durable copy.
4. `assets/audio/voice/jock/` — Glen's 10 recorded voice clips (embedded in
   both playable builds via base64 VOICE_DATA injection).

## Higgsfield Assets (generated, PARKED in Glen's library — not yet in game)
- Music (sonilo_music, completed): bush-morning explore theme 40s
  (job 1b735728-68e4-494f-8c70-5d188a56eeea), outback chase 30s
  (job f532811d-377d-4ee0-9afa-50612a938dfb)
- Voice clone "Jock" (element voice_id e7e8f245-6e27-4766-979f-ddd189ff57e0)
- 6 cloned lines (completed jobs): bloody-hell 2e15569c, incident-report
  93e2cafa, nope-nope c7cee3c0, paws-off-fungus 6389812f, influence-ya
  0f4b4c39, cuppa-later e9b73c5e
- Glen said "use the clips you already have for now" — generated audio is
  NOT wired in. To integrate: Glen downloads from Higgsfield and drags files
  into chat (container network policy blocks direct CDN downloads:
  upload.higgsfield.ai and cloudfront hosts are CONNECT-403).

## Next Steps (tomorrow)
1. Glen playtests the 3D build; verdict on 3D vs 2D direction.
2. If 3D: relaunch a polish/verification agent on jocks-quest-3d (finish roo
   geometry, screenshot iteration, perf check; regenerate README with results).
3. Optionally integrate parked music + cloned lines when Glen uploads them.
4. Then the deferred pipeline: /brainstorm (fast — design guide answers most),
   /setup-engine, /art-bible → formal GDD work. Engine still unconfigured.

## Delivery Notes
- Artifacts: 2D Level One at claude.ai/code/artifact/73c40400-…, movement
  proto at 14371e21-… (require claude.ai login — Glen prefers SendUserFile
  render into the panel; that worked).
