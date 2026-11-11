---
name: debugging
description: Diagnose software defects systematically using reproducible evidence instead of speculative patches.
---

# Debugging

1. Capture the exact symptom, expected behavior, environment and reproduction steps.
2. Reproduce with the smallest reliable case.
3. Inspect logs, stack traces, network traces and recent diffs.
4. Form ranked hypotheses and identify evidence that would confirm or reject each.
5. Trace the data/control flow to the root cause.
6. Add a regression test that fails before the fix when feasible.
7. Apply the narrowest root-cause fix; avoid unrelated cleanup.
8. Re-run regression and adjacent tests.
9. Explain root cause, why the fix works and residual risks.

Do not silence errors, weaken validation or add retries as a substitute for understanding the cause.
