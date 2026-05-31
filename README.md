# Ogün

I am building open-source tooling for AI coding agents, OSS maintainers, and safer Codex/MCP workflows.

## Current Focus

### [trace-to-skill](https://github.com/grnbtqdbyx-create/trace-to-skill)

Check whether a repository is Codex-ready, then turn failed Codex, Claude Code, Cursor, Copilot, and MCP-enabled agent runs into reusable `AGENTS.md` rules, `SKILL.md` files, and eval evidence.

The core loop:

```text
repo doctor -> failed agent run -> failure class -> reusable rule/skill -> eval gate -> keep/revise/reject
```

Built for maintainers who want AI agents to reduce review load without creating unverified noise.

Try it:

```bash
npx github:grnbtqdbyx-create/trace-to-skill doctor .
```

## Areas I Care About

- Codex and open-source maintainer workflows
- Agent trace analysis and evals
- `AGENTS.md` / `CLAUDE.md` instruction quality
- MCP security and capability boundaries
- Evidence-backed AI-assisted PR review

## Public Work

- [trace-to-skill](https://github.com/grnbtqdbyx-create/trace-to-skill): Codex readiness scoring, agent failure analysis, PR comments, MCP scoring, instruction drift detection, and before/after eval comparison.
