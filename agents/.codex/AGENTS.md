# Agent Role Market Instructions

Use this repository as a role-pack and workflow library.

## Source Directories

- `roles/`: reusable role packs grouped by work type.
- `workflows/`: common multi-role workflows.
- `templates/`: role pack templates.

## Selection Rules

1. Identify the task type and choose one primary role from `roles/`.
2. Add at most two supporting roles.
3. If the task matches a known flow, use the matching file in `workflows/`.
4. Keep role selection explicit in the task summary.
5. Require text-based evidence before calling work complete.

## Handoff Rules

Every completed task should include:

- Conclusion
- Completed work
- Artifact locations
- Verification evidence
- Risks and open questions
- Recommended next step

Do not rely on conversation memory as the only source of task state.
