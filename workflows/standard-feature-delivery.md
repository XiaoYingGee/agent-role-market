# Standard Feature Delivery Workflow

## Use When

- A feature needs product, design, engineering, and QA coordination.
- The work is larger than a small bugfix.
- Multiple artifacts must be handed between roles.

## Roles

- Coordinator: `task-coordinator`, optional `multi-agent-coordinator` for cross-tool or multi-session work
- Product: `product-manager`
- Design: `ux-flow-designer`, `ui-designer`, optional `accessibility-reviewer`
- Engineering: `api-designer`, `backend-architect`, `frontend-developer`, optional `database-architect`
- Quality: `qa-engineer`, `test-automator`, `code-reviewer`
- Operations: optional `devops-engineer` when deployment automation or CI/CD changes are in scope

## Phases

### 1. Intake

Create the task card and decide whether clarification is needed.

Output: task card.

### 2. Spec

Define goals, non-goals, user flow, and acceptance criteria.

Output: product spec.

### 3. Design

Define UX flow, UI states, component structure, accessibility requirements, and API needs.

Output: text design spec and state matrix.

### 4. Build

Implement backend and frontend work using explicit contracts.

Output: code changes and implementation handoff.

### 5. Review

Run tests, review code, and assess risks.

Output: QA result and review findings.

### 6. Release

Decide go/no-go, record release notes, and verify after release.

Output: release handoff.

### 7. Retro

Record important decisions, follow-ups, and lessons.

Output: retro notes.

## Required Handoff

- Product spec
- Design/state spec
- API or data contract
- Implementation summary
- Test and review evidence
- Release decision

## Completion Criteria

The feature is complete when it satisfies acceptance criteria and has recorded verification evidence.
