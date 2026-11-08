# Brief — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Stage 1 (persona-picker). Sources read today (2026-11-08): `CLAUDE.md`, `pipeline/config.yaml`,
`docs/lessons-learned.md` (§0–3 in full, plus §4, §7, §8, §10, §11, §12), `docs/creative-strategy.md`,
`learning/playbook.md` (everything UNTESTED, nothing RETIRED), `learning/next-moves.md` (no results:
follow the matrix), `runs/history.json` (1-T done), the previous brief
`runs/2026-11-07-2002-1t-first-line-fixer/brief.md` (layout), the Avatars Google Doc
(`1ySwoyCBQVAL59c04-La1qvvPs1qI766vbqMqYzMZJ0w`, read live with Drive `read_file_content`; checked
character-for-character against the plain-text export from `download_file_content`; this section has
no emojis, and its apostrophes are straight ASCII in the export).

**Creative reference (fixed by the owner):** the top-impression ad from the Meta Ad Library search
"resilia". Another agent breaks it down into `format.md`; this brief doesn't depend on it. Stage 2 maps
its shape onto this slot (authority-look explainer + crease visuals), copying the format, never its
words, face or brand.

## Persona (verbatim from the Avatars doc, section "PERSONAS/AVATARS BASED ON REDDIT")

> **The Proactive Problem-Solver (30s-40s)**
>
> This group is generally in their mid-thirties to forties and actively seeking effective solutions for existing wrinkles, often after realizing that lifestyle choices have impacted their skin. They are willing to invest in science-backed products or professional treatments.
>
> Acknowledging past neglect: They recognize the impact of lifestyle on their skin and are motivated to change. "I'm 37, treated my body like absolute trash the past....life. I imagine that these around the underside of my eyes are permanent wrinkles at this point, but I'm hoping there's something I can do to help."
>
> Seeking powerful treatments: They are interested in stronger solutions like prescription retinoids or cosmetic procedures beyond basic creams. "Tretinoin is what you want."
>
> Questioning product efficacy: They are skeptical of over-the-counter anti-wrinkle creams and seek genuine results. "I think I have tried every anti-wrinkle cream going... and not one of them improved my fine lines."

(Complete section: heading with age range, description paragraph, all three labelled traits and all
three quotes. Nothing trimmed. Unlike the First-Line Fixer, this section in the doc has no "Key
concern / Behavior / Emotional trigger" labels and no emojis; its own labels are copied as they are.
Her word "permanent" stays here as her quote only; see claim translation.)

### Picker's notes on her (separate from the verbatim section)
- **Age / situation:** 38. Busy, practical; years of short sleep, sun and not much of a routine have
  caught up with her. Fine lines under the eyes and at the outer corners, forehead lines, and a crease
  that is **deeper on the side she sleeps on** (she always sleeps on her right side). She's bought
  plenty of creams; none changed her fine lines. She researches before she buys and wants a reason
  that makes sense ("science-backed").
- **What she feels:** a bit guilty ("I treated my skin like trash"), resigned that some lines may be
  "permanent", but hopeful there's something she can still do. Tired of paying for creams that do
  nothing. Not panicked, pragmatic: she wants the *cause*, then a fix that works on it.
- **How she talks:** direct, a little self-deprecating, no-nonsense; likes a clear "here's why"
  explanation; knows the word tretinoin; distrusts hype.
- **Real quotes to draw from** (Avatars doc unless marked):
  - "I'm hoping there's something I can do to help."
  - "I think I have tried every anti-wrinkle cream going... and not one of them improved my fine lines."
  - "treated my body like absolute trash the past....life"
  - "It's my pillow, not me." (lessons §2, side-sleeper situation)
  - "they do seem to blur wrinkles after waking" / "noticed a difference after the first night" (lessons §2, her own words)

## Slot
- **Why this slot:** `runs/history.json` has 1-T done (P1 First-Line Fixer, posted by the owner on
  TikTok 2026-11-08). The next slot in the posting order (strategy §7, day 1, 15:17) is **2-T**, and its
  persona is **P2, not P1**, so it meets the owner's request for a different persona with no skipping.
- **Slot ID:** 2-T
- **Persona:** P2 = The Proactive Problem-Solver (Avatars doc)
- **Desire:** comfort / control (strategy §3): it's not her, it's her pillow, and that's something she can control
- **Awareness:** **TOF-U**. She sees her lines (and that one side is worse) but doesn't know that her
  pillow folds her face for hours every night, and doesn't know overnight patches answer that
- **Funnel stage:** TOF, "get me interested": ~80% the problem (one-sided lines, the pillow fold,
  crease visuals, the cause she didn't know, why creams don't touch it); last ~20% the patch as the
  answer with one line on how it works; brand visible (box/product in shot, brand name on screen and
  in the caption). Never a tips page.
- **Video type:** authority-look explainer: your pillow folds your face for hours a night; crease visuals
- **Presenter:** authority look (knowledgeable "skincare nerd" / educator styling), **no stated
  credential** spoken, on screen or in the caption
- **Copy angle:** evidence (the mechanism, crease visuals)
- **Comment keyword:** PILLOW
- **Target length: ~45 s (owner)** (owner's instruction, Nov 8, 2026; inside the TOF band of 30–50s,
  `video.seconds_by_stage.tof`). At `words_per_second` 3.0 that's ≈ 135 spoken words.
- **Credit cap:** 135 (`budget.max_credits_by_stage.tof`); 15 held back for retries → **≤120 first pass**.
  Budget is tight at 45s: if she talks on camera for all 45s on Kling 3.0 Pro (≈2.5 credits/s) that's
  ≈112 credits before stills. Keep stills to a few credits (reuse §7 assets, cutaways as checked stills
  with code motion), and let the prompt-engineer price Kling std (≈2 credits/s, ≈90) as the fallback.
  Preflight every job. **No credits spent at this stage.**
- **Hook direction (strategy §4):** "Why are your wrinkles worse on one side?" (pairs with angle 2's
  own "Seeing wrinkles on only one side of your face?")
- **Product timing (strategy §2):** may sit in frame earlier without comment (e.g. the box on her desk
  or nightstand); spoken about only in the last ~20%.
- **Black Friday:** don't mention it (see Price check).

## Tags for runs/history.json
| Tag | Value |
|---|---|
| slot | 2-T |
| persona | P2 (The Proactive Problem-Solver) |
| desire | comfort / control |
| awareness | TOF-U |
| funnel | tof |
| video type | authority-look explainer (pillow fold, crease visuals) |
| presenter | authority look (no credential) |
| copy angle | evidence |
| hook_type | curiosity / identification question (one-sided wrinkles) |
| length band | 30–50s (target ~45s, owner) |
| belief | opener (lines pressed in overnight by the pillow) |
| objection | none (slot has none) |
| keyword | PILLOW |
| CTA type | soft keyword comment |

## Same persona before
None. This is the Proactive Problem-Solver's first video; her face is new (below) and is reused in
2-M (STAY) and 2-B (KNOW), where the same woman appears as a peer. **Stands alone:** no "part 2", no
tease; every open loop closes inside this video. Not related to the P1 face from
`runs/2026-11-07-2002-1t-first-line-fixer` (different woman, different age).

## Angle (Avatars doc, quoted exactly)
Strategy §3 pairs P2 with **angle 2 (pillow / one side)**. The doc has two entries numbered "2)"; this
is the second one, identified by its first words "Seeing wrinkles on only one side…" (the other "2)",
"Sudden moment of looking at the mirror…", is the acceptance version for E2 and is NOT used here).

**Angle 2** (first words "Seeing wrinkles on only one side…"):
> "Seeing wrinkles on only one side of your face? Sleeping on one side of the pillow?"

**Use from the angle:** the one-sided pattern as the hook and the reveal (she sleeps on that side);
the pillow as the cause.
**Do NOT use:** "mirror" visuals from the other "2)" entry (no mirror in frame, lessons §4/§8).

## Belief to move and objection
- **Belief (opener, lessons §2, written for the side sleeper):** a lot of her lines are pressed in every
  night while she sleeps, so they're something she can stop. "Some of the lines you see in the morning
  were pressed in overnight." Belief 1 (holding the skin flat and sealed in moisture all night visibly
  smooths lines by morning) may appear as the one "how it works" line in the answer.
- **Objection:** none for this slot. Her "I've tried every cream" is the problem's texture (creams
  don't stop the fold), not an argument we rebut. Fall-off for side sleepers belongs to 2-M (STAY):
  don't answer it here.

## APPROVED CLAIMS — use nothing else (lessons §1–2)
1. **Usage:** apply to clean, dry skin with no serum, lotion or oil underneath; press each piece from the center outward so it lies flat; wear **overnight (6–8 hours)** (never "8 hours"); peel off gently in the morning; **"just clean and reuse"** (never "rinse and dry"); store each piece on its backing film. No needles, no tape, no refills, no actives.
2. **Mechanism / belief 1:** holding the skin flat and sealed in moisture all night **visibly smooths lines by morning**, with nothing going under the skin.
3. **Opener:** a lot of her lines are pressed in every night while she sleeps, so they're something she can stop. ("Some of the lines you see in the morning were pressed in overnight.") Side sleeper: creases on forehead/eyes no longer fade by midday; "It's my pillow, not me."
4. **Approved result words:** "smoother skin by morning", "softens your lines", "stops the creases you press in every night", "wake up looking rested", **"removes wrinkles"** / "removes my forehead lines overnight" (never permanent / forever / for good), **"lifts sagging skin"**. An informed peer or authority-look presenter may explain the mechanism; she may describe her own results in first person. Before/afters allowed (AI ones too, like-for-like).
5. **What it is:** The Wrinkle Smooth Face Set (5 Pieces) by The Daily Glow Co.: clear, thin (~1.5 mm), soft silicone, transparent with a slight frost; 1 forehead patch (14.3 × 6.1 cm, tab pointing DOWN between the brows) + 4 crescents 7.8 × 2.2 cm (2 under the eyes, 2 smile lines, lips uncovered); whole face in one kit; reusable.
6. **Offer (live Shopify, checked today 2026-11-08 per owner/coordinator):** Face Set 1 Set $45 · 2 Sets $60. TOF does not say a price.
7. **Guarantee:** 30-day money-back exists but **stays out of this creative** until the refund page is fixed (lessons §12).

**Claim translation:**
- Her quote's "permanent wrinkles" → never said as a claim either way; the video says the pillow
  "presses lines in every night" and the patch "stops the creases you press in every night" /
  "smoother by morning". Never "permanent / forever / for good" about our result.
- The matrix's "7 hours a night" (strategy §4 video-type wording) is **not an approved fact or
  statistic**: say "all night" / "for hours every night" / "every single night", never a number of
  hours of pillow contact, and never "8 hours". The wear time, if mentioned, is "overnight (6–8 hours)".
- "Science-backed": she values it, but we have no study. Explain the mechanism in plain words (the
  fold, holding skin flat); never "clinically proven", "studies show", "dermatologists say" or any %.

**Off limits:** a stated credential ("I'm a dermatologist", "Dr.", "as an esthetician", name tags, MD
captions), made-up statistics, study results or "X% of women", fake reviews or star ratings,
"permanent/forever/for good", "11s"/"11 lines" (say "frown lines"/"forehead lines"), "8 hours",
"rinse and dry", invented science (no claims about collagen, elastin or sleep-position research).

## On-screen person (new; must fit mid-30s to 40s)
Lessons §7 has nothing usable of this age with an authority look on Higgsfield: the 35-year-old (Black)
and 45-year-old (white) portraits are Runway-only (short IDs, no full IDs); the robe woman 3bcb3615
(40–45, Higgsfield media) reads as a bedtime peer, not an educator; DOCTOR.png/PRESENTER.png are the
owner's files and not uploaded. **New character, locked for all Proactive Problem-Solver videos:**
a **38-year-old woman**, warm medium-brown skin (South Asian or mixed heritage), dark hair pulled fully
back in a low sleek bun (nothing on the forehead), small silver studs, minimal makeup, unretouched skin.
Visible lines: fine lines under the eyes and at the outer corners, two or three horizontal forehead
lines, and a **sleep crease that is clearly deeper on her right side** (right cheek/outer eye, the side
she sleeps on). Authority styling for this video: a fitted cream knit or a crisp white shirt (a white
coat is allowed by lessons §2, but no name tag, logo or credential), seated at a clean, bright desk or
skincare-studio counter with soft window light; she talks to camera like an educator explaining why.
Crease visuals: (a) her right side close-up vs left side; (b) her face on a pillow, cheek folded,
morning lamp-off light; (c) a pillowcase showing its wrinkles. Build as Nano Banana 2 stills from
scratch (prompt-engineer), then save as an Element for 2-M and 2-B (where she appears as a peer at home).

## Product and brand moments: assets that already exist (lessons §7)
- **Branded Face Set box** (owner, Higgsfield, generated Nov 8): job `0f24791e-57ce-49ab-afe4-85d5f8e0d243`,
  file `assets/packaging/face-set-box-v1.png` (studio front 3/4 view on mint). Use it for the box on her
  desk or nightstand early (no comment), and for "what I use" shots.
- **9:16 hero shot** (brand studio look: teal backdrop, orange rim light, mist surface, droplets, empty
  space top and bottom for text): job `39637096-4223-49c3-a881-37feba3e280a`, file
  `assets/packaging/face-set-hero-9x16-v1.png`. Use it for the end card / CTA beat.
- Reuse by passing the job ID in `medias` (no credits). Box text is spelled correctly; the crescents
  in both are plumper than the real ones, so any on-face shot uses the Eye-patches Element
  (`9d766c06-2818-43e8-8ec4-1aac02d63897`) / Forehead-patch Element
  (`6375c707-7ad9-4df9-b7e0-69750993e7aa`) for shape, with the PATCHES block verbatim. GPT Image 2.6 is
  the model for anything with printed text (site logo media `91c93097-1a34-4128-9abb-7b21dacc80fb`).

## Production lessons carried over (from the 1-T runs; not their story)
- Her voice is native Kling 3.0 Pro (≈2.5 credits/s with sound): **every second she is heard is paid
  talking footage, including seconds under cutaways.** Whole-second clips; talking clips one sentence,
  ≤15 words, 4–6 s (`video.talking_clip`).
- Cutaways (crease close-ups, pillow fold, patches on, morning) are **checked Nano Banana stills with
  code motion**, not their own Kling clips.
- Frame one has motion or a pattern break (never a static title); hook text ≤8 words, in code.
- Before/after is like-for-like (same framing, softer, not erased).
- Fast-paced edit spec in `editing` (config); one generation per shot, no variations.

## Must avoid
- A stated credential of any kind (spoken, on screen, caption, name tag)
- Hour counts for pillow contact ("7 hours") or wear ("8 hours"); any statistic or study claim
- Smiling or talking with patches on; a posed silent lying-down "wearing" shot (applying looks organic)
- Mirrors in frame; "11s"/"11 lines"; "rinse and dry"; "permanent/forever/for good"
- Product talk before the last ~20%; banned transitions ("I have something for you", "that's where X comes in", "introducing", "what if I told you")
- Answering the fall-off objection (that's 2-M) or the guarantee (refund page not fixed)
- Black Friday "2nd set $15" or any price in this TOF video
- Any "part 2" / sequel / unclosed loop
- AI-rendered on-screen text (add in code)
- A tips page with no product: product/box in shot, brand name on screen and in the caption
- Copying the "resilia" reference ad's words, face, voice or brand

## Price check
Live Shopify, checked today 2026-11-08 (owner/coordinator): The Wrinkle Smooth Face Set (5 Pieces)
1 Set $45 · 2 Sets $60. The Black Friday "2nd set $15" is **not** in Shopify variant data: don't use
it. Not used in this TOF video anyway.

## Owner instructions for this run (Nov 8, 2026, they override anything above)
1. **Reference:** the top-impression ad from the Meta Ad Library search "resilia" (breakdown in `learning/swipe-file/2026-11-08-resilia-*.md`).
2. **Length: about 45 seconds.**
3. **Voiceover only.** The skeleton character does NOT talk on screen (no lip movement). Narration is one separate voiceover track (ElevenLabs is allowed because the video is voiceover-only). This replaces the talking-head authority presenter: the "authority look" comes from the explainer voice and visuals, not a talking person.
4. **A still image for every sequence** (every shot gets an approved still before any video credits).
5. **Animated shots are prompted "Pixar style"** (lessons §0).
6. **Technical explanation of how silicone patches help the skin**, approved wording only (lessons §1–2):
   - holds the skin flat, so it can't fold and crease against the pillow for hours;
   - seals the surface so less moisture escapes overnight, keeping the top layer hydrated and plump, so lines look smoother by morning;
   - nothing goes under the skin: no needles, no actives, purely physical;
   - "removes wrinkles" (never permanent/forever) and "lifts sagging skin" are approved.
   Not allowed without owner evidence: collagen/elastin, "repairs skin", scar-sheet research, any numbers or studies (incl. "7 hours").
7. **Apply `docs/lessons-learned.md` in full.**
