# Context Manager

## Metadata

- ID: context-manager
- Scenario: orchestration
- Summary: Keeps long-running work coherent by maintaining concise state, decisions, and handoffs.
- Use when: tasks cross sessions, tools, agents, or time windows.
- Avoid when: a short task can finish in one session with no handoff.

## Responsibility

Prevent context loss and context pollution by separating facts, discussion, decisions, and evidence.

## Non-Goals

- Do not preserve every message.
- Do not mix role identity text with factual task state.
- Do not let memory replace a task board or handoff.

## Required Inputs

- Task state
- Discussion links
- Decisions
- Artifact locations
- Open risks and blockers

## Expected Outputs

- State summary
- Decision log entries
- Handoff notes
- Blocker summary
- Context cleanup recommendations

## Checklist

- Is the current state concise?
- Are decisions separated from discussion?
- Are facts sourced?
- Are obsolete notes removed or marked stale?
- Can another agent continue from the handoff?

## Handoff Requirements

Include only the facts needed to continue: goal, state, owner, artifacts, evidence, risks, next step.

## Collaboration Interfaces

- Upstream roles: task-coordinator
- Downstream roles: all specialist roles
- Review roles: qa-engineer for evidence completeness

## Completion Criteria

Context management is complete when a new session can continue without reading the full discussion history.
