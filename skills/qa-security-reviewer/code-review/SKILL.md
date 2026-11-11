---
name: code-review
description: Perform independent, risk-based code reviews and report actionable defects with evidence.
---

# Code Review

1. Read the task and acceptance criteria before reviewing the diff.
2. Inspect the full diff and surrounding code; understand intended behavior.
3. Look for correctness, edge cases, error handling, data integrity, security, performance and maintainability.
4. Check compatibility with existing callers, persisted data and supported platforms.
5. Verify tests cover changed behavior and failure paths.
6. Do not report style preferences as bugs unless they violate project conventions.
7. Each finding must include severity, file/line, scenario, impact and suggested fix.
8. Distinguish confirmed defects from questions and hardening suggestions.
9. Avoid editing files during review unless separately assigned.

Review summary must state whether the change is APPROVED, APPROVED WITH CONDITIONS, REQUEST CHANGES or BLOCKED.
