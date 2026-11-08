# Clips check (gate B): run 2026-11-08-0909 "The Problem / Vs… / The Solution"

Stage 7 producer, stage B. The prompts are prompt-review Pass 2's replacements, applied word for word (`prompts.json` revision 2).
All clips are `kling3_0` pro, 9:16, sound off, one output each, and each was preflighted.
Each clip came out 1076×1928 at 24 fps with no audio stream.
Local files and frames: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/clips-trend/` (`<CLIP>.mp4`, `frames/<CLIP>_grid.png`).
I looked at six frames per clip, plus full-resolution face crops for C2.

**Result: 3/3 PASS. Clip spend: 21** (7 + 8.75 + 5.25, same as the preflights). The balance went from 931.4 to 910.4.
**Run total: 45 of the 135 cap** (stills 24, clips 21).

| Clip | Generation ID | Start → end | Cost | Gate B | Notes |
|---|---|---|---|---|---|
| C1_PROBLEM (4 s) | `4a47ae5f-aa57-465e-a9a3-0d412e50519c` | S1 `974e98b0` → none | 7 | PASS | She looks into the lens and touches her cheek, then breaks into a dramatic, wordless wail with her eyes squeezed shut, and starts to fall toward the pillow at the end. The sleep lines stay soft pressed grooves the whole time, with no injury look. His blurred face edge stays at frame-left, the room is stable, and the hands are fine. No patches in this shot. Notes: she lifts her frame-right hand, not the folded one. Her face isn't fully down in the pillow by 4.0 s; she's mid-drop, which is fine for the cut. |
| C2_TUCK_DOZE (5 s) | `d259fbf8-4ee7-4575-ab57-f49049fb33f9` | S6 `3fe0a84c` → S7 `ca4073b6` | 8.75 | PASS | His hand pulls the throw up to her chest and leaves through the top-right; she settles, her eyes close, and the clip lands on S7. All five patches stay clear, flat and in place throughout. No smile, no talking. Notes: **her lips part in a silent sigh at about 2.1–3.2 s** (no words; the owner has waved this through: "If her mouth just opens that is okay keep it"). The edit can also trim it. She grips the throw herself for a moment around 1.5 s. Her claw clip comes into view as her head tilts (it's in S7). |
| C3_EXHALE (3 s) | `c0eee195-16fc-4328-9edc-10b230e4da76` | S8 fix `e26cdd37` → none | 5.25 | PASS | One relaxed exhale with her eyes closed. Head and room are stable, there are no hands, and the patches stay clear and in place. Notes: **her lips part during the exhale at about 0.8–2.4 s** (the prompt asked for "through her nose") and are closed again by the end. There's no smile; same owner waiver as C2. |

Clip URLs are in `budget.json` → `clip_urls`.
**Owner to glance at:** the parted lips with patches on in C2 and C3. A breath, not a smile or speech; keep, or trim to the closed-lip frames.

---

# v3 clips (owner-ordered fix, ≤40 new credits)

All clips are kling3_0, sound off, one output each, one at a time, and each was preflighted. Local files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/clips-trend/v3_<CLIP>.mp4`, with frame grids in `frames/`.

**Result: 4/4 PASS with notes. Clip spend: 29.0. v3 total: 39.0 of the owner's 40** (balance 910.4 → 871.4). **Run total: 84 of 135.**

| Clip | Generation ID | Mode / s | Frames | Cost | Gate B | Notes |
|---|---|---|---|---|---|---|
| C_NIGHTS | `bbac6e12-6e51-4d81-b6c9-8e633e909872` | pro 4 | ST_NIGHT → none | 7 | PASS | Real-time sleeper motion: she nuzzles into the pillow and her hand grips it. Locked camera, eyes and lips closed, one hand, no injury look. Note: at about 1.6–2.0 s she lifts her head off the pillow and resettles (continuous, no jump), and her face looks briefly smoother at the top of the lift. **Edit windows:** 0–1.3 s and 2.2–4.0 s (face squashed). |
| C_BATH_GIVE | `35f390ea-b025-4a07-b508-4f28e4ace9fd` | pro 5 | ST_BATH_BEFORE fix → ST_BATH_GIVE | 8.75 | PASS | She studies her face with a small, real frown, and her fingertip touches the creases near her eye (no overacting). His hand brings the film in from the frame-right, and she gives a small closed-lip smile. The film's five pieces are clear with the tab down, never more than two hands. Notes: the crease texture looks a little coarse in close-up, but it's skin-coloured grooves, not injury. A plain mirror-cabinet panel appears behind her from about 3 s with nothing reflected. Her rising hand is motion-blurred at about 3.8 s. |
| C_APPLY | `8db7ef3d-928a-41a5-9ee3-5c1942e47f1f` | std 3 | S4 → S5 | 4.5 | PASS (note) | She presses the band (frosted and see-through, tab DOWN), then the crescents. No smile, no talking, and it ends on S5 with all five clear pieces. **Defect:** Kling inserted a hard cut at about 2.05 s, from the close-up to the wide S5 framing (against "no cuts"). Use it as two shots split at 2.05 s; the planned window 0.80–2.80 crosses the cut. Output is std resolution, **716×1284**, so it needs upscaling to 1080×1920 in assembly. Logged. |
| C_AFTER | `4c520df3-2cd4-4fcd-b2e3-0039f6eb18ad` | pro 5 | ST_BATH_AFTER → none | 8.75 | PASS | Same framing as the before. Her fingertips glide over the cheek and forehead, then a small, real smile (no patches on, so allowed). The skin stays smooth with no creases. One hand. The shelf stays clear for the box composite. Note: natural smile lines form at her outer eyes at the smile peak (about 4.5–5 s), which slightly undercuts "softer lines". The cleanest payoff is about 3.3–4.3 s. |

**Owner checks:** no exaggerated reactions; no mirror reflection anywhere; no patches turn white; the tab is DOWN; nothing looks like an injury; and every beat is now video.
**Owner to glance at:** the bathroom face reads older and more tired than the night face. The crease texture in the bathroom close-up is a little coarse.
