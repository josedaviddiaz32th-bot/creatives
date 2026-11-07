# creatives

An automated UGC video ad pipeline for The Daily Glow Co. It runs 3 times a day:

**persona doc → script → storyboard → Higgsfield prompts → generation (capped at 100 credits) → review → publish (TikTok, then Instagram/Facebook)**

- `pipeline/config.yaml`: every setting (budget, length, schedule, platforms)
- `.claude/agents/`: one file per agent, each with its instructions
- `CLAUDE.md`: how the stages fit together, plus the hard rules
- `runs/`: one folder per run with every intermediate file; `history.json` is the log
