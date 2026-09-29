# Qualification strategy

Project Relay is in pre-alpha. This document describes the intended qualification methodology, not a claim that every step is complete or that any adapter is production-ready.

## Establish a human-reviewed reference

For each qualification campaign, define the editing task and expected result before running automation. Use a human-reviewed gold standard so comparisons are based on an agreed interpretation of the media and intended edits. Use material that is appropriate and cleared for the test and any planned public demonstration.

## Qualify against known material

Use a controlled set of known cases to establish a baseline. Record the project version, relevant configuration, expected outcomes, and observed results for each run. Keep the case definitions stable while evaluating a build; if the system or criteria change, begin a separately identified run.

## Keep a holdout set

Evaluate previously unseen media separately from material used during development. Do not tune behavior against holdout outcomes and then report those same outcomes as independent validation. Review rules for dependencies on specific titles, scenes, filenames, or other content-specific cues; such rules do not demonstrate generalization.

## Classify failures

When an outcome differs from the reference, record the high-level failure category and whether the system detected it and stopped safely. Useful categories include semantic detection, edit timing, audio/video correctness, editor execution, result verification, and recovery. A detected mismatch or safe stop should remain visible as a qualification result rather than being counted as a successful edit.

## Repeat from clean baselines

Restore a clean project state between repeat runs and use the same defined inputs and configuration. Compare results across runs to assess repeatability. Investigate unexpected differences before treating a workflow as qualified.

## Extend qualification across editors

Where practical, use the same editor-neutral edit-plan cases to qualify each adapter. Filmora is the first adapter under development and qualification. DaVinci Resolve and Adobe Premiere Pro adapters are planned; cross-editor qualification can happen only when those adapters exist and are ready to evaluate.

## Qualification decisions

Set acceptance criteria before a campaign begins. Describe which cases were run, what passed or failed, how safely detected failures were handled, and what limitations remain. Qualification should support a clear, repeatable claim about a defined workflow rather than imply broader support than the evidence shows.
