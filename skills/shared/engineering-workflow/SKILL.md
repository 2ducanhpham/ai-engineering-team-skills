---
name: engineering-workflow
description: Apply a disciplined engineering workflow for software tasks, from intake through verification and handoff.
---

# Engineering Workflow

## When to use
Use for any non-trivial engineering task.

## Procedure
1. Classify the request: question, audit, plan, implementation, review, release.
2. Identify the exact repository and working directory. Never infer from project name alone.
3. Inspect project instructions, README, package manifests, architecture notes and Git status.
4. Establish baseline: relevant tests, current failures, build state and existing conventions.
5. Define scope, non-goals, acceptance criteria, dependencies and risks.
6. For implementation, assign a single owner to each overlapping file area.
7. Make the smallest coherent change.
8. Run targeted tests first, then broader checks when practical.
9. Review the diff for unintended changes, secrets, generated files and regressions.
10. Report verified outcomes and unresolved risks.

## Stop conditions
Stop and ask for approval before destructive operations, production access, schema changes, migrations, dependency additions, signing/release actions or changes with material security/privacy impact.

## Output
- Mode and repository
- Verified baseline
- Plan and scope
- Changes (if any)
- Commands and actual results
- Risks, blockers and next action
