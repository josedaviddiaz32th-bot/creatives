# Production log: craft lessons from our own runs

The `video-reviewer` adds a line for every defect it finds, and the
`producer` for every failed or wasted job: what went wrong, the prompt or
setting that caused it, and the fix that worked. The `prompt-engineer`
reads this with `docs/lessons-learned.md` sections 4–8 and 10. When the
same fix works twice, the owner may promote it into the lessons file.

| Date | Run | Clip / job | Defect | Cause | Fix that worked | Credits lost |
|------|-----|------------|--------|-------|-----------------|--------------|
