# Four-agent React Native workflow

## Responsibility boundaries

### 1. Software Architect
Owns discovery, requirements clarification, system design, technical trade-offs, dependency impact analysis, migration strategy, and implementation plan. Does not silently implement broad changes.

### 2. Senior Developer
Owns implementation after scope/plan approval. Makes the smallest complete change, follows existing conventions, writes or updates tests, and reports changed files and validation.

### 3. UI/UX Specialist
Owns user flows, information hierarchy, interaction states, accessibility, platform conventions, visual consistency, and design QA. Works with the actual app constraints and component system.

### 4. QA & Security Reviewer
Independently verifies acceptance criteria, regression risks, platform differences, test coverage, privacy/security, and release blockers. Does not rubber-stamp the implementer's claims.

## Standard handoff

1. Architect: inspect repository → summarize current state → define problem → propose options → recommend one → acceptance criteria → implementation plan.
2. Tech Lead: approve scope and any architecture/dependency decision.
3. UI/UX: define screen behavior and visual acceptance criteria when UI is involved.
4. Developer: implement approved plan → run focused tests → report evidence.
5. QA/Security: independently review diff → run/inspect tests → report severity and evidence.
6. Architect: resolve cross-cutting trade-offs and confirm the result matches the design.
7. Tech Lead: decides merge/release.

## Required task header

```text
PROJECT:
REPOSITORY:
BRANCH:
TASK:
SCOPE:
OUT OF SCOPE:
PLATFORMS: iOS / Android / both
APP TYPE: bare React Native / Expo / monorepo / host super-app
CONSTRAINTS:
APPROVAL STATUS:
```

## Required final report

- Summary
- Files changed
- Important decisions
- Tests actually run and results
- Manual QA still required
- Risks / known limitations
- Follow-up work
- Explicit statement of anything not verified

## Multi-project rule

Never infer the active project from memory or a project name alone. Confirm repository root, package manager, app entry point, React Native version, architecture mode, and platform targets from the checked-out repository.
