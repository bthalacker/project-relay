# Project Relay

**Development codename:** Project Relay  
**Status:** Pre-alpha · active development  
**Development version concept:** `0.0.1-dev`

Project Relay is a vendor-neutral video editing automation platform in development. It is intended to analyze existing media, create semantic edit plans, carry out approved plans through editor-specific adapters, and verify the results.

Project Relay is a development codename, not the final commercial product name or a trademark claim.

## The problem

Repetitive and precision-sensitive edits can take substantial time and are easy to apply inconsistently. Project Relay aims to help automate this work while keeping people in control of what changes: users should be able to review proposed edits before execution and verify the outcome afterward.

## Intended workflow

Import media → Analyze → Review proposed edits → Execute → Verify → Complete

This is a long-term product direction. The complete graphical workflow does not exist yet, and the GUI is not currently the primary production interface.

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

**Pre-alpha. Active development. A limited deterministic Filmora workflow has completed live qualification through planning, guarded execution, saved-project verification, and verified rollback.** Filmora is the first adapter; broader operation coverage and qualification remain in progress. DaVinci Resolve and Adobe Premiere Pro adapters are planned for future development.

The qualified subset uses project-bound video/audio ownership evidence and distinguishes acoustic observations from editorial audio ownership. It supports frame-accurate, source-bound structural planning where evidence permits, expected Open and Save As dialog states, and reviewed audio transitions whose durations derive from overlap geometry. Uncertain cases remain gated for review. More than 200 automated regression checks are currently passing.

This progress does not mean all Filmora editing is supported, that artistic decisions are automated, or that the product is production-ready. Continued work focuses on broader coverage, generalization, audio preservation, and end-to-end reliability.

## Design principles

- Keep the core analysis and edit plan independent of a specific editor.
- Give users a chance to review proposed changes before execution.
- Use evidence to support planning and guarded execution.
- Verify editor state and expected results, including safe recovery.
- Preserve source media and stop safely when conditions are unexpected.
- Expand editor support only as adapters can be qualified.

## Roadmap

Current priorities include broadening structural-edit coverage, completing remaining audio ownership and preservation decisions, expanding end-to-end qualification, improving generalization and review handling, and continuing safety and recovery qualification. The intended 1.0 goal includes Filmora, DaVinci Resolve, and Adobe Premiere Pro adapters; these are goals, not commitments or release-date promises.

See [ROADMAP](ROADMAP.md) for milestones and [CHANGELOG](CHANGELOG.md) for a high-level development summary.

## Project documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Development status](docs/DEVELOPMENT_STATUS.md)
- [Editor adapters](docs/EDITOR_ADAPTERS.md)
- [Qualification strategy](docs/QUALIFICATION_STRATEGY.md)
- [Safety and validation](docs/SAFETY_AND_VALIDATION.md)
- [Security](SECURITY.md)

## Availability

Project Relay is in pre-alpha development. It is not currently presented as a production-ready product or public download.

## Trademarks

Filmora, DaVinci Resolve, and Adobe Premiere Pro are trademarks of their respective owners. Project Relay is not affiliated with or endorsed by their respective owners.
