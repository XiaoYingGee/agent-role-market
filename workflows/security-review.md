# Security Review Workflow

## Use When

- Work touches authentication, authorization, secrets, payments, user data, external input, deployment exposure, or sensitive logs.
- A release needs security confidence.

## Roles

- Primary: `security-auditor`
- Supporting: `code-reviewer`, `qa-engineer`
- Engineering support: `backend-architect`, `api-designer`, `frontend-engineer` as needed

## Phases

### 1. Scope

Define changed assets, trust boundaries, sensitive data, and user impact.

Output: security scope.

### 2. Threat Review

Identify abuse cases and likely attack paths.

Output: threat list.

### 3. Control Review

Check authorization, validation, data handling, logging, dependency, and configuration risks.

Output: findings with severity.

### 4. Fix Or Accept

Assign mitigations or record accepted risk.

Output: mitigation plan.

### 5. Verify

Confirm fixes or compensating controls.

Output: verification evidence.

## Required Handoff

- Scope
- Findings by severity
- Mitigations
- Verification evidence
- Residual risk

## Completion Criteria

Security review is complete when risks are either mitigated or explicitly accepted by the decision owner.
