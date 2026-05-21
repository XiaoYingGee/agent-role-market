# Workflows

Workflows define how role packs are combined for common work patterns.

Each workflow is tool-agnostic. It does not assume a specific chat platform, agent runtime, task board, or repository host.

## Workflow Principles

- Use one primary owner per phase.
- Use one primary role and at most two supporting roles per task.
- Keep a task record outside conversation memory.
- Require handoff evidence before moving to the next phase.
- Split the task when more than three roles are needed at the same time.

## Common Workflows

| Workflow | Use For |
|---|---|
| `requirement-clarification.md` | Turning vague asks into scoped work |
| `feasibility-validation.md` | Testing feasibility before full build |
| `standard-feature-delivery.md` | Product/design/engineering/QA feature delivery |
| `bugfix-regression.md` | Reproducing, fixing, and preventing regressions |
| `security-review.md` | Reviewing security-sensitive changes |
| `release-readiness.md` | Preparing and verifying a release |
| `incident-response.md` | Handling production or critical workflow incidents |

## Generic Phase Model

```text
INTAKE -> SPEC -> DESIGN -> BUILD -> REVIEW -> RELEASE -> RETRO
```

Small tasks may skip phases, but they should not skip owner, scope, expected output, verification evidence, and handoff.
