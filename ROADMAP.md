# Project Relay — Product and Engineering Roadmap

**Pre-alpha · Development codename · Updated October 27, 2026**

**Vision:** Reduce repetitive video-editing work while keeping the editor in
control of meaning, pacing and the final result.

This is a milestone roadmap, not a release schedule or an availability promise.
Workstreams overlap. A bounded demonstration does not complete a whole phase.

## Milestone map

```mermaid
flowchart TD
    A["1. Foundation — bounded demonstrations"] --> B["2. Guided Editing — partially demonstrated"]
    B --> C["3. Adaptive Automation — experimental"]
    C --> D["4. Integrated QC — preview-first prototype"]
    D --> E["5. Selective Restoration — bounded live demonstration"]
    E --> F["6. Product Reliability — qualification in progress"]
    F --> G["7. External Beta — planned, not open"]
    G --> H["8. Future Integrations — planned or exploratory"]
```

| Phase | Current position | Evidence required to advance |
| --- | --- | --- |
| **1. Foundation** | **Demonstrated in bounded workflows.** Media analysis, native project inspection, source mapping and saved-change comparison support current experiments. | Broader supported media/project structures, independently checked boundaries and source coverage, with explicit handling of unsupported cases. |
| **2. Guided Editing** | **Partially demonstrated.** Initial live handoff/capture, a desktop workspace, a later bounded supervised review/correction batch, and shared-navigation checks. | Repeated live navigate → handoff → save → capture cycles; reliable pause/resume, exact current-state navigation and measured latency across representative projects. |
| **3. Adaptive Automation** | **Experimental, with bounded authorized execution demonstrated.** Eleven automatic edits and one later reviewed edit completed in separate verified continuation work. | Tested rules derived from approved examples, positive/negative and held-out cases, explicit editorial authority, and no duplicate changes. General audio/artistic choices remain blocked. |
| **4. Integrated Quality Control** | **Working development prototype; broader qualification open.** Embedded preview-first playback, searchable history, scoped approvals, audio simulations, a bounded supervised batch and 17 isolated real-widget case workflows. | Broader repeated review/correction cycles, native-render equivalence, supported restoration paths and preservation under interruption. Preview approval alone does not qualify output. Required for the eventual 0.1 experience. |
| **5. Selective Restoration** | **Bounded live demonstration.** An earlier isolated edit was restored while ten later edits and 37 saved fade settings remained intact. | Complete human correction-and-resume qualification, more supported edit types, dependency/conflict handling and preservation of later work. Several inverse scenarios remain gated. |
| **6. Product Reliability** | **QA harness and bounded recovery foundations demonstrated; product work remains.** October 27: 94-record audit, 263 local regression tests, 82 separate smoke tests and six bounded native checks; open render/performance defects retained. | Performance, verified backups, crash/interrupted-save tests, understandable history, installation, accessibility and usability testing. No guaranteed recovery claim. |
| **7. External Beta** | **Planned; not open.** No external media intake or production pilot is authorized. | Supported-workflow assessment, permission/privacy/retention process, isolated tests, qualified recovery, actionable failure reports and a useful measured workflow. |
| **8. Future Integrations** | **Planned or exploratory.** Filmora is the initial adapter target. | Separate implementation and qualification for additional editors; feasibility work for possible native processing capabilities. |

## Planned non-destructive editing architecture

```mermaid
flowchart LR
    A["Analyze"] --> B["Build Proposed Edit Plan"]
    B --> C["Preview"]
    C --> D["Review or Correct"]
    D --> E["Execute Authorized Operations"]
    E --> F["Verify Saved and Rendered Results"]
    F --> G["Export"]
```

**Planned complete architecture, not a completed end-to-end workflow.** Preparing
a plan before mutation would let the user inspect the whole plan, revise earlier
proposals, check dependencies, execute approved operations in a controlled
sequence and verify saved results afterward. Automation can then expand only as
each operation earns evidence and authorization. Unsupported restoration or
verification must stay gated.

### Intended operating modes

| Mode | Intended behavior | Current qualification |
| --- | --- | --- |
| Review First | Analyze, prepare proposals, preview, adjust and approve the plan before execution. | Source-preview review exists in bounded workflows; complete editable-plan execution is planned. |
| Automate Then Review | Execute independently qualified, authorized edits on a protected copy, then review results. | Bounded execution and QC demonstrations exist; the general complete mode remains unqualified. |
| Full Automation | Optional analysis through editing, verification, rendering and encoding using saved preferences. | Planned and unqualified; no unattended artistic-editing claim. |

### Planned encoding profiles

Reusable codec, resolution, quality, audio configuration, subtitle handling and
export-destination preferences are future work. A bounded diagnostic native export
does not establish configurable automated rendering or encoding.

## Evidence behind the current positions

- Earlier saved-change work identified removed picture/audio, retained detached
  audio and saved fades. One blind comparison found eight picture removals,
  eight audio removals, four retained audio clips and three positive saved fade-outs.
- The initial guided pilot demonstrated one live manual handoff and capture,
  with **27/27** focused tests recorded for that scope.
- **October 10:** V2 workspace/session work recorded **60/60** focused tests.
  Repeated sequences in that run were synthetic; no new live editing cycle ran.
- **October 13:** a bounded continuation completed eleven authorized edits,
  followed by one additional previously reviewed edit. Protected history and
  saved source coverage were checked; the entire video project was not completed.
- **October 13:** selective-restoration and Batch QC V3 work recorded **59**
  focused tests passing and the bounded live restoration described above.

- **October 25–27:** bounded supervised QC, embedded preview-first review, audio
  simulations, searchable history and source-preview reconstruction advanced.
  The latest audit supports 59 of 94 records and gates 35. The October 27 campaign
  exercised 17 GUI case workflows, eight cross-case flow types, 263 local regression
  tests, 82 separate smoke tests and six bounded native checks; 65 protected hashes
  matched. See the [scoped milestone report](docs/QA_MILESTONE_2026-10-27.md).
- **Open:** a native rendered-frame discrepancy, 77–107-second difficult navigation
  checks, missing reconstruction evidence and general final-output qualification.

These counts belong to different scopes and are not added into a combined
qualification score. Automated checks do not establish artistic quality.

## Product goals that remain in scope

- **Fast navigation and searchable detection:** a reusable local candidate index,
  filters for supported pauses, transitions, titles and recurring material,
  and measured latency and landing accuracy. No per-click AI delay is a design
  goal, not an achieved performance guarantee.
- **User-approved adaptive proposals:** record what a saved edit changed; ask
  briefly about intent only when needed. A correction does not automatically
  retrain a model or authorize another similar edit.
- **Integrated QC:** share navigation and context between editing and review,
  keep unapproved proposals distinct, and support correction without losing
  unrelated later work where the inverse is qualified.
- **Verified backups and history:** checkpoint verification, clear restore
  choices, visible storage use and explicit optional cleanup limited to
  Relay-owned temporary data. Preserve originals and accepted projects.
- **A usable application:** project creation/media import, onboarding,
  configuration, accessible controls, installation and copyright-safe demos.
- **Future editors:** DaVinci Resolve and Adobe Premiere Pro remain planned
  directions, not current support or release commitments. A native processing
  backend and possible native timeline capabilities remain exploratory.

## Before external testing

The project must qualify a useful supported workflow, recovery and clear failure
handling before accepting outside content. Permissions, private handling,
retention/deletion, test isolation and feedback arrangements must be agreed first.
See [External-testing readiness](docs/EXTERNAL_TESTING.md).

## Keep this roadmap current

Update this roadmap, [Development status](docs/DEVELOPMENT_STATUS.md) and
[Changelog](CHANGELOG.md) together after verified milestones or changed limits.
Feature ideas should record the editing problem, desired outcome, priority,
dependencies, acceptance criteria and status. Completion needs evidence of its
declared scope, not just a checked box. Do not attach private media, project files
or internal evidence to public issues.

See the [Product experience](docs/PRODUCT_EXPERIENCE.md),
[potential use cases](docs/USE_CASES.md) and [Qualification strategy](docs/QUALIFICATION_STRATEGY.md).
