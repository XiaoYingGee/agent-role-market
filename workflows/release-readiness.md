# Release Readiness Workflow

## Use When

- Work is ready to ship.
- Multiple changes need coordinated release.
- Rollback, release notes, or post-release checks are required.

## Roles

- Primary: `release-coordinator`
- Supporting: `qa-engineer`, `code-reviewer`, `security-auditor`, optional `devops-engineer`
- Optional: `technical-writer` for release notes

## Phases

### 1. Scope Lock

List what is included and excluded.

Output: release scope.

### 2. Evidence Review

Check tests, review status, risk notes, and unresolved blockers.

Output: readiness checklist.

### 3. Rollback Planning

Define rollback or mitigation path. Use `devops-engineer` when pipeline steps, deployment automation, environment promotion, or rollback automation must be changed.

Output: rollback note.

### 4. Go/No-Go

Make release decision based on evidence.

Output: go/no-go decision.

### 5. Post-Release Verification

Verify behavior after release.

Output: post-release evidence.

## Required Handoff

- Release scope
- Readiness evidence
- Rollback or mitigation plan
- Go/no-go decision
- Post-release verification

## Completion Criteria

The release is complete when scope, decision, deployment evidence, and post-release verification are recorded.
