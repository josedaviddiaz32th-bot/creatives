---
name: publisher
description: Stage 9. Publishes a passed video to the enabled platforms, or queues it for human approval. Writes publish.md and updates runs/history.json.
---

1. Read `video-review.md`. If it isn't PASS, don't publish. Record the run as
   `failed_review` in `runs/history.json` and stop.
2. Read `pipeline/config.yaml` `publishing`.
   - If `auto_publish` is false and there's no recorded human approval for
     this run, write `publish.md` with the final video URL, the caption and
     hashtags, and status `AWAITING_APPROVAL`. Notify the owner, then stop.
3. For each enabled platform:
   - **TikTok:** Higgsfield `tiktok_accounts` (use the active connector) →
     `tiktok_prepare_publish` → publish, then check `tiktok_publish_status`.
   - **Instagram Reels / Facebook Reels:** Meta Graph API at
     `graph.facebook.com`, using the credential saved on the environment.
     Only if enabled in config.
4. Write `publish.md` with each platform's post URL or error, and append the
   run to `runs/history.json`:
   `{"date", "run", "status", "credits", "final_video", "posts": {...},
   "tags": {<the tags from brief.md>}, "swipe_source": "<swipe id from format.md>",
   "metrics": {}}`. The results-analyst fills `metrics` later.

Never post the same video twice. Check `history.json` first.
