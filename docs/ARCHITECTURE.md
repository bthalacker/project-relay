# Architecture

Project Relay is designed around an editor-neutral analysis flow with editor-specific adapters. This overview is intentionally high-level.

## Analysis layer

The analysis layer examines existing media and identifies meaningful content and candidate edits. Its intended output is independent of the target editor.

## Candidate indexing and navigation — planned separation

Heavy media analysis should produce reusable candidate locations ahead of
interaction. A local index and deterministic navigation path are planned so an
interactive jump need not wait for another AI reasoning cycle. Low-latency search
and reliable standalone jumps are not demonstrated product capabilities.

## Semantic edit plan

Analysis is represented as a semantic edit plan: a description of proposed changes and their relationships, rather than a sequence tied to one editor's interface. The plan is intended to be reviewable before execution.

## Audio and editorial ownership

Acoustic observations and editorial ownership answer different questions. Evidence about what is audible is kept distinct from evidence about which video or audio contribution belongs in the edit. Project-bound ownership evidence informs planning and execution; unresolved ownership or other uncertainty can keep an operation gated for review.

## Editor adapter abstraction

An adapter translates the shared edit plan into operations for a particular editor and reports relevant state. This boundary allows the core analysis system to remain vendor-neutral while editor-specific behavior is developed and qualified separately.

Filmora is the first adapter. A limited deterministic workflow has completed live qualification in pre-alpha; broader operation coverage and qualification remain in progress. DaVinci Resolve and Adobe Premiere Pro adapters are planned for future development only. Additional adapters may be considered as the architecture and qualification work mature.

## Evidence-bound execution

The execution layer applies approved plan operations through guarded adapter actions when required project-bound evidence and expected editor states are available. Expected dialog states, such as opening or saving a project under a new name, are part of the workflow model. If conditions are uncertain or diverge from expectations, execution can stop and request review.

## Guided human control and approval

The intended guided flow separates candidate detection, editor navigation,
human control, saved-result verification, and approval. One bounded manual
handoff has been demonstrated: navigate, yield control, accept the user's saved
edit, record observed differences, and pause. Navigation currently requires
development assistance; repeated-session reliability remains unqualified.

Automatic proposals require separate qualification and human confirmation.
An original proposal and a later human correction must remain distinct evidence.
Recorded observations can inform tested rules but cannot establish artistic
intent, grant future editorial permission, or automatically retrain a model.

## Verification, reconciliation, and recovery

After execution, the saved project is checked against expected outcomes. Reconciliation identifies differences, including unexpected changes to unrelated timeline contributions. Mutation journaling supports recovery, and rollback is treated as successful only when its result is verified. These capabilities have been demonstrated for the limited qualified Filmora subset; broader coverage remains in qualification.

## Failure handling

Unexpected conditions should be surfaced, and execution should stop safely when continuing could produce an unreliable result. Validation, failure detection, recovery, and repeatability remain active development and qualification areas.

## Future directions

The adapter boundary is intended to support future editor integrations. A native media-processing backend is also a possible future direction. Neither additional integrations nor a native backend are represented as current capabilities.
