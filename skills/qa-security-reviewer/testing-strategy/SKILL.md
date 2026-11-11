---
name: testing-strategy
description: Create a pragmatic test strategy that prioritizes user-critical flows, regression risk and observable outcomes.
---

# Testing Strategy

1. Map requirements to observable behaviors.
2. Identify risk by impact, likelihood, change surface and usage frequency.
3. Select test layers: unit, component/UI, integration, API/contract, E2E, performance and exploratory.
4. Include happy paths, boundaries, invalid inputs, permission failures, network failures, retries and lifecycle interruptions.
5. Prioritize critical journeys and historically fragile modules.
6. Keep tests deterministic; control time, randomness, network and external dependencies.
7. Use representative devices, OS versions and screen sizes for mobile.
8. Report coverage gaps and flaky tests separately from product defects.
9. Define release-blocking criteria before testing.

Do not equate test count with quality. Explain what the tests prove and what they do not prove.
