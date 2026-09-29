# Safety and validation

Project Relay is being designed to make editing automation observable and to reduce the chance that uncertain results are treated as success. The following are product-level design goals and active development requirements.

- Verify relevant editor state before taking actions.
- Validate expected edit results after execution.
- Preserve source media.
- Stop when conditions are unexpected or uncertain.
- Avoid silent destructive failures.
- Retain appropriate evidence and diagnostics for verification and troubleshooting.
- Test repeatability across qualification runs.

Validation, reconciliation, failure detection, and safe-stop behavior are central to the design. Their implementation and qualification remain in progress; this document does not claim production readiness.
