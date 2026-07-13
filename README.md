# claude-skills

Agent Skills for [Claude Code](https://claude.com/claude-code).

Each skill is a self-contained folder: a `SKILL.md` that Claude loads when the task matches, plus reference files and assets it pulls in only as needed.

## Skills

| Skill | What it does |
|---|---|
| [`artist-grant-writing`](./artist-grant-writing) | Write and pressure-test artist grant applications for Quebec and Canadian funders — Canada Council, CALQ, Conseil des arts de Montréal — with a visual-arts subdivision covering research, production, travel, and exhibiting in Quebec, Canada, and Asia. |

## Install

Clone into your personal skills directory:

```bash
git clone https://github.com/msolav/claude-skills.git ~/.claude/skills-repo
ln -s ~/.claude/skills-repo/artist-grant-writing ~/.claude/skills/artist-grant-writing
```

Or copy a single skill:

```bash
cp -r artist-grant-writing ~/.claude/skills/
```

Skills in `~/.claude/skills/` are available across all projects. For a project-scoped skill, use `.claude/skills/` inside the project instead.

Claude invokes a skill automatically when the task matches its description, or on request (`/artist-grant-writing`).

## A note on accuracy

These skills encode real program rules — deadlines, eligibility, criteria weightings, fee schedules — which **change every year**. Canada Council restructured its entire grant architecture in 2025, and CALQ revises criteria per cycle. Every skill here is built to fetch live guidelines rather than trust its own cached numbers, and reference files carry explicit staleness warnings. Treat them as maps, not as sources of truth.

## Licence

[MIT](./LICENSE)
