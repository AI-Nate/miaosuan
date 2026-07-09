# Setup — OpenClaw (or similar always-on agent platforms)

Works on any platform where an agent has (a) a persistent workspace, (b) a skills folder, (c) a cron facility.

1. **Install the skill.** Drop the repo into the agent's workspace, e.g. `workspace/skills/miaosuan/` containing `SKILL.md`, `doctrines/`, `templates/`.

2. **Bootstrap strategy files.** Copy `templates/strategy/` → `workspace/strategy/` and fill in your fronts and bets once.

3. **Create the daily cron.** Schedule a daily job (pick a quiet hour) with a prompt like:

```
Run the miaosuan skill. Window = last 24h.
Sources: the channels you can read, git logs, task files.
Deliver: 今日要点 / 兵法解读 / 变更摘要 / 明日一手 to this channel;
if the digest triggers, render it as a single-page card.
```

4. **Point it at real sources.** The review is only as good as its GATHER step. Give the agent read access to where work actually happens (channels, repos, trackers) — not summaries of summaries.

5. **Tips from production use**
   - Keep the strategy files in the agent's *bootstrap* context so every session knows the current bets, not just the review session.
   - Let the review update the files, but require explicit human words for anything touching 红线.md or 主攻.md pivots.
   - Resist making the report longer over time. The discipline is the product.
