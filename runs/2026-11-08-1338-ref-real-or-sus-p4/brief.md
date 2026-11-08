# Brief: run 2026-11-08-1338, owner-picked remake "REAL or SUS?" expert stitch (P4, The "Botox-Resistant Pragmatist")

Stage 1 (persona-picker), trial mode. Owner: "Do this one for P4". Sources read today (2026-11-08):
`learning/owner-feedback.md` (all), `docs/lessons-learned.md` (all; §0 first, §1–2 claims), `CLAUDE.md`,
`pipeline/config.yaml`, `docs/creative-strategy.md`, `learning/production-log.md`, `runs/history.json`
(1-T, 2-T and the problem-vs-solution trend remake done; no P4 video yet), the previous brief
`runs/2026-11-08-0909-ref-problem-vs-solution/brief.md` (layout), and the Avatars Google Doc
(`1ySwoyCBQVAL59c04-La1qvvPs1qI766vbqMqYzMZJ0w`, read live with Drive `read_file_content`, checked against
the plain-text export from `download_file_content`). `read_file_content` escapes "!" as "\!"; the escape is
removed here. This persona's section has no emojis.

**Creative reference (fixed by the owner):** a 30.62 s "REAL or SUS?" stitch / green-screen reaction by an
expert-looking creator (a real, named surgeon: we never imitate him or any real person). Local file:
`/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/ref2/ref.mp4`.
Frame sheet: `learning/swipe-file/refs/2026-11-08-real-or-sus-stitch-sheet.jpg`. Breakdown and mapping:
`format.md`.

## Persona (verbatim from the Avatars doc, section "PERSONAS/AVATARS BASED ON REDDIT")

> **The "Botox-Resistant Pragmatist"**
>
> This persona is often in their late 30s to 50s, actively seeking effective wrinkle treatments but explicitly avoiding Botox or fillers, sometimes due to health reasons, philosophical objections, or a desire for more "natural" results. They are pragmatic, looking for proven alternatives and willing to commit to consistent routines or less invasive procedures.
>
> Key concern: Finding non-injectable solutions for wrinkles, particularly on the forehead, that offer noticeable improvement. "I am a 35 YO F and I'm looking to get some kind of treatment to help improve skin texture but, most importantly, the wrinkles on my forehead. I don't want to use Botox or filler."
>
> Behavior: Researching retinoids (like tazarotene), microneedling, peels, red light therapy, and even wrinkle patches, often sharing their experiences with these alternatives. "What treatments have you don't that have been absolutely worth the money? I'm looking into micro needling, but from what I can see online it is kind of a mixed bag whether or not people find it worth it."
>
> Emotional trigger: A desire to address wrinkles without resorting to injectables, often driven by personal values or health considerations. "I'm not interested in Botox (no judgment, it's just not for me). So, I'm wondering what other products have worked for you."

(Complete section: heading, description paragraph, key concern, behavior, emotional trigger, every quote.
Nothing trimmed. "you don't" is her typo, kept.)

### Picker's notes on her (separate from the verbatim section)
- **Why she fits this reference:** the reference caption, "people assume I've had Botox & fillers but I'm
  just wearing [patches]", is her exact position: she wants a result people could mistake for Botox, without
  Botox. Her key concern is "particularly on the forehead", and the reference's proof is a forehead patch.
  She researches alternatives and finds "mixed bag" claims online, so a neutral expert's "real or sus?"
  verdict is the help-me-choose moment she is looking for.
- **Age / situation:** 46, American, works full time, lives in a suburban US house. Bare-faced at night. She
  has moderate forehead lines and the start of frown lines. She has read about microneedling, retinoids and
  red light, and has seen wrinkle patches on TikTok but doubts the before/afters.
- **What she feels:** pragmatic, a little skeptical, no drama. "No judgment, it's just not for me."
- **Real quotes to draw from:**
  - "I don't want to use Botox or filler." (Avatars doc)
  - "it is kind of a mixed bag whether or not people find it worth it" (Avatars doc)
  - "I'm not interested in Botox (no judgment, it's just not for me)." (Avatars doc)
  - "I'm trying everything I can before botox because the price, and I'm terrified" (lessons §2)
  - "This ad… can't be real" (lessons §2, her verdict on over-edited before/afters: the exact doubt
    "REAL or SUS?" plays on)

## Slot
- **Slot ID:** `REF-RoS` (owner-picked remake, trial mode). It fills **P4 × MOF**, the persona and stage of
  matrix slot 4-M, in a different format. It does **not** use up 4-M's "us vs them under the eyes" type or
  its keyword EYES.
- **Persona:** P4 = The "Botox-Resistant Pragmatist" (Avatars doc)
- **Desire:** safety / comfort (a result without needles)
- **Awareness: MOF (solution-aware).** Why: the video names the category in frame one ("Wrinkle smoothing
  patches"), so it speaks to someone who already knows patches exist and doubts them. Its whole job is
  "help me choose": is this real, how does it work, why this kit over tape or one-size patches. That is
  strategy §2's MOF job (why overnight patches, why *this* kit, how it works, a demo/before-after) and its
  MOF hook rule ("about choosing… doubting patches").
- **Funnel stage:** MOF ("help me choose"). The product is the subject from frame one.
- **Video type:** "REAL or SUS?" stitch / green-screen expert reaction. Original UGC clip (a P4 woman
  applying at night and peeling in the morning) with an expert-looking presenter reacting in the corner,
  then a full-screen product beat, then green-screen explanation and a verdict.
- **Presenter:** authority look (original, unnamed character; doctor look allowed; **no stated
  credential**) + a silent peer in the UGC clip.
- **Copy angle:** evidence (live demo + mechanism + verdict)
- **Comment keyword:** **REAL** (unique: PHOTO, PILLOW and SLEEP are used; the matrix reserves FIRST, TIRED,
  SEEN, LOVE, ROUTINE, STAY, MYTH, EYES, NEEDLE, KNOW, WORTH, GENTLE).
- **Target length: ≈30.6 s (owner: same length as the reference).** Inside the MOF band (25–45 s).
- **Credit cap: TBD by the owner** (main session asked). Config would give MOF 120, but the owner's Nov 8 rule
  ("135 is for a 45 seconds video, this is a short video, no more than 50") points lower. **Plan for ≤85;
  a ≤50 variant with named cuts is in `story.md`.** One pool for all versions. **No credits spent at this
  stage.**
- **Hook direction:** the reference's own: on-screen question "REAL or SUS? Wrinkle smoothing patches"
  over motion in frame one (she holds the clear patch up to the lens). It is a question, so it meets
  lessons §0.
- **Product timing:** the patch is in frame from 0 s; the brand name and real box arrive at ≈12 s.

## Tags for runs/history.json
| Tag | Value |
|---|---|
| slot | REF-RoS (owner remake) |
| persona | P4 (The "Botox-Resistant Pragmatist") |
| desire | safety / comfort |
| awareness | MOF (solution-aware) |
| funnel | mof |
| video type | "REAL or SUS?" stitch / green-screen expert reaction over UGC apply + peel |
| presenter | authority look (no credential) + silent peer |
| copy angle | evidence |
| hook_type | skeptic question ("REAL or SUS?") + live demo |
| length band | ≈30.6 s (owner: reference length) |
| belief | 1 (holding skin flat + sealing moisture smooths lines by morning, nothing under the skin); belief 2 touched in the choosing beat (owner-directed) |
| objection | "is this TikTok hype, the before/afters look fake" |
| keyword | REAL |
| CTA type | keyword on the end card + caption |
| swipe_source | 2026-11-08-real-or-sus-stitch |

## Same persona before
None. This is P4's first video, so her face here becomes P4's recurring face (4-T, 4-M, 4-B). **It stands
alone:** no "part 2". Suggested identity: reuse Higgsfield media `3bcb3615` ("woman of about 40–45 in a
robe", lessons §7) as the cast reference, if the prompt-engineer finds it fits; otherwise a new 46-year-old
(below).

## Angle (Avatars doc, quoted exactly)
Strategy §3 pairs P4 with angles 4 and 6.

**Angle 4** (first words "In your 40s? Paper thin…"):
> "In your 40s? Paper thin under eyes?"

**Angle 6** (first words "50s struggling with dry skin…"):
> "50s struggling with dry skin and wrinkles? Tried all kinds of nighttime moisturizers? The questions is always should i get botox?"

**Used:** angle 6's "should I get Botox?" is the tension the reference caption plays on ("people assume
I've had Botox"). Angle 4 (under-eyes) is not the focus; the forehead is (her key concern). The kit's
under-eye and smile-line pieces show in the box/flat-lay pop-up and the choosing line.

**Objection from the doc's REMOVING OBJECTIONS section that this video must not trigger:** "If you think
pulling your skin like this to take them off wouldn't destroy your elastin you're delulu." The peel must
look gentle (lessons §6 fold-back, close to the skin), never stretching the skin.

## Belief to move and objection
- **Belief 1 (lessons §2, north star):** holding the skin flat and sealed in moisture all night visibly
  smooths lines by morning, with nothing going under the skin.
- **Objection:** "is this TikTok hype, the before/afters look fake" (lessons §2 list). The format answers it
  head-on: a neutral expert asks the viewer's question and gives the verdict.

## APPROVED CLAIMS: use nothing else (lessons §1–2)
1. **Mechanism:** holding the skin flat and sealed in moisture all night **visibly smooths lines by
   morning**, with **nothing going under the skin**. "No needles."
2. **Results wording:** "smoother skin by morning", "softens your lines", "wake up looking rested",
   "removes wrinkles" / "wrinkles gone" (never "permanent", "forever", "for good"). The persona may describe
   her own results in first person.
3. **Belief 2:** patches she tried failed because they **fell off or weren't shaped for each area**; this kit
   covers the whole face (fall-off is the category's #1 complaint).
4. **What it is:** clear, thin, soft silicone; 5 pieces: 1 forehead band (tab DOWN between the brows),
   4 crescents (2 under the eyes, 2 on the smile lines). Never opaque or white.
5. **Usage:** clean, dry skin, nothing underneath; press from the center outward; wear **overnight**; peel
   off gently in the morning; **"just clean and reuse"**; store on the backing film. No needles, no tape, no
   refills, no actives.
6. **Name:** "The Wrinkle Smooth Face Set" by The Daily Glow Co. "Frown lines" / "forehead lines", never
   "11s".
7. **Offer (verified live in Shopify today, 2026-11-08):** Face Set: 1 Set (5 Pieces) **$45**, 2 Sets
   **$60**. (Not used on screen in this video; MOF.)
8. **Authority look allowed;** **no stated credential** (no "Dr.", no "dermatologist", no MD tag), no made-up
   statistics, no fake reviews.

## Claim translation (the reference's lines → our approved words)
| Reference says | Problem | Ours |
|---|---|---|
| "They splint those wrinkles smoother" | "splint" not in our approved words | "They hold your skin flat all night, so it can't fold and crease." |
| "they teach your muscles not to create those lines" | **Not approved** (a muscle/lasting claim) | Dropped. Replaced with "seal in moisture, so lines look smoother by morning" + "No needles." |
| "You can get a similar result using [competitor], or Scotch tape" | Names a competitor; sends her elsewhere | "Tape and one-size patches can fall off. This kit is shaped for each area." (belief 2 wording; no brand named; v2 per story-review) |
| "They're called [competitor product]" | Competitor name | "It's the Wrinkle Smooth Face Set." |
| "I bet these results are real, not sus" | Copying a creator's exact line | "My verdict? Real. Not sus." (format phrase kept; his sentence not copied) |

## Owner instructions for this run
- **Same length (~30.6 s), same structure and on-screen text pattern:** "REAL or SUS?" title; a bottom
  caption over the UGC part; "REAL! Not SUS" at the end. Adapted to The Wrinkle Smooth Face Set by The Daily
  Glow Co. **Never "Wrinkles Schminkles", never a competitor's name** ("tape" / "cheap patches" generically).
- **All video** (live-footage format): no stills with zoom or shake. Stills only as start/end frames.
- **US setting:** American bedroom, US clinic-style office, American English.
- **No real person's likeness:** the expert is an original, unnamed character who must not resemble the
  reference creator (different age, ethnicity, hair, wardrobe).
- **Reactions natural** (a genuine impressed look, not a cartoon gasp). **Nothing injury-like** (no red
  marks after peeling).
- **Product box:** the real asset only (`assets/packaging/face-set-box-v1.png`, Higgsfield
  `0f24791e-57ce-49ab-afe4-85d5f8e0d243`), composited as a pop-up in code; **never generated** in a clip.
- **Lip sync is our weak spot (Kling 3.0):** every spoken clip ≤15 words, 4–6 s (config `talking_clip`),
  short sentences, expert in the lower-half or corner framing where possible.
- **Credit cap TBD by the owner;** plan ≤85, show the ≤50 cut list.

## On-screen people
- **UGC woman (P4):** 46, American, light-olive skin, dark-brown shoulder-length hair pulled fully back off
  the forehead (claw clip at night, low bun in the morning), small gold studs, a sage cotton tank top.
  Moderate horizontal forehead lines and faint frown lines at rest. Bare-faced, matte skin. Or Higgsfield
  media `3bcb3615` if it fits.
- **Expert (original):** a man of about 55, white, short silver hair, trimmed grey beard, thin dark-rimmed
  glasses, white coat over a light-blue button shirt, **no name tag, no badge, no embroidery**. Warm, dry,
  matter-of-fact. (Deliberately unlike the reference creator.) Option for the owner: reuse the owner's
  DOCTOR.png presenter (lessons §7) if they prefer.

## Must avoid
- Smiling with patches on; talking with patches on (she never talks); mirrors; "11s"; "8 hours"; "rinse
  and dry"; "permanent / forever / for good"; "teaches your muscles"; statistics; fake reviews; "Dr." or any
  credential; a name tag; any competitor's name or packaging; a generated box; red skin after the peel; a
  skin-stretching peel; overacted reactions; stills standing in for live action; the forehead tab pointing up.

## v2 revision (2026-11-08, story-review REVISE)
Bottom caption is now "When people ask if I've had Botox but I just sleep in my Wrinkle Smooth patches" ("& fillers" implied volume; "assume" implied Botox-equivalence). Choosing line is now "Tape and one-size patches can fall off. This kit is shaped for each area." Bottom caption, box pop-up and CTA line sit above the bottom 35% of the frame.
