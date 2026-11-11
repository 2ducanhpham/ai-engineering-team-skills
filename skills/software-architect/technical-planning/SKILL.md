---
name: technical-planning
description: Turn product and engineering requests into sequenced, testable implementation plans with clear ownership.
---

# Technical Planning

1. Rewrite the request as an observable user or system outcome.
2. List assumptions, unknowns and constraints.
3. Inspect relevant code and identify reuse points.
4. Split work into small vertical slices; avoid vague tasks such as “improve architecture”.
5. For every task specify owner, scope, dependencies, acceptance criteria, tests and risk.
6. Sequence foundational work before dependent work.
7. Include rollout, monitoring and rollback when behavior or data changes.
8. Identify decisions requiring Tech Lead approval.

Acceptance criteria must be testable and avoid subjective terms unless paired with measurable examples.
Do not start implementation in plan-only mode.
