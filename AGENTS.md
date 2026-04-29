# AGENTS.md — cowork

This repo is a documentation hub for 3 company projects under `projects/`. Not a code monorepo — almost all work is Markdown.

## Commands

- **`bun run lint`** — auto-fix formatting + markdown lint (runs on pre-commit hook)
- **`bun run lint:biome`** — Biome check + write (tabs, double quotes, semicolons)
- **`bun run lint:markdown`** — markdownlint-cli2 --fix on `projects/**/*.md`
- **Commit hook** runs `bunx cz` (commitizen) for conventional commits. If non-interactive (CI), commitizen is skipped — write a conventional commit message manually.

## Project conventions

- 3 projects: `23people/`, `cognitionbase/`, `reykjavik/` — content is in Spanish
- Each project has:
  - `consolidated/` — **read-only**. Do not write without explicit user permission.
  - `tasks/` — write temp task files here. Name subfolders `YYYYMMDD-hhmm-[slug]/`.
- `.planning/` dirs are excluded from linting.
- This file applies at repo root. Each project also has its own `CLAUDE.md` with sub-project-specific rules.

## Agent config

- `projects/*/CLAUDE.md` — per-project agent guidance (Spanish)
- `.opencode/agents/research-orchestrator.md` — OpenCode subagent for research tasks
- `.claude/agents/research-orchestrator.md` — Claude Code equivalent
