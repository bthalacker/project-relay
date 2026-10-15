# Project Relay — Intended Product Experience

**Concept, not a shipping feature list.** Relay is pre-alpha. Parts have been
demonstrated, but the complete application experience below does not yet exist.

## An educator's example

An educator has a two-hour recorded training session. Relay could eventually
find candidate pauses, repeated material, unwanted sections and transitions,
then present a short queue explaining what might need attention.

Rather than repeatedly searching the timeline, the editor selects a candidate
and Relay navigates to the relevant location. The editor can review a separately
qualified proposal or take control and make the edit normally. After saving,
Relay checks the saved changes and records what actually changed.

The educator keeps responsibility for instructional meaning: a pause may give
learners thinking time, and a repeated explanation may be useful reinforcement.
Detection is not permission to remove content.

**This educational workflow has not been validated as a complete experience.**
There is no production-use or time-saving claim for a two-hour training recording.

## Find, go, choose

Planned searches could include:

- “Find pauses longer than two seconds.”
- “Show possible transitions and recurring title sequences.”
- “Find repeated material for me to check.”
- “Take me to audio overlaps that may need attention.”

The intended design does heavy analysis ahead of interaction and reuses an index
for navigation. Each detector and navigation path needs its own qualification.
“Instant” remains a goal; current bounded landing checks are not a broad speed benchmark.

For a supported candidate:

- **Guided manual editing:** Relay yields control. The editor edits normally,
  saves in the editor and selects **Done Editing** to capture verified changes.
- **A qualified proposal or approved batch:** Relay uses an isolated working
  copy and only the permitted edit scope. Proposed artistic choices remain
  unapproved until the user accepts them; successful saving is not approval.
- **Defer:** unsupported or ambiguous work stays visible for later review.

## Review a batch without starting over

The intended integrated QC flow visits each affected area with enough picture
and separately identifiable audio context to make an editing decision:

1. **Looks Good:** accept this specific result.
2. **Not Good — Let Me Edit:** restore only the supported affected section,
   preserve independent later edits, then hand control to the editor.
3. **Done Editing:** after the editor saves, capture the correction and check
   that unrelated work survived.
4. **Review Later:** keep the item unresolved.
5. **Save & Exit:** preserve Relay progress and close its workspace. This does
   not save unsaved changes in the video editor.

The V3 queue and controls are experimental. One limited live selective inverse
has been demonstrated; the full human correction-and-resume loop is not qualified.
If dependencies or an unsupported edit prevent a safe local restore, Relay must
show the conflict and defer that correction. A whole-project rollback is a
different action and must not be substituted silently.

## History and recoverability

The planned History & Recovery area would distinguish:

| Choice | Intended meaning and current limit |
| --- | --- |
| Restore a checkpoint | Return to a verified recorded project state. Bounded known-state recovery exists; general recovery is not guaranteed. |
| Restore one edit | Preserve independent later work when that inverse and its dependencies are supported. A bounded live case exists; broader restoration remains gated. |
| Manage backups | Understand retained snapshots and storage use. A complete backup-management interface is planned. |
| Clean temporary storage | Review explicit optional cleanup of Relay-owned temporary data. Originals and accepted projects are not disposable backups. |

## Intended application areas

| Area | What the editor would use it for |
| --- | --- |
| Project Home | Open a project and see supported capabilities and recovery state. |
| Find Edits | Search supported detectors and filter candidates. |
| Guided Session | Navigate, edit, save, capture, pause and continue. |
| QC Queue | Play context, approve, defer or correct affected edits. |
| History & Recovery | Inspect checkpoints, dependencies and supported restores. |
| Preferences | Choose supported thresholds, review gates and control settings. |

These are product design areas, not six completed application screens. The
current desktop workspace is a development interface, not a public installer.

## What learning means

Saved changes show **what changed**. They do not necessarily reveal **why**.
Optional explanations can distinguish “preserve speech” from a pacing choice.
Reusable rules need positive, negative and independent examples, plus editorial
permission for the intended scope. Similarity alone cannot authorize deletion,
retention or a fade, and a correction does not automatically retrain an AI model.

See [Development status](DEVELOPMENT_STATUS.md), [Roadmap](../ROADMAP.md),
[Use cases](USE_CASES.md) and [Safety and validation](SAFETY_AND_VALIDATION.md).
