# Safety and validation

Project Relay is being designed to make editing automation observable and to reduce the chance that uncertain results are treated as success. A limited deterministic Filmora subset has demonstrated guarded execution, saved-project verification, checks for unexpected changes to unrelated timeline contributions, and verified rollback/recovery in live qualification. These claims apply only to that qualified scope.

- Use relevant project-bound evidence and verify expected editor state before guarded actions.
- Treat expected Open and Save As dialogs as explicit workflow states.
- Validate expected results in the saved project and reconcile observed state against the plan.
- Preserve unrelated timeline contributions and source media; flag unexpected changes.
- Record mutations so recovery can be checked, and verify rollback rather than assuming it succeeded.
- Stop or gate for review when conditions are unexpected or evidence is uncertain.
- Continue testing repeatability and safe failure behavior against human-reviewed references.

Broader operation coverage, recovery behavior, and end-to-end qualification remain in progress. This document does not claim support for all Filmora editing or production readiness.
