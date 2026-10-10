# Project Relay

**Development codename:** Project Relay  
**Status:** Pre-alpha · active development  
**Development version concept:** `0.0.1-dev`

Project Relay is a vendor-neutral video editing automation platform evolving toward **Guided Adaptive Editing**. It aims to find useful edit locations, guide the editor to them, support manual editing or separately qualified proposals, and verify saved results through editor-specific adapters.

Project Relay is a development codename, not the final commercial product name or a trademark claim.

## The problem

Repetitive and precision-sensitive edits can take substantial time and are easy to apply inconsistently. Project Relay aims to reduce the total human time to an accepted edit: finding it, editing, reviewing, correcting, and recovering. The editor keeps creative control; a saved cut does not explain its artistic purpose.

## Intended workflow

Find → Navigate → Edit manually or review a qualified proposal → Save → Verify → Capture changes → Continue or QC

This is the intended product flow. **One live manual handoff has been demonstrated**, not the full repeated-session workflow. Automatic editorial proposals are not qualified. The current guided prototype requires active development assistance for navigation; fast standalone seeking is planned.

## High-level architecture

```text
Media
  ↓
Analysis
  ↓
Semantic Edit Plan
  ↓
Review / Approval
  ↓
Editor Adapter
  ↓
Execution
  ↓
Validation / Reconciliation
```

The analysis system is intended to produce an editor-neutral edit plan. Adapters translate that plan for supported editors, keeping core analysis independent from any one editor. Validation and reconciliation check whether the resulting project matches the plan and surface unexpected conditions.

## Current development

**Pre-alpha. One bounded guided manual-editing pilot has been demonstrated.**
Relay navigated to a candidate, fully handed control to the editor, captured the
saved manual change, recorded observed differences without inventing artistic
intent, and paused safely. The accompanying validation recorded **27/27 focused
tests passing**. Automatic proposal lifecycle checks used a simulated executor;
no live automatic editorial proposal was qualified.

An earlier blind saved-project comparison identified **eight picture-removal
spans, eight audio-removal spans, four retained detached-audio clips, and three
positive saved fade-outs**. These are observations of saved settings, not proof
of rendered sound quality or the reason for each edit.

The earlier limited deterministic Filmora workflow remains a separate bounded
qualification result, covering approved planning, guarded execution, saved-state
verification, and verified rollback. It does not establish general autonomous
editing competence or qualify the guided automatic-proposal path. Filmora 14 is
the initial guided development target; future adapters remain planned.

Repeated guided-session reliability, rapid standalone navigation, prospective
editorial decisions, and unattended completion remain unqualified. Project Relay
is not production-ready and no public beta is available. See
[Development status](docs/DEVELOPMENT_STATUS.md) for the scope of each result.

## Design principles

- Keep the core analysis and edit plan independent of a specific editor.
- Give users a chance to review proposed changes before execution.
- Use evidence to support planning and guarded execution.
- Verify editor state and expected results, including safe recovery.
- Preserve source media and stop safely when conditions are unexpected.
- Expand editor support only as adapters can be qualified.

## Roadmap

The next milestone is repeated, reliable guided editing with accurate navigation
and safe handoffs. Further goals include a fast local candidate index, searchable
detection, reviewed adaptive proposals, integrated QC, verified backups, selective
restoration, and beta testing. Filmora, DaVinci Resolve, and Adobe Premiere Pro
remain an intended longer-term adapter direction, not a support or release promise.

See the visual [Roadmap](ROADMAP.md), the [Product experience concept](docs/PRODUCT_EXPERIENCE.md),
and the [Changelog](CHANGELOG.md). Milestones will be updated as evidence changes;
there are no speculative completion dates.

## Project documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Development status](docs/DEVELOPMENT_STATUS.md)
- [Product experience concept](docs/PRODUCT_EXPERIENCE.md)
- [Editor adapters](docs/EDITOR_ADAPTERS.md)
- [Qualification strategy](docs/QUALIFICATION_STRATEGY.md)
- [Safety and validation](docs/SAFETY_AND_VALIDATION.md)
- [Security](SECURITY.md)

## Availability

Project Relay is in pre-alpha development. It is not currently presented as a production-ready product or public download.

## Trademarks

Filmora, DaVinci Resolve, and Adobe Premiere Pro are trademarks of their respective owners. Project Relay is not affiliated with or endorsed by their respective owners.
