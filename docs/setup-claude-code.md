# Setup — Claude Code

> **Shortcut:** you can skip this page — clone the repo and paste the install prompt from the [README Quickstart](../README.md#quickstart-5-min); Claude Code will do the steps below itself. This page is the manual/reference path.

1. **Install the skill.** Copy the repo's `SKILL.md` into your project as `.claude/skills/miaosuan/SKILL.md` (or `~/.claude/skills/miaosuan/SKILL.md` for all projects). Copy `doctrines/` and `templates/` alongside it:

```
.claude/skills/miaosuan/
├── SKILL.md
├── doctrines/wujing/…
└── templates/…
```

2. **Bootstrap strategy files.** In your workspace: copy `templates/strategy/` to `strategy/` and fill in your fronts/bets once, by hand. (Ten minutes. The harness maintains them afterwards.)

3. **Run manually.** In a session: `/miaosuan` or just ask — *"Run miaosuan over this week: <paste or point at your activity sources>."*

4. **Make it daily (optional).** Use any scheduler you already have (cron + `claude -p`, CI schedule, or your agent platform's cron) to fire once a day:

```
claude -p "Run the miaosuan skill over yesterday's activity. \
Sources: git log since yesterday, TODO.md, notes/inbox.md. \
Post the report to <where you read it>."
```

5. **Answer in one word.** When a decision digest appears, reply with the literal option (`go` / `hold` / …). That's the whole point.
