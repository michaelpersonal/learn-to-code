# learn-to-code

A Socratic coding mentor skill for Claude Code and Codex.

The output is not code. The output is a learner who can design, test, debug, and explain the code.

## What it does

- Routes each session into the right teaching mode: new project, stuck on code, weak concept, code review, or course readiness
- Never gives the full answer — reveals only the next useful piece
- Calibrates to the learner's actual level from what they say, not what they claim
- Tracks a learning map across sessions so it can refer back to past struggles
- Bridges out when the learner is ready: "You're ready for Total TypeScript — you don't need me for this anymore"

## Install

### Claude Code

Copy `claude/SKILL.md` and `claude/LEARNING-MAP.md` into your skills directory:

```bash
mkdir -p ~/.claude/skills/learn-to-code
curl -o ~/.claude/skills/learn-to-code/SKILL.md \
  https://raw.githubusercontent.com/michaelpersonal/learn-to-code/main/claude/SKILL.md
curl -o ~/.claude/skills/learn-to-code/LEARNING-MAP.md \
  https://raw.githubusercontent.com/michaelpersonal/learn-to-code/main/claude/LEARNING-MAP.md
```

Then invoke it with `/learn-to-code` in any Claude Code session.

### Codex

Copy `codex/SKILL.md` into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills/learn-to-code
curl -o ~/.codex/skills/learn-to-code/SKILL.md \
  https://raw.githubusercontent.com/michaelpersonal/learn-to-code/main/codex/SKILL.md
```

The Codex version overrides Codex's default file-editing behavior while the skill is active — it will ask questions instead of implementing.

## How a session works

Start with what you can already build and what you want to build next. The skill picks the right branch, proposes the smallest real project, and starts grilling immediately.

At the end of each session it writes a `LEARNING-MAP.md` into your working directory. Next session it picks up from where you stopped.

## Inspired by

[Matt Pocock's skills](https://github.com/mattpocock/skills) — concise, branch-driven, operationally precise.
