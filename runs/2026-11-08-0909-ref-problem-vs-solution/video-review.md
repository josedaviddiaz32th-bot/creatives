# Video review (stage 8): run 2026-11-08-0909 "The Problem / Vs… / The Solution" (v1)

Reviewer: video-reviewer, independent. Read: `learning/owner-feedback.md` (first), `CLAUDE.md`, brief owner
section, `story.md` v2, `story-review.md`, `clips-check.md`, `assembly.md`, `qa.json`, lessons §10 checklists.
**Judged as a TREND REMAKE** (owner rules: same length, captions, timings and cuts, same vibe and story, no
speech, sound added in-app), not by the TOF spoken-hook/CTA/length rules. No credits spent; video not edited.

**How I checked:** ffprobe on `final.mp4`; 22 full-res frames (1080×1920) at every cut and caption change,
each paired side by side with `ref.mp4` at the same time; full-res crops of her face (shot 1 creases, shots
4/5/6/7/9 patches), both box composites, and the "Vs…" band in shots 3–4; frame-difference check (YDIF) on
the still-based shots for handheld motion. Frames: `scratchpad/vrev/` (session scratchpad).

## Verdict: **PASS** (with 3 free polish fixes recommended before posting)

No score below 8 (`review.min_score_to_publish` = 8). Claims clean. Budget 45 / 135.

## Hard facts
| Check | Result |
|---|---|
| Duration | 15.067 s vs ref 15.067 s (−0.007 frame) ✅ |
| Format | 1080×1920, 9:16, 30 fps, H.264 + silent AAC (−91 dB) so the apps accept it; owner adds the sound ✅ |
| Cuts | all 9 ref cuts on the exact frame, plus the ref's in-shot re-frames at 3.833 / 6.7 / 7.167 ✅ |
| Captions | "The Problem 😭🛏️" 0–3.267, "Vs…" 3.267–10.0, "The Solution 🤤❤️" 10.0–end; same height, size, centring and white-outline style as the ref (side-by-side checked) ✅ |
| Speech | none; no voice, no on-screen claim ✅ |

## Scores (1–10)
| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Trend fidelity (length, cuts, captions, story arc) | 10 | Cut-for-cut match; same misery → partner's caring build → bliss arc; the box replaces the body pillow at the same beat |
| 2 | Problem reads instantly / never injury | 8 | Soft pressed grooves on her frame-right cheek, fingertip traces one at ~1.6 s, then a big wordless cry under "The Problem 😭🛏️". **Nothing reads as injury** (full-res crops: texture, faint pink flush, no red streaks). The grooves are subtle at phone speed; the caption + cry carry it. Acceptable trade-off given the owner's injury rule |
| 3 | Product moment clear | 9 | Real box lands at 3.27 s, sheet insert 4.37, band-on 4.77, full set 5.2 — the turn is unmistakable |
| 4 | Patches correct | 8 | 5 pieces, forehead **tab down** between the brows (shot 3 sheet and shot 4 face), crescents under eyes and along smile lines, lips uncovered, flat, skin visible through them. Note: in C2/S9 the under-eye crescents read a touch milky/chunky (frosted, not opaque) — passes checklist, not ideal |
| 5 | Box composite looks real | 9 | Label sharp and correct, perspective and shading match, contact shadow kept, fingertip correctly in front (S2); S10 nightstand box lit from the lamp side, beside the glass. Doesn't read pasted |
| 6 | Same two people / continuity | 8 | Same woman throughout (face, double gold studs, grey crewneck, claw clip); same man (stubbled jaw shot 1; hairy forearm + navy sleeve shots 3/6). Hair: cool ash-brown in shot 1 vs warm honey/strawberry in 2–10 — explained by the morning vs lamp grade, reads as the same person |
| 7 | No smile with patches | 9 | Calm, eyes closed, no smile in 5–10. Lips part in C2 (~7.6–8.3 s) and C3 (~10.3–11.6 s) as a silent breath — owner-waived ("If her mouth just opens that is okay keep it") |
| 8 | Caption style / placement | 8 | Style and position match the ref. **"Vs…" sits on the inner ends of the top crescents in shot 3 (4.37–4.77) and across her upper lip/mouth in shot 4 (4.77–5.2)** — 0.83 s total, minor at phone speed but against the brief's "not covering faces/patches" |
| 9 | Handheld feel / grade | 9 | Still-based shots carry the same frame-to-frame motion as the clips (YDIF ≈3.2–4.3 vs 3.3); grain and sway match; morning-cool vs evening-warm grade mirrors the ref's day → night |
| 10 | Anatomy / uncanny at phone speed | 8 | Hands 5 fingers where visible; no melting. Shot 3: his forearm is long and the elbow angle a bit odd, but it's on screen 0.4 s. Nothing uncanny at speed |
| 11 | Claims | 10 | No claim spoken or shown; only the ref's captions |
| 12 | Budget | 10 | 45 of the 135 cap |

### Checklists B/C (lessons §10), trend-remake subset
- ✅ Patch clear and slightly frosted, never opaque · ✅ tab down · ✅ crescents, not circles · ✅ right count (5) and placement
- ✅ No smile with patches · ⚠️ lips part (owner-waived breath, no speech) · ✅ hands 2 × 5 where visible
- ✅ Wrinkles/creases don't change mid-clip in shot 1 · ✅ text in safe zone · ✅ real box asset, never model-drawn
- n/a (trend rules): spoken hook, CTA full-screen beat, live price, −16 LUFS, music licence — owner adds the trending sound in-app (publisher: confirm the account can use it)

## Fixes (all optional polish; none blocks PASS)
1. **[free]** Shot 3 (4.37–4.77): re-frame the S3 still (shift the sheet up ~120 px or scale so "Vs…" at y≈956 lands in the backlit gap below the top crescents) so the caption doesn't overlap the crescent tips.
2. **[free]** Shot 4 (4.77–5.2): re-frame S4 so "Vs…" lands on her chin/collar, not her upper lip (push in ~1.08× and lift the face ~110 px, keeping the full forehead band and both hands in frame).
3. **[free]** Shot 1 (0–1.9): optional mild local contrast/clarity on the frame-right cheek groove area (texture only, no added red) so the pillow creases read a beat faster. Re-check full-res afterwards that nothing reads as a scratch.
4. **[needs credits — not recommended]** Milky under-eye crescents in C2/S9: only fixable by regenerating; within owner tolerance, leave as is.

## Logged
Two lines added to `learning/production-log.md` (caption band over patch/face in shots 3–4; milky under-eye crescents in C2/S9).
