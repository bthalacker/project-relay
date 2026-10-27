# Qualification strategy

Project Relay is in pre-alpha. This document describes the qualification methodology and the limits of current results, not a claim that every step is complete or that any adapter is production-ready.

A limited deterministic Filmora workflow has completed live qualification through planning, guarded execution, saved-project verification, and verified rollback. Qualification against human-reviewed reference results continues, and broader operation coverage and generalization remain open work.

## Establish a human-reviewed reference

For each qualification campaign, define the editing task and expected result before running automation. Use a human-reviewed gold standard so comparisons are based on an agreed interpretation of the media and intended edits. Use material that is appropriate and cleared for the test and any planned public demonstration.

## Qualify against known material

Use a controlled set of known cases to establish a baseline. Record the project version, relevant configuration, expected outcomes, and observed results for each run. Keep the case definitions stable while evaluating a build; if the system or criteria change, begin a separately identified run.

## Keep a holdout set

Evaluate previously unseen media separately from material used during development. Do not tune behavior against holdout outcomes and then report those same outcomes as independent validation. Review rules for dependencies on specific titles, scenes, filenames, or other content-specific cues; such rules do not demonstrate generalization.

## Classify failures

When an outcome differs from the reference, record the high-level failure category and whether the system detected it and stopped safely. Useful categories include semantic detection, edit timing, audio/video correctness, editor execution, result verification, and recovery. A detected mismatch or safe stop should remain visible as a qualification result rather than being counted as a successful edit.

## Repeat from verified baselines

Use the same defined inputs and configuration for comparable runs. Start from a
verified baseline or independently verified recovery state; preserve accepted
work and distinguish a new test copy from a clean original. Compare outcomes
across runs and investigate differences before claiming repeatability.

## Extend qualification across editors

Where practical, use the same editor-neutral edit-plan cases to qualify each adapter. Filmora is the first adapter; qualification currently applies to a limited deterministic subset. DaVinci Resolve and Adobe Premiere Pro adapters are planned; cross-editor qualification can happen only when those adapters exist and are ready to evaluate.

## Qualification decisions

Set acceptance criteria before a campaign begins. Describe which cases were run, what passed or failed, how safely detected failures were handled, and what limitations remain. Qualification should support a clear, repeatable claim about a defined workflow rather than imply broader support than the evidence shows.

## Guided prototype qualification boundary

The first guided milestone demonstrated one manual handoff and saved-change
capture, with 27 recorded focused tests passing. Proposal/approval/correction
lifecycle tests used a simulated executor. They do not qualify a live automatic
editorial proposal. Earlier held-out examples test recognition of observed saved
changes, not prospective artistic choices.

Further qualification needs consecutive guided cycles, representative navigation
and latency measurements, interrupted saves, unknown external changes, rejected
proposals, and verified recovery. Report actual live scope separately from unit
tests and simulations. Saved geometry alone does not establish editorial or
rendered audiovisual correctness. See [Development status](DEVELOPMENT_STATUS.md).

## Later workspace, batch and restoration campaigns

The October 10 V2 campaign recorded 60/60 focused tests, including synthetic
session and layout checks; it ran no new live editing cycle. The October 13
restoration/Batch QC campaign recorded 59 focused tests and a separately bounded
live inverse preserving ten later edits and 37 saved fade settings. A continuation
also completed eleven authorized edits followed by one additional reviewed edit.
These are distinct evidence scopes, not a combined application qualification score.

Selective restoration requires source-coverage, audio ownership, saved-envelope,
later-work preservation, conflict, interruption and recovery checks. A complete
old-project rollback does not prove selective restoration. Offline lifecycle
tests do not qualify the full live human correction-and-resume loop.

Rendered audiovisual checks and editorial approval must be evaluated separately
from saved-project structure. Experimental proposals remain unapproved after a
successful save. External workflows require their own support assessment and
permission/privacy arrangements before media intake; see
[External-testing readiness](EXTERNAL_TESTING.md).

## October 27: layered engineering QA

The latest campaign combines an offline 94-record audit, 17 genuine visible
case workflows, eight cross-case flow types, 263 local regression tests, 82
separate smoke tests and six bounded native checks. See the
[public milestone report](QA_MILESTONE_2026-10-27.md). Existing results were
inspected rather than rerun for publication.

Use complementary evidence layers:

1. Unit/regression tests for exact contracts and negative cases.
2. Saved-project checks for source coverage, ownership and unrelated work.
3. Independently decoded source frames and audio samples for preview composition.
4. Real interface tests for actual controls, playback and state transitions.
5. Bounded native editor checks on disposable projects.
6. Isolated native exports decoded independently to test rendered behavior.
7. Human review for artistic choices and audiovisual acceptance.

These layers are not interchangeable. The small native export exposed an unwanted
graphic despite decoded-clean saved geometry; this remains a failure requiring
investigation, not a successful edit qualification. Preserve such negative
evidence and do not change expected values merely to obtain PASS.

## Planned independent black-box testing

Ongoing engineering combines regression checks with autonomous exploratory QA.
For significant milestones, a separate testing assignment should approach Relay
as a first-time user without implementation knowledge, explore workflows and
produce an independent defect report before engineering investigates fixes.
The current engineering-authored harness is not independent external testing.
External beta testing has not occurred and is not open.

Future campaigns should expand interruptions, unknown external saves, rejected
proposals, supported restoration and recovery, representative project structures
and native-rendered audio/video checks. Record distinct workflow coverage and
actual latency; assertion totals alone cannot establish usability or quality.
