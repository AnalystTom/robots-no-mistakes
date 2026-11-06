---
name: robots-check
description: Prepare and drive a no-mistakes validation with preserved intent and honest evidence. Use when shipping Robots changes through the installed gate.
---

# Robots Checkpoint

This is a workflow profile over the installed no-mistakes engine, not a new engine or a guarantee of zero defects.
Read the installed no-mistakes skill and live AXI help for that binary's exact commands.
The source checkout and installed binary may be different versions; do not apply flags from a newer checkout to an older daemon.
Never update or restart the shared daemon as an incidental prerequisite.

## Before the gate

Inspect repository status, current branch, intended base, publishing target, and existing run ownership.
Preserve unrelated edits and pipeline-authored commits.
Carry the user's original objective, later corrections, accepted tradeoffs, and explicit exclusions into the intent.
Provide the observable acceptance check and known environment limits separately when the installed version supports it.
Do not rewrite the objective as a list of changed files.

Read the project's scripts and perform the required deterministic checks.
Prefer behavioral regressions at real boundaries to tests that grep source or prompt wording.
A scenario that requires unavailable authentication is untested; a mock does not make it live-tested.
Use account sign-in or existing authorized credentials through the supported tool, never a pasted-key request.

Run the required Ponytail review once before publication where the project requires it.
Use the gate as the owner of its own review, fixes, tests, documentation, push, PR, and CI phases.
Do not add redundant serial review rounds unless the user or repository specifically requires them.

## During the gate

Follow its actual findings and next-action output.
Resolve routine mechanical findings within existing authority.
For a finding that challenges accepted intent, cite the existing decision when the gate supports clarification; escalate a genuinely new decision once.
Never blanket-approve ask-user findings, weaken checks, or report an override as a clean pass.

When the run holds the branch, let its supported fix or synchronization operation perform the change.
Do not edit its worktree from outside, reset history, discard private commits, or start a replacement run to escape custody.
A slow running step and a parked decision are different states; inspect the current run before deciding recovery.

Do not repeat an unchanged pending question after every wake.
Retain the required supervision path and report again when the state changes or the user requests status.

## Delivery

Use [the PR presentation policy](references/pr-presentation.md) when preparing the intent, collecting evidence, and drafting or updating a PR.
Report the exact terminal outcome, including skips, overrides, failures, or untested scenarios.
Verify head/base and host mergeability immediately before calling the PR ready.
For UI changes, require the available UI quality check, screenshots, and a short video from the real built app, with working reviewer-accessible links.
A passed gate or merged PR does not prove a deployment.
Only claim live after checking the deployed revision and the exact requested production behavior, within the user's deployment authorization.
