# Development status

**Updated October 9, 2026 · Pre-alpha · No public beta or production release**

Project Relay is a development codename. Qualification describes a bounded
workflow and its evidence, not general support for an editor or artistic decisions.

## Demonstrated within a limited scope

| Capability | Evidence and boundary |
| --- | --- |
| Saved-project change comparison | Initial comparison validation recorded 20 focused tests and recognized 6/6 held-out observational examples. Recognition does not choose an edit on unseen footage. |
| Blind saved-change recovery | Identified eight picture removals, eight audio removals, four retained detached-audio clips, and three positive saved fade-outs without an explanation of artistic purpose. Saved settings do not establish rendered audio quality. |
| Guided manual handoff | One live candidate navigation, full human handoff, saved edit capture, and safe pause. The saved comparison was independently reproduced. Navigation required active development assistance. |
| Guided focused validation | Recorded 27/27 passing tests, including saved-state gates, human ownership, stale proof, interrupted-state handling, and distinct proposal/correction records. Automatic lifecycle tests used a simulated executor. |
| Earlier deterministic Filmora subset | Limited approved planning, guarded execution, project-bound A/V ownership, saved-state reconciliation, expected Open/Save dialog handling, and verified rollback. This is separate from guided editorial proposal qualification. |

Observations, human approval, and editorial hypotheses remain distinct.
Overlap alone does not establish a fade or justify retaining/deleting audio.
Existing protected editing checkpoints were preserved during the demonstrations.
No project/source materials or internal evidence are distributed here.

## Experimental or not qualified

- Repeated guided next-edit/save/advance sessions, general landing accuracy,
  and long-session interruption behavior.
- Guided automatic editorial proposals on live projects. None was qualified
  by the manual pilot; simulated lifecycle tests are not live qualification.
- Prospective adaptive decision rules. Recognizing a saved edit or similar
  footage does not authorize another edit or automatically retrain an AI model.
- Arbitrary partially edited project reconciliation and Smart Resume. Recovery
  of a known recorded transaction is a different, narrower capability.
- Broad audio ownership, transition decisions, structural coverage, and rendered
  audiovisual quality across new material. Uncertainty continues to gate edits.
- Unattended full-project completion and guaranteed recovery.

## Planned product capabilities

- Low-latency local navigation and a reusable candidate index, with measured
  landing accuracy and latency.
- Searchable detection for silences, transitions, titles, recurring material,
  and audio concerns. Each detector needs separate validation.
- Editing and QC through one understandable queue, with context playback,
  corrections, skip/review-later, and verified save capture.
- Backup/history visibility, verified restores, storage estimates, and optional
  explicit cleanup confined to Relay-owned temporary data.
- Dependency-aware selective restoration of an earlier edit; future research.
- Project creation/media import, onboarding, configuration, accessible controls,
  reproducible qualification, and copyright-safe demonstrations.
- External beta testing only after a useful bounded workflow and recovery tests
  demonstrate real time savings and documented limitations.
- Independently qualified DaVinci Resolve, Adobe Premiere Pro, and other future
  editor integrations. They are not supported today.

See the [Roadmap](../ROADMAP.md), [Product experience](PRODUCT_EXPERIENCE.md),
[Qualification strategy](QUALIFICATION_STRATEGY.md), and [Changelog](../CHANGELOG.md).
Recorded test counts are development observations, not a public benchmark or a
claim that these tests were rerun for this documentation update.
