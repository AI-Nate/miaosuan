# Setup — any other coding agent (Cursor, Codex CLI, aider, …)

miaosuan is plain markdown. Any agent that can (a) read files in your workspace and (b) follow instructions can run it — a dedicated "skills" feature is convenient, not required.

## The one requirement

The agent must have `SKILL.md`, `doctrines/`, and `templates/` readable in its workspace, and your live `strategy/` files writable. That's the whole integration surface.

## Recommended layout

```
your-workspace/
├── miaosuan/            # this repo, cloned as-is
│   ├── SKILL.md
│   ├── doctrines/wujing/…
│   └── templates/…
└── strategy/            # YOUR live files, copied once from miaosuan/templates/strategy/
```

Keep `strategy/` **outside** the cloned repo — it's your private state, not the tool. (The repo's `.gitignore` blocks `strategy/` as a second line of defense, but separation is cleaner.)

## Wiring it up, per agent style

**Agents with an instructions file** (Cursor rules, `AGENTS.md`, `CONVENTIONS.md`, system prompt): add one line —

> When asked to "run miaosuan" / "战略复盘", follow `miaosuan/SKILL.md` exactly, using `miaosuan/doctrines/wujing/` as the active doctrine and `strategy/` as the rolling state.

**Agents without one**: just say it in the session —

> Read `miaosuan/SKILL.md` and run it over this week. Sources: git log, my notes files. Update `strategy/` per the procedure.

## First run

1. Copy `miaosuan/templates/strategy/` → `strategy/` and fill in your fronts and bets once, by hand (~10 min — the harness maintains them afterwards).
2. Run manually once and check the output discipline: every interpretation must end in a 所以应该 action, and stalled decisions must surface as the digest card.

## Daily loop

Use whatever scheduler you have — cron + your agent's headless/CLI mode, a CI schedule, or your platform's built-in cron:

```
<your-agent> "Run miaosuan per miaosuan/SKILL.md. Window = last 24h.
Sources: git log since yesterday, TODO.md, notes/.
Deliver the report to <where you read it>."
```

The harness degrades gracefully: no cron → run it when you remember; no chat channel → write the report to a file. The only thing that doesn't degrade is the discipline — one word from you closes each digest.
