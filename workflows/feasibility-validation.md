# Feasibility Validation Workflow

## Use When

- Feasibility is uncertain.
- A technical approach needs validation before full implementation.
- Cost, performance, integration, or developer effort is unknown.

## Roles

- Primary: `backend-architect` or `frontend-engineer`, depending on the unknown
- Supporting: `api-designer`, `database-architect`, `reliability-engineer`, or `qa-engineer`
- Coordinator: `task-coordinator`

## Phases

### 1. Hypothesis

Write what the experiment is trying to prove or disprove.

Output: hypothesis and success criteria.

### 2. Constraints

Define time box, allowed scope, non-goals, and throwaway vs reusable expectations.

Output: validation boundary.

### 3. Build Minimal Proof

Implement the smallest artifact that tests the hypothesis.

Output: minimal implementation, experiment, or integration note.

### 4. Measure

Collect text-based evidence: commands, logs, test results, benchmark numbers, error messages, or integration behavior.

Output: evidence summary.

### 5. Decision

Choose one: proceed, pivot, reject, or run another validation pass.

Output: decision record and next-step recommendation.

## Required Handoff

- Hypothesis
- Time box and scope
- What was built
- Evidence collected
- Decision and rationale
- Risks if proceeding

## Completion Criteria

The validation is complete when it answers the hypothesis with evidence, even if the answer is “do not proceed.”
