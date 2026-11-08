# Clips check (gate B) — run 2026-11-08-0230-2t-proactive-problem-solver

Producer stage B, 2026-11-08. Prompts = prompt-review pass 2 replacements (C01, C03, C06, C08, C10, C20) word for word; C21, C24 unchanged; C06 start-only (owner). All kling3_0 pro, 3 s (3.04 s, 1076×1924, 24 fps), 9:16, sound off, 1 output each, preflight 5.25 each. Six frames per clip pulled with ffmpeg and viewed (plus zoomed crops for C06, C20). Files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/clips-2t/`.

| Clip | Generation ID | Frames | Credits | Gate B | Note |
|---|---|---|---|---|---|
| C01_FLOP | `7bd30ef7-4620-49c7-a9f4-082df7c8ef91` | P01 | 5.25 | **PASS (note)** | Flop onto pillow, lands eyes closed, mouth closed, nightstand front empty, lamp steady. Motion smear t≈1.0–1.4 s with one arm flung toward the lamp (cartoony, reads as speed) |
| C03_LAMP | `be68ab42-c1e5-436a-8384-1f5c177bb497` | P03 | 5.25 | **PASS** | Fingertip presses lamp-base switch, shade goes dark at ≈1.5 s, hand slides out frame-left; one hand; head/eyes still; chain still |
| C06_FOLD | `a4c8b26f-dd03-4eb9-bdf6-36aae96fff72` | P06A (start only, owner) | 5.25 | **PASS (trim)** | Pillow stays white; mouth closed; fold lines form at the eye corner t≈1.5–2.0 s then relax by 2.3 s. Use t 0.2–1.9 s (shot 6 = 1.7 s); add the orange glow in code |
| C08_PRESS | `bdb87e0d-1604-4424-a5ca-b04639ad5555` | X08A→X08B | 5.25 | **PASS** | V crease forms under the pillow with orange glow, block steady, no new objects; lands on end frame |
| C10_ALARM | `fe865bee-5794-4822-a789-593adfe2f949` | P10 | 5.25 | **FAIL** | Mouth opens into a gasp from t≈0.5 s (wide O at 1.8 s), stays parted to the end. Usable only t 0–0.4 s; cover the sit-up with a code push on P10 + alarm SFX, or owner-approved redo |
| C20_PRESS_ON | `558ff853-6453-4be2-85da-7b90be38b471` | P20A→P20B | 5.25 | **PASS** | Fingertip presses and glides along the one crescent under the frame-left eye; frame-right eye bare throughout; band and tab steady; clear; mouth closed; other hand on duvet |
| C21_HELD | `244e958c-fb99-4511-b67a-7fbba736264d` | X21 | 5.25 | **FAIL** | Invented dark plunger arm enters from top t≈0.4–2.2 s; clear layer turns milky white from t≈2.3 s. Usable t 0–0.3 s only; alternative: code push on X21 |
| C24_PLUMP | `942d430c-9af8-403c-9061-5db833339580` | X23→X24 | 5.25 | **PASS (note)** | Droplets shimmer then soak in by ≈2.3 s; layer stays flat with bright edge; ends slightly milky as in X24; plumping is subtle |

**Clips:** 6 pass (2 with notes/trim), 2 fail (C10, C21); none redone (owner rule). Clip spend 42.0.

## Voiceover
- **Owner change (Nov 8): voice must be ElevenLabs "Hope", not Lara.** Chosen ID `tnSpp4vdxKPjI9w0GnoV` ("Hope - upbeat and clear", young American female, social media). Other Hope voices in the library: `zGjIP4SZlMnY9m93k97r` (podcaster), `OYTbf65OHHFELVut7v2H` (natural conversations), `uYXf8XasLslADfZ2MB4u` (conversational bestie), `cVd39cx0VtXNC13y5Y7z` (storyteller).
- **Hope NOT generated (blocked):** ElevenLabs connector quota exhausted (192 credits left, 716 needed; request failed, no charge); Runway workspace out of credits; Higgsfield has no Hope voice. Per owner, no fallback voice was used.
- **Superseded Lara take (do not use):** ElevenLabs eleven_v3, voice `vChnJZ1Cu89g2XXumPfT`, generation `QXzpQVlCP3Pz8NOq63Xm`, 716 ElevenLabs credits (0 Higgsfield), **45.84 s**. whisper-cli (small.en) word check: all 133 words present and in order (only tokenisation/digit differences, e.g. "2 a.m.", "4 30"). File: `clips-2t/voiceover.mp3` (kept for reference/timing only).
- **Owner action:** top up ElevenLabs (≥716 credits) or Runway, then generate Hope once with the same text (VO_HOPE in prompts.json).

## Totals
Higgsfield: stills 48.5 + clips 42.0 = **90.5 of the 135 cap** (first-pass limit 120). Balance 1064.5 → **974.0** (matches transactions).

## Owner decision (Nov 8, 2026)
- **C10 accepted as is:** "If her mouth just opens that is okay keep it." Her mouth opening (no speech) is fine.
- **C21 accepted as is:** "C21 is also good, is minor." In the edit, keep the plunger area cropped or short if possible, but the clip is approved.
