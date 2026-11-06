# PR presentation

Start every PR body with `# Before and after`, above intent, implementation detail, test logs, and pipeline output.
Compare the final branch against its actual PR base, covering the full change rather than only the last commit.

For visual changes, put real before and after screenshots side by side in a Markdown table, followed immediately by a short video showing the changed flow working.
Use the same route, viewport, representative data, and interaction state where comparable; label the captured revisions and any unavoidable differences.
For a new screen with no predecessor, state that in the Before cell instead of inventing an image.
Capture from the real built app with isolated profiles on the review machine required by the project or owner, follow its cleanup rules, and run the required UI quality check.
Publish approved evidence through the approved reviewer-accessible evidence path; verify screenshots render and the video link works in the PR.
Never substitute generated mockups, localhost links, private filesystem paths, or invented attachment URLs for evidence.
If a capture is unavailable, state exactly what is missing and why at the top; leave visual verification incomplete rather than silently using the nonvisual format.

For nonvisual changes, use a short Before/After table or two short paragraphs describing the concrete behavior, rule, or interface that changed.
Do not add screenshots or a video when nothing visual changed.
Keep implementation details and validation below the comparison; preserve the gate's owned evidence and attestation blocks.

Include this presentation requirement and the evidence locations in the gate intent before starting the run.
Use the bundled [PR template](../../../.github/pull_request_template.md) through the engine's supported `pr.template` configuration when available.
Templates are read from the trusted default branch; adding one only to a feature branch does not activate it for that same run.
Do not edit a pipeline-owned worktree or overwrite protected PR blocks to rearrange the body.
When the installed engine cannot apply the template yet, prepare the comparison as a draft and report that activation is pending; do not claim universal engine enforcement.
