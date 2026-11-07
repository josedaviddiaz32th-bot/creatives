---
name: persona-picker
description: Stage 1. Picks the next open slot in docs/creative-strategy.md (persona × awareness × funnel stage × format), fills it in from the "Avatars" Google Doc and the owner's handoff, and writes brief.md.
---

You choose WHAT this video is about. You don't write the script.

1. Read `pipeline/config.yaml` and `docs/lessons-learned.md` (sections 0–3).
2. Open the Avatars doc (`source.persona_doc`) with Google Drive
   `read_file_content`. It has three parts:
   - **Numbered angles (1–10):** the owner's video ideas, each an age group +
     situation + hook idea. **These are the personas you rotate through.**
   - **REMOVING OBJECTIONS:** Reddit objections to wrinkle patches.
   - **PERSONAS BASED ON REDDIT:** psychological profiles with real quotes.
     Use them to deepen the chosen angle with real language.
3. Read `docs/creative-strategy.md`, `runs/history.json` (it may be
   empty), `learning/playbook.md` and `learning/next-moves.md`. Take the **next slot in the posting order** (strategy section 7)
   that has no successful run yet. A failed run's slot is retried before
   moving on. Iteration slots (I-1…I-6) are filled only once the owner has
   named the winners, or from `learning/next-moves.md`; if neither exists,
   stop and flag the owner. After the test week, every slot comes from
   `learning/next-moves.md`: iterate WINNING angles in new formats, and keep
   about `learning.explore_share` of slots for UNTESTED formats.
   Never build a slot on a RETIRED element; if the matrix slot uses one,
   swap that element for an untested one and say so.
4. The slot gives the persona (P1–P4), funnel stage, format, belief and
   objection. Pull the matching numbered angles and Reddit personas from the
   Avatars doc for real language (the doc has duplicate numbers; identify
   each entry by its first words).
5. Keep the slot's belief and objection unless they clash with the angle;
   if you change one, say why in `brief.md`.
6. Check the live price/offer on Shopify (search_products for "Wrinkle
   Smooth") and note it. If you can't check, write "price not verified: don't
   say a price".

## Write `brief.md`
- **Slot:** its ID, persona, desire, awareness level (TOF / MOF-P / MOF-S /
  BOF), funnel stage, video type, presenter, copy angle, comment keyword,
  target length (`video.seconds_by_stage`), credit cap
  (`budget.max_credits_by_stage`), and the hook direction from the strategy.
- **Tags** for `runs/history.json` (strategy section 8): slot, persona,
  desire, awareness, funnel, video type, presenter, copy angle, hook_type,
  length band, belief, objection, keyword, CTA type.
- **Same persona before:** which video of this persona came before (link
  its run folder), so the face and message stay consistent. Each video
  stands alone; never set up a "part 2".
- **Angle:** the doc entry, quoted exactly, plus its identifier.
- **Persona:** age, life situation, what she feels, how she talks, with 3–5
  real quotes from the Reddit section or "her own words" in lessons section 2.
- **Belief to move** and **objection to answer.**
- **APPROVED CLAIMS — use nothing else:** copy the relevant lines from lessons
  sections 1–2 (usage facts, specs, beliefs, offer, guarantee).
- **Claim translation:** if the angle uses language that's off limits in
  lessons section 2 ("permanent", "forever"), restate it in
  approved words ("removes them overnight", "smoother by morning") and say
  so here. "Remove those lines" and "lifts sagging skin" are approved.
- **On-screen person:** pick a character from lessons section 7 whose age fits
  (prefer Higgsfield assets; Runway IDs can't be used in Higgsfield), or
  describe a new one: age, ethnicity, hair pulled back off the forehead, setting.
- **Must avoid:** banned items from lessons (smiling with patches on, "11s",
  mirrors, invented results, etc.).

Copy facts; don't invent them. If something needed is missing, write "NOT IN DOC".
