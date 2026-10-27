# Editor adapters

Project Relay is intended to keep its analysis and semantic edit plan independent of a specific video editor. Editor adapters translate that shared plan into editor-specific operations where practical.

| Editor | Status |
| --- | --- |
| Wondershare Filmora | First adapter. Limited deterministic workflow live-qualified in pre-alpha; broader operation coverage and qualification remain in progress. |
| DaVinci Resolve | Planned for future adapter development only. |
| Adobe Premiere Pro | Planned for future adapter development only. |

The Filmora qualification covers a defined subset of planning, guarded execution, saved-project verification, and recovery. It does not imply general support for all Filmora editing or autonomous artistic decisions. Planned editors are not currently supported and are not release-date commitments. Adapter availability depends on implementation and qualification.

## Current QC/native boundary

Preview-first review can run without navigating Filmora. Inspect and manual
correction require a fresh verified native landing. Earlier bounded single-seek
checks passed; later difficult navigation took 77–107 seconds and required
multiple bounded candidates. Low-latency navigation remains unqualified.

Supported source audio simulations do not imply native audio Apply support.
One tiny native export exposed a saved-geometry/render discrepancy; the cause
and corrective mapping remain open. Adapter qualification must therefore include
rendered evidence as well as saved structure. See the
[October 27 milestone](QA_MILESTONE_2026-10-27.md).
