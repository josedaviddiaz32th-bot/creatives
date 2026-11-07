# Creative strategy: web research notes (Nov 7, 2026)

These notes are raw inputs for `docs/creative-strategy.md`, which gets written
after reviewing the owner's videos. **Source quality:** most material comes from
agency or vendor blogs with something to sell. Only Meta's engineering posts
are primary sources. Treat every number below as a heuristic to test, not a rule.

## Meta Andromeda (ad retrieval)

**Primary sources (Meta):**
- Dec 2024: Andromeda is the retrieval engine behind Advantage+. Retrieval
  narrows tens of millions of candidate ads to a few thousand before ranking.
  https://engineering.fb.com/2024/12/02/production-engineering/meta-andromeda-advantage-automation-next-gen-personalized-ads-retrieval-engine/
- Oct 28, 2026: the next-gen system (what blogs call "Andromeda 2.0") scores
  every eligible ad at over a billion ads per second. Meta reports +2.4%
  Facebook conversions since 2025.
  https://engineering.fb.com/2026/10/28/ml-applications/meta-andromeda-next-gen-ads-retrieval-gpu-co-design/

**Meta statements reported secondhand** ([Apogee](https://www.apogee.ad/en/blog/meta-andromeda/)):
- Apr 2025: creative diversification is now a better lever for reaching the
  right people than niche targeting.
- Dec 2025: ads that look or feel alike count as variations of one creative.
  Meta shows a creative-diversity indicator (high/medium/low) and calls it an
  estimate still in development.
- Meta reporting includes Creative Similarity and "Top Creative Themes".

**Practitioner consensus, not verified by Meta:**
- **Creative is the targeting.** Targeting decides which ads are eligible;
  Andromeda then matches each ad's content to people. The copy, visuals,
  persona, setting and format of an ad signal who it's for.
- **Near-duplicates collapse into one concept.** Changing only the first 3
  seconds, the color or the caption barely counts as a new ad. Blogs say
  similar ads are grouped (an "Entity ID") and only the best in each group
  gets much delivery.
  ([Battlebridge](https://battlebridge.com/blog/meta-andromeda-and-creative-diversity-why-ten-similar-ads-count-as-one/),
  [Adsuploader](https://adsuploader.com/blog/meta-andromeda),
  [Admove](https://www.admove.ai/blog/meta-andromeda-guide))
  Specific thresholds, like "60% similarity", are unverified.
- **How many concepts:** no official number. Blogs say anything from 3–5 to
  8–20 genuinely distinct concepts per campaign or ad set; AdScale saw 4–6
  per ad set work across about 1,200 accounts.
  ([AdScale](https://adscale.com/blog/meta-andromeda-update/))
- **Fatigue:** Meta's help content reportedly says to add a *materially
  different* new concept, not a variation of the tired one.

## Awareness levels × funnel

- Schwartz's five levels (Breakthrough Advertising, 1966): unaware →
  problem-aware → solution-aware → product-aware → most aware.
- Common practitioner mapping: unaware and problem-aware = top of funnel;
  solution-aware = middle; product-aware and most aware = bottom. The funnel
  is how *we* organize campaigns; awareness is what *she* knows. They map
  onto each other but aren't the same thing.
  ([Segwise](https://segwise.ai/blog/advertising-awareness-levels-2026),
  [Motion](https://motionapp.com/blog/five-customer-awareness-stages-advertising),
  [adlibrary](https://adlibrary.com/posts/awareness-stages-facebook-ads))
- Advice: tag every creative by awareness level and hook type, then let the
  results show which level works for which persona.

## Diversity frameworks

- Build a **matrix** of persona × angle (or desire) × format, sometimes
  × awareness ("PDA": persona, desire, awareness) or × offer.
  ([Spark UGC](https://www.sparkugc.com/resources/creative-diversity-persona-angle-format),
  [Tidal](https://tidal.digital/the-4-dimensions-of-creative-diversity/),
  [RoasPig](https://roaspig.com/blog/creative-diversification-strategy/),
  [Karb](https://karb.ai/blog/meta-ads-creative-diversification-2026))
- Example sizes: 5 angles × 3 formats = 15; or 2–3 personas × 3–4 angles ×
  2–3 formats.
- **Test design:** a *format test* keeps the message and changes the format;
  a *message test* keeps the concept and changes the hook or angle. Change
  one variable at a time.
  ([TheOptimizer](https://theoptimizer.io/blog/how-to-test-ad-creatives-on-meta-after-the-andromeda-update-2026-playbook),
  [Soar](https://www.soarwithus.co/blog/how-to-run-creative-testing-on-meta-a-complete-guide))

## Format catalog (DTC, beauty/skincare)

Talking-head UGC testimonial-style · problem → solution · product demo /
how-to · us vs. them / comparison · reasons why (listicle) · unboxing /
first reaction · routine (GRWM, night routine) · street interview /
vox-pop · founder story · green-screen reaction (creator over an article,
Reddit post or review) · split-screen · "things I wish I knew" ·
myth-busting / educational · skit / POV meme · static comparison card ·
carousel.
([Curtis Howland, $100M on Meta](https://curtishowland.substack.com/p/ive-spent-100m-on-meta-ads-in-the),
[Demand Curve](https://gp.demandcurve.com/lessons/ad-creative-formats),
[Taylor Sicard](https://taylorsicard.com/blog/dtc-ad-formats-2026),
[Influee](https://influee.co/blog/tiktok-ad-formats))

## Organic-first testing and metrics

- Post concepts organically, and promote only those that clear hook and
  hold thresholds.
  ([Finch](https://finch.com/blog/how-to-build-ad-creative-testing-roadmaps-that-wins/),
  [Sociallyin](https://sociallyin.com/resources/how-to-test-social-media-creative-for-maximum-performance/))
  The claim that organic results predict paid results is a vendor claim
  with no independent data.
- **Definitions:**
  - Meta: hook rate = 3s views ÷ impressions; hold rate = ThruPlays ÷ 3s views.
  - TikTok: 2s views ÷ impressions; 6s views ÷ 2s views.
  ([Motion](https://motionapp.com/blog/key-creative-performance-metrics),
  [Billo](https://billo.app/creative-insider/data-insights/hook-rate-benchmarks/))
- **Benchmarks conflict**: hook rate 25–30%+ (some say 70%+); beauty
  reported around 30–42%. Build your own baseline from the first week.
- **Diagnosis:** strong hook + collapsing hold = the opening promised
  something the body didn't deliver. That matches the drop-off diagnosis in
  the handoff (lessons section 11).

## Not reachable from this session
segwise.ai blocks fetches here, so its articles are known only from search snippets.
