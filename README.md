# Project Relay — AI-Assisted Video Editing Automation

**Less repetitive editing. More control over the result.**

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

## Our approach

**Analyze footage → Find editing opportunities → Navigate → Propose a qualified
edit or hand over control → Review → Correct or approve → Continue**

This is the intended complete workflow. Individual parts have been demonstrated;
the entire experience is still under development. Relay's goal is to reduce the
total effort of reaching an accepted edit, including review and correction.

## What's working today

The private development prototype has demonstrated these limited capabilities:

- **Compare saved edits:** identify removed picture/audio, retained detached
  audio and saved fade settings without inventing the editor's artistic reason.
- **Execute previously authorized edits:** bounded Filmora workflows with saved
  project checks, source-coverage verification and protected earlier history.
- **Hand control to a human:** one live guided navigation, manual edit, saved
  change capture and safe pause demonstration.
- **Use a desktop workspace:** a dark interface with contextual controls,
  progress, and Save & Exit, window-close and Ctrl+Q handling. Its focused tests
  cover session behavior; they do not prove repeated live editing reliability.
- **Restore an earlier isolated edit:** one bounded live restoration preserved
  ten later edits and 37 saved fade settings. Only a qualified subset is supported;
  dependent or unsupported changes remain blocked.

Two bounded shared-navigation checks also passed. **Fast navigation across
representative projects, long-session reliability, full rendered audiovisual QC
and unattended artistic editing remain unqualified.** A successful save does not
establish that an edit looks or sounds right.

See [Development status](docs/DEVELOPMENT_STATUS.md) for separately scoped results.

## What we're building

- Guided editing with reliable navigation and clear human handoffs.
- Searchable editing opportunities, including supported pauses, titles,
  transitions and repeated material.
- Proposals informed by user-approved examples and independently tested rules.
- Safe batches followed by integrated playback, approval and correction in QC.
- Verified checkpoints, understandable history and backup management.
- Selective restoration that preserves independent later work when supported.

These are development goals, not a list of available product features. The
complete live correction-and-resume loop still needs qualification. Experimental
editorial proposals remain explicitly unapproved until reviewed.

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
download. Integrated QC is a requirement for the eventual **0.1 experience**,
not a completed feature or an announced release.

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
