# Architecture

Project Relay is designed around an editor-neutral analysis flow with editor-specific adapters. This overview is intentionally high-level.

## Analysis layer

The analysis layer examines existing media and identifies meaningful content and candidate edits. Its intended output is independent of the target editor.

## Semantic edit plan

Analysis is represented as a semantic edit plan: a description of proposed changes and their relationships, rather than a sequence tied to one editor's interface. The plan is intended to be reviewable before execution.

## Audio and editorial ownership

Acoustic observations and editorial ownership answer different questions. Evidence about what is audible is kept distinct from evidence about which video or audio contribution belongs in the edit. Project-bound ownership evidence informs planning and execution; unresolved ownership or other uncertainty can keep an operation gated for review.

## Editor adapter abstraction

An adapter translates the shared edit plan into operations for a particular editor and reports relevant state. This boundary allows the core analysis system to remain vendor-neutral while editor-specific behavior is developed and qualified separately.

Filmora is the first adapter. A limited deterministic workflow has completed live qualification in pre-alpha; broader operation coverage and qualification remain in progress. DaVinci Resolve and Adobe Premiere Pro adapters are planned for future development only. Additional adapters may be considered as the architecture and qualification work mature.

## Evidence-bound execution

The execution layer applies approved plan operations through guarded adapter actions when required project-bound evidence and expected editor states are available. Expected dialog states, such as opening or saving a project under a new name, are part of the workflow model. If conditions are uncertain or diverge from expectations, execution can stop and request review.

## Verification, reconciliation, and recovery

After execution, the saved project is checked against expected outcomes. Reconciliation identifies differences, including unexpected changes to unrelated timeline contributions. Mutation journaling supports recovery, and rollback is treated as successful only when its result is verified. These capabilities have been demonstrated for the limited qualified Filmora subset; broader coverage remains in qualification.

## Failure handling

Unexpected conditions should be surfaced, and execution should stop safely when continuing could produce an unreliable result. Validation, failure detection, recovery, and repeatability remain active development and qualification areas.

## Future directions

The adapter boundary is intended to support future editor integrations. A native media-processing backend is also a possible future direction. Neither additional integrations nor a native backend are represented as current capabilities.
