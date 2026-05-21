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
- `frontend-developer`
- `qa-engineer`
- `security-auditor`
- `error-detective`
- `performance-engineer`
- `devops-engineer`
- `multi-agent-coordinator`
- `task-distributor`

Use only the agents needed by the project. Loading every role by default is not recommended.
