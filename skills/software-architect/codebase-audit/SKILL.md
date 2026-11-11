---
name: codebase-audit
description: Perform a structured, read-only audit of an unfamiliar codebase and report verified findings.
---

# Codebase Audit (READ-ONLY)

## Rules
Do not modify files. Do not install dependencies. Do not run destructive commands. Preserve the working tree.

## Audit sequence
1. Confirm root, branch, Git status and project instructions.
2. Inventory app entry points, modules, dependencies, build scripts and test suites.
3. Trace the relevant user flow end-to-end: UI → state → domain/service → API/storage.
4. Review error handling, validation, permissions, concurrency and lifecycle behavior.
5. Inspect test coverage and identify untested high-risk paths.
6. Check dependency health and configuration exposure without disclosing secret values.
7. Record findings with evidence, impact, severity and confidence.
8. Recommend prioritized remediation; separate quick wins from architectural work.

## Severity
Critical: likely compromise, data loss or broad unauthorized access.
High: serious exploitable weakness or major user-impacting failure.
Medium: meaningful risk with constraints or limited scope.
Low: minor weakness or maintainability issue.
Info: observation or hardening opportunity.

Never call an issue confirmed if evidence is only circumstantial.
