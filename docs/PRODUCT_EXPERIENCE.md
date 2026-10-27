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

## Current preview-first development workspace

For supported cases, the working development flow is:

**Preview → Looks Good → Next Preview**

Before/After picture and separately identified outgoing, incoming and retained
audio play inside Relay. History search revisits an edit without automatically
moving Filmora. Selecting another case or treatment loads without autoplay; an
explicit Play starts playback.

Supported treatment simulations offer unchanged audio, tail deletion, outgoing
fade, incoming fade and combined fades with relative presets. Approve Audio
Preview records only that exact simulation choice. Native Apply remains disabled.
A saved-state reconstruction, original excerpt and unexecuted proposal must be
labelled differently; none is silently called a native export.

**Inspect in Filmora** is optional. **Let Me Edit** requires fresh verified native
navigation and a safe handoff; after saving, **Done Editing** or **Capture Saved
Changes** records the saved difference without inventing its artistic reason.
Inspecting alone is not an approval, and Back to Previews does not undo the editor.

A bounded supervised three-case batch and isolated real-widget tests support
these claims. Wider reliability, unsupported restorations and final rendered QC
remain open. Current native navigation can take 77–107 seconds in difficult
cases; users should not mistake a slow pending seek for completion.

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

A preview-first queue and scoped approval/capture now function in development.
One bounded supervised batch captured a correction; one earlier limited live
selective inverse was demonstrated separately. This does not qualify the complete
correction/restoration loop for every edit shape.
If dependencies or an unsupported edit prevent a safe local restore, Relay must
show the conflict and defer that correction. A whole-project rollback is a
different action and must not be substituted silently.

## Planned complete-plan experience

The longer-term architecture is **Analyze → Build Proposed Edit Plan → Preview
→ Review/Correct → Execute → Verify → Export**. Reviewing the entire proposal
before mutation would allow dependency checks and revisions to earlier choices.
This full workflow is planned, not delivered.

Intended modes are Review First, Automate Then Review for qualified authorized
operations on a protected copy, and optional Full Automation. Full Automation,
saved output preferences and configurable encoding remain planned and unqualified.

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
