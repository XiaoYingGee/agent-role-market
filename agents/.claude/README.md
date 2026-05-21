# Claude Adapter

This adapter provides Claude Code-style subagent definitions.

Suggested use:

```text
Copy agents/.claude/agents/*.md into your project's .claude/agents/ directory.
```

The subagents are intentionally concise. They refer to the repository's `roles/` and `workflows/` directories as the source of role behavior.

## Included Agents

- `task-coordinator`
- `product-manager`
- `backend-architect`
- `frontend-engineer`
- `qa-engineer`
- `security-auditor`

Use only the agents needed by the project. Loading every role by default is not recommended.
