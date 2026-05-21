# Incident Response Workflow

## Use When

- Production or critical workflow behavior is failing.
- User impact, data risk, or operational risk is active.
- Immediate coordination is more important than full feature process.

## Roles

- Primary: `incident-responder`
- Supporting: `reliability-engineer`, relevant engineering role, `qa-engineer`
- Optional: `security-auditor` if access, abuse, or data exposure is possible

## Phases

### 1. Triage

Capture symptom, impact, severity, and current status.

Output: incident brief.

### 2. Contain

Stop or reduce impact using the safest available action.

Output: containment note.

### 3. Diagnose

Gather facts, timeline, logs, recent changes, and hypotheses.

Output: diagnosis summary.

### 4. Mitigate Or Fix

Apply mitigation or fix with rollback awareness.

Output: mitigation/fix evidence.

### 5. Verify

Confirm recovery using text-based operational evidence.

Output: recovery verification.

### 6. Follow Up

Record root cause, prevention work, and owners.

Output: post-incident notes.

## Required Handoff

- Impact and severity
- Timeline
- Actions taken
- Verification evidence
- Root cause or current hypothesis
- Follow-up tasks

## Completion Criteria

The incident workflow is complete when impact is resolved or accepted, verification is recorded, and follow-up work has owners.
