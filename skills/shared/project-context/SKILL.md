---
name: project-context
description: Discover and respect the architecture, conventions, constraints and domain rules of an existing codebase.
---

# Project Context Discovery

1. Confirm repository root and branch.
2. Read repository-specific agent instructions and contribution guides.
3. Inspect manifests, lockfiles, app entry points, routing/navigation, state management and data boundaries relevant to the task.
4. Identify runtime versions, platform targets and architectural patterns from actual files.
5. Find nearby implementations and tests; follow established patterns unless they are demonstrably defective.
6. Identify generated code, vendored code and files that must not be edited manually.
7. Check Git status before edits; preserve pre-existing user changes.
8. Do not claim a dependency, API or feature exists until verified in the repository.

Record facts separately from assumptions. If context is insufficient, request the missing artifact or permission.
