---
name: test-driven-development
description: Use tests to define expected behavior and protect changes against regression.
---

# Test-Driven Development

1. Identify behavior and observable contract.
2. Choose the lowest test level that gives meaningful confidence: unit, component, integration, contract or end-to-end.
3. Write a failing test for the expected behavior and important edge cases.
4. Confirm the test fails for the intended reason.
5. Implement the minimum code to pass.
6. Refactor while keeping tests green.
7. Add negative, boundary, permission and failure-path tests.
8. Avoid brittle tests coupled to implementation details.
9. Report test scope and gaps honestly.

When a legacy test suite is unstable, isolate baseline failures from regressions introduced by the change.
