---
name: implementation
description: Implement scoped software changes safely, consistently and with production-quality engineering practices.
---

# Implementation

1. Read the task, acceptance criteria and repository instructions.
2. Inspect adjacent code and existing patterns before editing.
3. Confirm Git status; do not overwrite unrelated user changes.
4. Make the smallest complete change within assigned scope.
5. Preserve public contracts unless explicitly authorized to change them.
6. Handle loading, empty, error, success and boundary states where relevant.
7. Add/update tests alongside behavior changes.
8. Run formatter, lint, typecheck and relevant tests available in the project.
9. Review the final diff for accidental changes, debug code, secrets and generated artifacts.
10. Report exact files changed and checks actually run.

Ask before adding dependencies, changing schemas, modifying authentication, or altering release/build configuration.
