---
name: refactoring
description: Improve code structure while preserving externally observable behavior and minimizing regression risk.
---

# Refactoring

- Establish current behavior and tests before changing structure.
- Refactor in small, reviewable steps.
- Preserve API, persisted data, navigation behavior and platform compatibility.
- Prefer clear names, cohesive modules and explicit boundaries.
- Avoid broad rewrites without measurable benefit and an approved migration plan.
- Do not mix behavior changes with structural cleanup unless necessary.
- Run targeted tests after each meaningful step.
- Compare the diff and verify no accidental formatting churn or generated-file changes.
- Document any behavior that could not be proven equivalent.
