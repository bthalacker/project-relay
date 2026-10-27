# Project Relay — AI-Assisted Video Editing Automation

**Less repetitive video editing, more control over the finished result.**

Project Relay aims to help video creators find repetitive editing work, make
supported changes, and review the results while keeping creative decisions with
the editor. Its direction is **Guided Adaptive Editing**: assistance that can
learn from verified examples without treating every similar scene as permission
to edit.

**Pre-alpha · Development codename · No public download or open beta**

Project Relay is a development codename, not the final commercial product name
or a trademark claim.

## The problem

Recorded classes, tutorials and other long videos can take considerable effort
to search, trim and check. Locating transitions, removing unwanted material,
cleaning audio and revisiting earlier edits can consume time before the editor
is satisfied with the result.

## Guided Adaptive Editing

Relay's direction is to analyze footage, identify editing opportunities, and
either propose an independently qualified change or hand control to the editor.
Observed saved edits describe what changed; they do not automatically reveal
artistic intent or authorize another similar edit.

The planned complete architecture is:

**Analyze → Build Proposed Edit Plan → Preview → Review/Correct → Execute → Verify → Export**

Parts exist in bounded development workflows. The complete reviewable-plan,
execution and export experience is **planned, not qualified end to end**.

## Preview-first quality control

The development workspace now supports embedded video/audio playback,
Before/After source previews, separately identified outgoing/incoming audio,
searchable editing history, revisiting reviews, explicit approval/correction
states, and saved-session resume.

The everyday direction is **Preview → Looks Good → Next Preview**. Advancing a
source preview does not require Filmora navigation. Optional **Inspect in
Filmora** requests a fresh verified landing; correction workflows use saved-edit
capture and retain their separate safety gates.

A bounded supervised three-case batch recorded two accepted results and one
captured human correction. Automated testing also exercised the genuine visible
interface across 17 case workflows. Neither result qualifies every project,
all restoration paths or long unattended sessions.

### Audio preview and fades

Supported source previews offer Keep, Delete Tail, outgoing fade, incoming fade
and combined fade simulations, with relative fade presets. Separate stems make
audio ownership explicit. Unsupported source mappings and saved envelopes remain
gated, and no-tail cases do not offer redundant choices.

**Approving an audio preview records only that specific simulation decision.
It does not apply the treatment in Filmora or certify final rendered output.**
Native audio Apply remains disabled in the current QC workspace.

## October 27 engineering QA milestone

| Check | Recorded scope |
| --- | --- |
| Historical records audited | 94; 59 reconstructable, 35 evidence-gated |
| Genuine GUI testing | 17 case workflows and eight cross-case workflow types |
| Local QC regression suite | 263 tests passed |
| Launcher smoke suite | 82 tests passed, reported separately |
| Native editor checks | Six bounded checks, including one tiny diagnostic export |
| Preservation | 65 protected file hashes matched; existing decisions and editing histories preserved |

Reconstructable does not mean executed or approved. Test suites overlap and are
not added into an overall reliability score. See the
[public milestone report](docs/QA_MILESTONE_2026-10-27.md) for methods and limits.

Recent fixes address history selection undoing Next, stale preview controls,
cached treatment binding, single-instance handling, session-save retries and
source-bound incoming-title evidence. Older bounded workflows also demonstrated
saved-change comparison, authorized execution and selective restoration.
[Development status](docs/DEVELOPMENT_STATUS.md) separates those scopes.

## Editing safety and current limits

Relay emphasizes preserved originals and accepted work, saved-project checks,
recorded operation history, verified supported recovery, and explicit stops
when evidence is missing. These are bounded results, not a general recovery
guarantee.

- **Native render discrepancy remains open:** an isolated export retained a
  graphic frame even though decoded source evidence and saved geometry indicated
  a clean start. No accepted correction was applied.
- **Navigation is not fast-qualified:** earlier bounded single-seek checks
  passed, but latest difficult checks took about 77–107 seconds and needed
  multiple bounded seek candidates.
- **35 historical records remain gated** on missing qualified reconstruction
  evidence.
- Unattended artistic editing, arbitrary project support, broad final rendered
  audiovisual QC and universal restoration remain unqualified.

The vendor-neutral vision, verified backups, selective correction, adaptive
proposals, and future editor adapters remain active product goals. No public
download, open beta or availability date is announced.

## Potential applications

Relay could eventually assist people creating **educational videos, recorded
classes, tutorials, webinars, training presentations and other long-form content**.
For example, an instructor could review suggested pauses or recurring sections
without repeatedly searching the timeline. Editors would retain control over
instructional meaning, pacing and what should stay.

These workflows have not been validated with outside educational organizations.
There are no measured time-saving promises. Read the [potential use cases](docs/USE_CASES.md).

## High-level architecture

```text
Media → Analysis → Semantic edit plan → Review / approval
                                            ↓
                                      Editor adapter
                                            ↓
                                        Execution
                                            ↓
                               Validation / reconciliation
```

The design keeps analysis and edit intent independent of a particular editor.
Adapters translate supported operations and verify results for each editor.
Filmora 14 is the initial development target; additional adapters must earn
their own qualification. See [Architecture](docs/ARCHITECTURE.md) and
[Editor adapters](docs/EDITOR_ADAPTERS.md).

## Development status and roadmap

Project Relay remains **pre-alpha**, with a development version concept of
`0.0.1-dev`. It is not a production-ready application or a general-purpose public
download. A preview-first QC prototype now functions in bounded development workflows;
product-wide QC qualification remains a requirement for the eventual **0.1
experience**, not an announced release.

The visual [milestone roadmap](ROADMAP.md) describes demonstrated, experimental,
blocked and planned work without speculative completion dates. See also the
[intended product experience](docs/PRODUCT_EXPERIENCE.md) and [Changelog](CHANGELOG.md).

## Future collaboration

Relay may eventually benefit from feedback from creators, instructors and
organizations with different editing workflows. **External testing is not open.**
No partnership, pilot commitment or endorsement is being announced.

Before accepting outside media, Relay needs a defined supported workflow,
permission and privacy arrangements, isolated testing, verified recovery and
a feedback process. The [external-testing readiness plan](docs/EXTERNAL_TESTING.md)
explains these prerequisites. Please do not upload private footage or project
files to public issues.

## Project documentation

- [Development status](docs/DEVELOPMENT_STATUS.md)
- [Product experience](docs/PRODUCT_EXPERIENCE.md)
- [Potential use cases](docs/USE_CASES.md)
- [Architecture](docs/ARCHITECTURE.md)
- [Qualification strategy](docs/QUALIFICATION_STRATEGY.md)
- [Safety and validation](docs/SAFETY_AND_VALIDATION.md)
- [Future external testing](docs/EXTERNAL_TESTING.md)
- [Security](SECURITY.md)

## Trademarks

Filmora, DaVinci Resolve, and Adobe Premiere Pro are trademarks of their
respective owners. Project Relay is not affiliated with or endorsed by their
respective owners.
