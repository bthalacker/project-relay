# Project Relay — Product Experience (Concept)

> **Design concept, not a shipping feature list.**
> Project Relay is in pre-alpha. The complete experience below does not yet exist.

## A simple editing session

The user opens a project and tells Relay what kind of edit to find:

- “Find silences longer than two seconds.”
- “Show possible scene transitions.”
- “Find title cards or recurring bumper sequences.”
- “Take me to audio overlaps I should check.”

Relay's intended workflow is to analyze footage in the background, index
candidate locations, and present a queue with concise descriptions and
confidence indicators. The editor selects **Next** or picks a result to go
directly to that location.

For each candidate, one of two paths is available:

**Guided manual editing.** Relay navigates and fully yields control.
The editor makes any preferred changes in the native editing program,
saves, and clicks **Done Editing**. Relay compares saved versions, records
what changed, and advances.

**Reviewed automatic proposal.** For a separately qualified edit category,
Relay proposes an edit on an isolated working copy. The editor approves
it or makes a correction. Approval and correction history become distinct
evidence. Automatic proposals are **not qualified today**.

## Quality control without a second learning curve

The planned navigation queue is intended to support **Quality Control** mode:

1. Visit edited locations, uncertain boundaries, and detected anomalies.
2. Play or inspect relevant context in the editor.
3. Mark **Correct**, **Fix It**, or **Review Later**.
4. After a fix, capture the saved differences and update the issue status.
5. Advance without requiring the editor to interpret internal frame maps.

A later, separately qualified batch mode may allow approved categories to run
with checkpoints, followed by this QC queue. It must not silently treat
uncertain decisions as approved.

## Recoverability and trust

The intended **History & Recovery** screen would distinguish:

- **Restore checkpoint:** Return to a previously verified project state.
- **Restore selected edit:** Reverse one earlier edit, preserving independent
  later changes when dependency checks permit. This is future research.
- **Temporary storage cleanup:** Show Relay-generated files and estimated
  recoverable disk space, then request explicit confirmation.
- **Keep originals:** User source media and accepted finished projects are
  never treated as disposable backups.

Recovery capability must be proven through fault and compatibility testing.
It is not currently a promise that every editing mistake can be undone.

## Proposed interface areas

| Area | Purpose |
| --- | --- |
| **Project Home** | Open a project, view its supported editor and recovery state. |
| **Find Edits** | Choose supported detectors or request a plain-language search. |
| **Guided Session** | Next / Previous, Let Me Edit, Done Editing, approve/correct, skip, pause. |
| **QC Queue** | Revisit uncertain or completed work and track corrections. |
| **History & Recovery** | Inspect verified snapshots, restore when safe, manage backups. |
| **Preferences** | Configure detector thresholds, review gates, and user control settings. |

## Performance and learning philosophy

An interactive jump should not require the AI to reason through the entire
video again. The intended design separates **background analysis**,
**deterministic indexed navigation**, and **saved-result verification**.
Seek latency and frame accuracy will be benchmarked on representative
projects; “instant” remains a goal, not a current measured capability.

Saved human edits can show exactly **what changed**, even when the software
cannot establish **why**. Optional labels such as “keep speech” or
“remove bumper” may help describe the preference, but proposed reusable
rules require independent positive and negative testing.

### Current boundary

One bounded live manual handoff and native saved-edit comparison have been
demonstrated. The pilot still requires active development assistance for
navigation; repeated guided sessions have not been qualified. A finished standalone interface, reliable rapid navigation,
independently qualified automatic edit proposals, selective restoration,
and an externally available beta are future work.

See [Development status](DEVELOPMENT_STATUS.md) for demonstrated scope and the
[Roadmap](../ROADMAP.md) for milestone acceptance criteria.
