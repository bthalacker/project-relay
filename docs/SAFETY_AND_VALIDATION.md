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

## Guided human editing

The guided design requires complete release of editor control while the person
edits. After Done, saved identity and state must be verified before comparing
changes or permitting further automated input. One bounded handoff and pause have
been demonstrated; wider reliability remains unqualified. User originals and
accepted projects must remain distinct from disposable work.

Known-checkpoint recovery differs from selectively undoing an earlier edit or
accepting an arbitrary partially edited project. One bounded selective inverse
has now preserved ten later edits and 37 saved fade settings. Only a qualified
subset is supported; unsupported dependencies remain gated. The complete live
human correction-and-resume loop, a visible backup-management interface and
optional cleanup still require development and qualification.
No general recovery guarantee is made. See [Product experience](PRODUCT_EXPERIENCE.md).

## Proposals, correction and outside content

- Keep experimental proposals isolated and explicitly unapproved. A successful
  structural verification is not a decision about artistic quality.
- Preserve a verified restoration checkpoint separately from a human correction
  working copy. Record observed corrections without inventing their purpose.
- Do not substitute whole-project rollback for unsupported selective restoration.
- Report unknown changes and uncertain audio decisions instead of treating
  absent clips, overlapping audio or matching patterns as approval.
- Qualify rendered picture/audio QC separately from saved settings.

External testing is not open. Future testing requires explicit rights and
permissions, private handling, agreed retention/deletion, original preservation
and a supported-workflow assessment. These are required preparations, not a
current service guarantee. See [External-testing readiness](EXTERNAL_TESTING.md).

## Preview approval and current evidence limits

Source-derived previews identify their sources, scope and whether they reconstruct
saved geometry or propose an unexecuted change. Explicit approval applies only
to that reviewed scope, does not grant future similar-edit authority, does not
apply a native treatment and does not certify final rendered audiovisual QC.
Native audio Apply is currently disabled.

The October 27 campaign preserved 65 protected file hashes and prior decisions.
It also reproduced a native exported-frame discrepancy despite decoded-clean
source geometry. No correction was promoted to accepted work. Missing evidence
still gates 35 historical reconstructions. These are reasons to retain strict
source, saved-state and rendered checks, not to weaken them.

A changed saved project must invalidate stale geometry/approval bindings.
Read-only browsing can remain available while fresh reconciliation gates native
actions. Existing save retries, single-instance controls and bounded recovery
tests reduce specific risks; arbitrary external changes and universal recovery
remain unqualified. See the [scoped milestone](QA_MILESTONE_2026-10-27.md).
