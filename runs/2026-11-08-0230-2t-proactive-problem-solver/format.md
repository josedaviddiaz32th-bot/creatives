# Format — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Stage 2 (creative-scout), mapping half only (sections 4 and 6). The owner fixed the reference, so no
search was run this time. Sources read: `brief.md` (incl. "Owner instructions for this run"),
`docs/lessons-learned.md` (all; §0–3 and §8 closely), `docs/creative-strategy.md`, `learning/playbook.md`
(all UNTESTED, nothing RETIRED), `learning/production-log.md`, `pipeline/config.yaml`, the swipe-file
breakdown, and the reference's transcript and frame sheets.

## The reference

- **Swipe file:** `learning/swipe-file/2026-11-08-resilia-skeleton-14-day-timeline.md` (full breakdown
  table, source links, winning signal: #2 by total impressions and top video in the Meta Ad Library
  "resilia" search, Library ID 3030773153939023; same copy across 8+ pages and many cuts).
- **What it is:** 2:37 AI 3D cartoon skeleton with a see-through body, second-person narrator VO over a
  music bed, a dated day-by-day run of small wins (Day 1 … Day 14), macro CGI of the hidden mechanism,
  pack in frame from 0 s, brand named only at ~116 s, ~4.5 cuts per 10 s, one-word captions.
- **Core mechanism:** "Watch it happen inside you, step by step." A cute see-through body acts out a
  dated ladder of small, relatable moments while CGI shows the hidden mechanism, so the viewer believes
  the cause before the product is pitched.
- **Watched:** yes (transcript + frames, by the earlier agent; transcript and contact sheets re-checked here).
- **Compliance:** the reference's claims (plaque, blood pressure, heart attack) are not ours and nothing
  of them carries over. Copy the structure only. The swipe note says "do not imitate their skeleton
  character": the owner overrode that for this run (a Pixar-style see-through character is requested).
  Ours stays clearly different: a woman, a translucent skin layer over the face (the "organ" we need to
  see), our bedroom at night, our palette, no kitchen, no pack-swallowing gag.

## Fit with the slot

The reference is TOF→MOF and builds belief in a hidden cause before the pitch, which is exactly the
TOF-U job here (show a cause she didn't know: her pillow folds her face every night). Its ladder of dated
product wins does NOT fit TOF as is (that would make the video mostly product). So the ladder is
**flipped onto the problem**: one night, clock-stamped (LIGHTS OUT → 2:00 AM → 4:30 AM → ALARM →
12:00 PM), showing the crease being made. Then a short second ladder carries the answer: **NIGHT 1 →
MORNING 1**. Same shell, our stage's proportions.

## Mapping table (their element → our P2 version → TOF job)

| Their element | Our persona's version (P2, 38, side sleeper, "tried every anti-wrinkle cream going") | TOF job it serves |
|---|---|---|
| Frame 1: cute see-through skeleton doing an everyday action, pack already in frame | **Pixar-style see-through woman** (glossy ivory skeleton body, a translucent glass-like skin layer over face and hands, dark hair in a low bun, small silver studs, sage sleep shirt) **flops onto her side into a big pillow**; the real Face Set box sits on the nightstand, uncommented | Motion in frame one; weird-but-warm pattern break; product/brand ambient from 0 s |
| Hook: result-in-a-timeframe promise ("this is what happens if…") | **Question hook:** "Why are your wrinkles worse on one side?" (8 words, on screen as the hook text). The timeline that follows is the implied "watch what happens tonight" | Calls out her exact situation (one-sided lines); TOF hooks must be questions (config `structure.hook`) |
| Second-person narrator VO ("you swallow…") | **One second-person narrator** (ElevenLabs Lara, config) narrating *her* night: "You roll onto your side. Same side, every night." The character never talks; jaw stays closed | Viewer projects herself into the character; authority comes from the explainer voice + visuals, no presenter, no credential |
| "Day N" cards as a dated ladder | **Problem ladder, clock stamps:** LIGHTS OUT · 2:00 AM · 4:30 AM · ALARM · 12:00 PM. **Answer ladder:** NIGHT 1 · MORNING 1. Clock times only; never a duration ("7 hours" is banned) | Mini open loops every 3–4 s; ~65% of runtime on the problem |
| Inside-the-body CGI of the hidden mechanism (artery walls) | **Pixar-style skin cross-section:** pillow fabric presses the top skin layer into a V-shaped crease; later the clear patch lies on that layer, the layer stays flat, moisture droplets are held under the patch and the top layer plumps | The "evidence" copy angle: she sees the cause (fold) and the fix (flat + sealed) with no study or number |
| "You thought it was age / genetics" reframe | "You blamed your age. Tried every cream going. But no cream stops a pillow folding your face." Then the opener belief: "A lot of those lines are pressed in while you sleep. So you can stop them." | Reveals the cause she didn't know (opener belief, lessons §2); mild hot take earns comments |
| Real-life proof moments (mirror, BP cuff, coworker) | **Photoreal inserts** of the P2 woman (brief's locked face): the crease at her outer eye on waking; a left-vs-right split at noon (deeper on her sleeping side); MORNING 1 before/after, same light and framing | Makes the cartoon land on a real face; before/afters allowed (lessons §0); no mirror in frame |
| Pack in frame early, brand named late | Box on the nightstand in the bed shots from 0 s; she reaches for it at ~27 s; product name and "The Daily Glow Co." **on screen** at the end and in the caption (not spoken, to keep the VO short and TOF-soft) | TOF must read as a brand, never a tips page |
| Product story + guarantee + scarcity + emotional close | **Dropped.** No price, no guarantee (refund page not fixed, lessons §12), no scarcity. One line of how it works + the morning payoff + soft CTA | TOF "get me interested", not "buy" |
| CTA "Learn more" / "grab yours" | "Comment PILLOW and we'll send you the link." on its own full-screen end-card beat (lessons §8: CTA gets its own beat) | Soft keyword CTA that measures intent |
| ~4.5 cuts/10 s, one-word captions, constant music bed | ≤2.5 s per shot (config `editing.max_shot_seconds`), a change every ≤1.5 s in the first 3 s, ~6 cuts/10 s, word-by-word captions, punch-ins, SFX one per visual event, commercial-library music bed ducked ~10 dB under VO | Fast-paced spec (lessons §0, config `editing`) |
| 2:37 length | **~45 s** (owner, overrides the band; inside TOF 30–50 s) | One idea, starts and ends in this video |

## Hook patterns noted for the scriptwriter (TOF)

From the reference and lessons §3: result-in-a-timeframe ("watch what happens by morning"), counterintuitive
truth ("some of the lines you see in the morning were pressed in overnight"), direct callout of a body
detail (one side worse), POV of a private moment (rolling onto the same side). All are rewritten as
questions in `story.md`.

## The plan

- **Type:** Pixar-style animated explainer with a clock-stamped night timeline + photoreal inserts
  (voiceover only). Counts as this week's "authority-look explainer" for 2-T (one use).
- **Hook pattern:** identification question about her one-sided lines, with motion in frame one (the
  flop onto the pillow) and the hook text on screen within 2 s.
- **Who speaks:** one second-person narrator VO (ElevenLabs, voiceover-only video). **Nobody talks on
  camera.** The Pixar character's jaw stays closed and never moves as if talking; the photoreal woman's
  lips stay closed.
- **Shot style:** mix.
  - **Pixar style** (3D-animated, soft rounded shapes, warm cinematic light; moonlit blue night, warm
    lamp, Sunrise Orange #F08A2C glow for the crease line): the see-through woman in bed, the clock
    stamps, the skin cross-sections, the cream shelf, NIGHT 1 application, sleeping with patches.
  - **Photoreal** (lessons §4 STYLE block): the P2 woman's real crease on waking, the noon left/right
    split, MORNING 1 before/after, the clear sheet in fingers, the product hero/end card.
  - Every shot gets its own approved still (owner). The product/box is never invented: real box asset
    (`face-set-box-v1.png`, job `0f24791e…`) for the nightstand box, hero `39637096…` for the end card,
    Elements + PATCHES block for every patch, including the Pixar ones (clear, never white; forehead
    tab DOWN; slim crescents, never circles or rings).
- **Product timing:** box ambient from 0 s; reach for the box at ~27 s; patch on at ~30 s (NIGHT 1);
  brand on screen ~42 s; CTA end card ~44 s.
- **Pacing:** ~29 shots in ~46 s, none over 2.5 s; clock-stamp cards as pop-ups; word-by-word captions.
- **Length:** ~45 s (owner; `video.seconds_by_stage.tof` 30–50 s).
- **Note for stage 5/6 (cost, not story):** with ~26 new stills, most motion should be code motion
  (push-ins, parallax, pops) on stills; spend Kling seconds only where real motion sells the beat (the
  frame-one flop, the fold forming, sitting up at the alarm). Before/after pair: build the "before" first,
  the "after" as a softening edit of it (production log, confirmed fix).
