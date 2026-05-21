# Bugfix Regression Workflow

## Use When

- A bug must be reproduced, fixed, and protected from returning.
- There is uncertainty about root cause.
- The bug may affect existing behavior.

## Roles

- Primary: `error-detective` for diagnosis, then relevant engineering role for fix
- Supporting: `qa-engineer`, `test-automator`, `code-reviewer`
- Optional: `incident-responder` if user impact is active

## Phases

### 1. Reproduce

Capture expected behavior, actual behavior, environment, and reproduction steps.

Output: reproducible bug report.

### 2. Diagnose

Identify root cause or most likely cause with evidence. Keep the fix recommendation minimal and avoid turning diagnosis into a broad implementation plan.

Output: diagnosis note.

### 3. Fix

Apply the smallest safe change.

Output: code change and fix summary.

### 4. Protect

Add or update tests where practical.

Output: regression test or documented reason if not automated.

### 5. Verify

Run targeted and relevant regression checks.

Output: pass/fail evidence.

## Required Handoff

- Reproduction steps
- Root cause
- Fix summary
- Test evidence
- Remaining risk

## Completion Criteria

The bugfix is complete when the issue is reproducible before the fix, verified after the fix, and protected where practical.
