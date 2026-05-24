# Claude Code Setup

Deploy agent-role-market roles as Claude Code subagents.

## Prerequisites

- Claude Code installed (`npm install -g @anthropic-ai/claude-code`)
- `~/.claude/` directory exists (created on first run)
- Git

## Quick start

### 1. Clone the repository

```bash
git clone https://github.com/XiaoYingGee/agent-role-market.git ~/agent-role-market
```

### 2. Install agents

**Option A — Symlink the entire directory (recommended)**

```bash
# Back up existing agents if any
[ -d ~/.claude/agents ] && mv ~/.claude/agents ~/.claude/agents.bak

# Symlink
ln -s ~/agent-role-market/agents/.claude/agents ~/.claude/agents
```

All agents are available immediately. Updates to the repo are reflected without reinstalling.

**Option B — Copy selected agents only**

```bash
mkdir -p ~/.claude/agents
cp ~/agent-role-market/agents/.claude/agents/task-coordinator.md ~/.claude/agents/
cp ~/agent-role-market/agents/.claude/agents/backend-architect.md ~/.claude/agents/
cp ~/agent-role-market/agents/.claude/agents/qa-engineer.md ~/.claude/agents/
```

Pick only what you need. You must re-copy after updates.

**Option C — Symlink selected agents**

```bash
mkdir -p ~/.claude/agents
ln -s ~/agent-role-market/agents/.claude/agents/task-coordinator.md ~/.claude/agents/
ln -s ~/agent-role-market/agents/.claude/agents/qa-engineer.md ~/.claude/agents/
```

Best of both: selective and auto-updating.

### 3. Verify

```bash
ls -la ~/.claude/agents/
claude -p "list available agents"
```

## Available agents

| Agent | Role group | Use for |
|-------|-----------|---------|
| task-coordinator | orchestration | Multi-role task scoping, assignment, and handoff |
| task-distributor | orchestration | Parallel task splitting and fan-out |
| multi-agent-coordinator | orchestration | Cross-session and cross-tool agent coordination |
| product-manager | planning | Requirements, scope, and acceptance criteria |
| backend-architect | engineering | Service design, data flow, reliability planning |
| frontend-developer | engineering | UI implementation, component structure, state |
| qa-engineer | quality | Test strategy, coverage, regression checks |
| security-auditor | quality | Security review, vulnerability assessment |
| error-detective | quality | Bug root-cause analysis and reproduction |
| devops-engineer | operations | CI/CD, deployment, infrastructure automation |
| performance-engineer | operations | Profiling, optimization, load testing |

## Role packs and workflows

Agents reference role packs from `roles/` and workflow templates from `workflows/` in this repository. For agents to resolve these references, the repo must be accessible from the working directory, or you can set `additionalDirectories` in `~/.claude/settings.json`:

```json
{
  "permissions": {
    "additionalDirectories": ["~/agent-role-market"]
  }
}
```

## Coexistence with personal agents

If you have personal agent definitions (project-specific roles, custom agents with device-specific rules), you can:

1. **Merge**: symlink the repo agents alongside your personal ones in `~/.claude/agents/`
2. **Override**: create a same-named file in `~/.claude/agents/` that imports the base role and adds personal constraints
3. **Separate**: keep repo agents in a subdirectory and personal agents at the top level

## Device and environment information

This repository intentionally contains **no device-specific information** (paths, credentials, SSH aliases, environment variables).

For device setup, OS configuration, and environment details, refer to your personal knowledge repository. If you use [knowledge-for-everything](https://github.com/XiaoYingGee/knowledge-for-everything):

- `devices/` — per-device environment info (VM, Mac, Windows)
- `devices/standards.md` — cross-device conventions
- `setup/claude-code.md` — Claude Code installation and configuration (API keys, hooks, MCP servers)

## Uninstall

```bash
rm ~/.claude/agents.bak  # if you backed up
rm -rf ~/.claude/agents   # if symlinked
# or remove individual files if you copied selectively
```

## Windows notes

On Windows, symlinks require either:
- Developer Mode enabled, or
- An elevated (Administrator) terminal

Alternatively, use **Option B** (copy) which works without special permissions.
