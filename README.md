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

The analysis system is intended to produce an editor-neutral edit plan. Adapters translate that plan for supported editors, keeping core analysis independent from any one editor. Validation and reconciliation are intended to check whether the resulting project matches the plan and to surface unexpected conditions.

## Current development

**Pre-alpha. Active development. Filmora is the first editor adapter under development and qualification. DaVinci Resolve and Adobe Premiere Pro adapters are planned for future development.**

Semantic media analysis and the edit-plan architecture are in place. Automated Filmora timeline interaction is under active qualification. Work emphasizes validation, reconciliation, failure detection, safe stops, automated testing, and qualification with media. These are development activities, not claims of production readiness or a public download.

## Design principles

- Keep the core analysis and edit plan independent of a specific editor.
- Give users a chance to review proposed changes before execution.
- Verify editor state and expected results.
- Preserve source media and stop safely when conditions are unexpected.
- Expand editor support only as adapters can be qualified.

## Roadmap

Near-term work focuses on qualifying Filmora automation, improving verification and recovery, and building a reliable end-to-end project workflow. The intended 1.0 goal includes Filmora, DaVinci Resolve, and Adobe Premiere Pro adapters; these are goals, not commitments or release-date promises.

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
