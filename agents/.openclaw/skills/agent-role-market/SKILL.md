---
name: agent-role-market
description: Tool-agnostic role and workflow selection for multi-agent software work. Use when a task needs explicit roles, handoffs, workflow phases, or verification evidence.
---

# Agent Role Market

Use this skill as a thin adapter over the repository's `roles/` and `workflows/` directories.

## Role Selection

- Pick one primary role.
- Add at most two supporting roles.
- Split the task if more roles are required.
- Keep role selection explicit in the task record.

## Workflow Selection

Use `workflows/` when the task matches a common multi-step pattern, such as requirement clarification, feasibility validation, feature delivery, bugfix regression, security review, release readiness, or incident response.

## Handoff Standard

Every handoff must include:

- Conclusion
- Completed work
- Artifact locations
- Verification evidence
- Risks and open questions
- Recommended next step

## Completion Standard

Conversation alone is not completion. Work is complete only when the expected output and text-based verification evidence are recorded.
