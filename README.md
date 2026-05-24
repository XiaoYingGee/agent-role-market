# Agent Role Market

Agent Role Market is a tool-agnostic collection of reusable role packs for AI agent workflows.

It is designed for teams that want stable, explicit, and auditable agent behavior without coupling their workflow to a specific agent runtime, chat platform, or vendor format.

## What This Repository Provides

- Role packs for common software work.
- Workflow templates for common multi-role task patterns.
- Clear activation boundaries: when to use a role and when not to use it.
- Input and output contracts for each role.
- Review checklists and handoff expectations.
- A neutral Markdown format that can be adapted to any agent runtime or workflow system.

## What This Repository Does Not Provide

- No tool-specific configuration.
- No private team process or identity files.
- No chat-platform-specific IDs, mentions, channels, or workspace paths.
- No direct copy of third-party role prompts.
- No guarantee that every role should be loaded at once.

The intended use is selective: choose a small number of role packs per task, adapt them to your local workflow, and keep the task's source of truth in your own project system.

## Design Principles

1. **Tool agnostic**: role packs describe capabilities and outputs, not vendor-specific commands.
2. **Role first**: roles are grouped by work type, not by personality.
3. **Small surface area**: each role has a narrow responsibility and clear non-goals.
4. **Explicit contracts**: every role defines required inputs, expected outputs, and handoff requirements.
5. **Composable but bounded**: use one to three role packs for a task; split the task if it needs more.
6. **Evidence-based completion**: a task is not done until outputs and verification evidence are recorded.

## Repository Layout

```text
agent-role-market/
  roles/
    01-discovery-planning/
    02-design-product/
    03-engineering/
    04-quality-security/
    05-operations/
    06-orchestration/
  templates/
    role-pack-template.md
  workflows/
    requirement-clarification.md
    feasibility-validation.md
    standard-feature-delivery.md
    bugfix-regression.md
    security-review.md
    release-readiness.md
    incident-response.md
  agents/
    .claude/
    .codex/
    .openclaw/
```

## Quick Start

See [setup/](setup/) for deployment guides. Currently supported:

- [Claude Code](setup/claude-code.md) — symlink or copy agents into `~/.claude/agents/`

## Tool Adapters

The `agents/` directory contains optional adapter packages for common agent tools.

| Adapter | Purpose |
|---|---|
| `agents/.claude/` | Claude Code-style subagent definitions |
| `agents/.codex/` | Codex-style project instructions and skill package |
| `agents/.openclaw/` | OpenClaw-style skill package |

Adapters are intentionally thin. They point back to `roles/` and `workflows/` instead of redefining a separate private process.

## Role Groups

| Role group | Use For |
|---|---|
| `01-discovery-planning` | Requirements, planning, prioritization, documentation |
| `02-design-product` | Product flows, UX, UI structure, accessibility review |
| `03-engineering` | Backend, frontend, API, database, implementation planning |
| `04-quality-security` | QA, test automation, review, security assessment |
| `05-operations` | Incident response, release readiness, operational reliability, DevOps, performance work |
| `06-orchestration` | Task coordination, multi-agent distribution, context control, handoff governance |

## How To Use

1. Pick the role group matching the task.
2. Select one primary role pack.
3. Add at most two supporting role packs when needed.
4. Copy the relevant role pack content into your local agent tool, skill, instruction file, or task prompt.
5. Bind it to your own task board, issue tracker, or handoff format.

Example:

```text
Task: design and implement a new API-backed settings page

Primary role: roles/03-engineering/api-designer.md
Supporting roles:
  - roles/02-design-product/ux-flow-designer.md
  - roles/04-quality-security/qa-engineer.md
```

## Workflow Templates

Use workflows when a task needs multiple roles or phases.

| Workflow | Use For |
|---|---|
| [requirement-clarification](workflows/requirement-clarification.md) | Turning vague asks into scoped work |
| [feasibility-validation](workflows/feasibility-validation.md) | Testing feasibility before full build |
| [standard-feature-delivery](workflows/standard-feature-delivery.md) | Product/design/engineering/QA feature delivery |
| [bugfix-regression](workflows/bugfix-regression.md) | Reproducing, fixing, and preventing regressions |
| [security-review](workflows/security-review.md) | Reviewing security-sensitive changes |
| [release-readiness](workflows/release-readiness.md) | Preparing and verifying a release |
| [incident-response](workflows/incident-response.md) | Handling production or critical workflow incidents |

## Suggested Task Card

```markdown
Task ID:
Role group:
Primary role:
Supporting roles:
Goal:
Non-goals:
Inputs:
Allowed scope:
Expected outputs:
Verification evidence:
Handoff location:
Open questions:
```

## References And Inspiration

This repository is inspired by public agent role and subagent collections, especially:

- [wshobson/agents](https://github.com/wshobson/agents) for plugin-style organization, role boundaries, and progressive loading ideas.
- [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) for broad subagent categorization and role discovery patterns.
- [contains-studio/agents](https://github.com/contains-studio/agents) for product, design, engineering, and operations role organization.
- [Piebald-AI/claude-code-system-prompts](https://github.com/Piebald-AI/claude-code-system-prompts) for studying how agent prompts are structured and separated by responsibility.

The role packs in this repository are original, condensed, tool-agnostic templates. They are not copied from those projects.

## License

MIT. See [LICENSE](LICENSE).
