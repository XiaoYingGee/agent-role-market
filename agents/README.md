# Tool Adapters

This directory contains optional adapters for common agent tools.

The core package remains tool-agnostic:

- `roles/` defines reusable role packs.
- `workflows/` defines common multi-role task flows.
- `agents/` provides installable or copyable wrappers for specific tools.

## Adapters

| Directory | Target |
|---|---|
| `.claude/` | Claude Code subagent-style setup |
| `.codex/` | Codex project instructions and skill-style setup |
| `.openclaw/` | OpenClaw skill-style setup |

## Rules

- Do not put private workspace paths, account names, bot IDs, tokens, or chat IDs in adapters.
- Keep adapters thin and reference `roles/` and `workflows/` for the source material.
- If an adapter needs tool-specific syntax, isolate it under that adapter directory.
- Do not let adapter behavior override role handoff, evidence, or completion rules.

## Suggested Use

Copy the adapter directory that matches your tool into the location expected by that tool, then edit only local settings such as model choice or tool permissions.
