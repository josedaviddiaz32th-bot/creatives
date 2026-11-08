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
