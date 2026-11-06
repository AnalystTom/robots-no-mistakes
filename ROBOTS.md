# Robots No Mistakes

Maintained by AnalystTom, with upstream credit to Kun Chen.
This is a public independent derivative repository, not a claim to original authorship or an upstream-endorsed release.

## What changed

- [robots-check](skills/robots-check/SKILL.md)

The profile favors a specific requested outcome, remembered decisions, bounded clarification, and evidence that separates tested, merged, and live.
The runtime engines are unchanged.
Existing active skills, Robostrator homes, and the installed no-mistakes binary have not been replaced.

## Use and edit

Open a fresh task and ask the agent to read the linked Robots skill for the task you want to perform.
Edit those files in this repository and review their behavior on the scenarios in the Robots Skills repository before rollout.
For a durable installation, select only the desired Robots skill directories in your harness's supported skill installer; avoid installing a second copy of every upstream skill.
Do not point an active Robostrator home or production gate at this checkout without a separate migration and isolated smoke test.

## Provenance and updates

- Upstream: https://github.com/kunchenguid/no-mistakes
- Starting commit: `6aa19b15791994c27660f792d01a275fcf0070d6`.
- Snapshot fetched: 2026-11-04 UTC.
- Original licence: [LICENSE](LICENSE).
- Owner repository: https://github.com/AnalystTom/robots-no-mistakes

`origin` points to the AnalystTom repository and `upstream` points to the original project.
The public repository starts with fresh Git history; original revisions are recorded in [NOTICE.md](NOTICE.md), and the old repository is retained as a private archive.
Review upstream updates on a branch and rerun the relevant checks before adopting them.
Keep upstream notices and names in their original code; robot branding lives in the user-facing profile, not renamed binary interfaces.

## PR presentation

The [presentation policy](skills/robots-check/references/pr-presentation.md) puts a before/after comparison first, with real screenshots and a short video for visual changes, or a concrete text comparison for nonvisual changes.
The bundled template is selected in this repository's `.no-mistakes.yaml`; the engine reads it from the trusted default branch. The same template is available to GitHub's PR editor.
To adopt it in another project, copy the template there and select that repository-relative file through `pr.template` on its trusted default branch.
The driver skill carries the same requirement into gate intent; this is a workflow policy using the upstream engine, not a new binary-level enforcement check.

## Validation boundary

Skill structure and document links can be checked mechanically.
That does not establish model behavior or a lower failure rate.
The scenario set is a calibration starting point, not a benchmark result.

## Public source edition

Build with `make build`; the resulting executable stays under `bin/` until you explicitly install it. Do not run `make install` against an active shared daemon as part of a source review. Existing upstream installers and `no-mistakes update` still refer to upstream distribution; do not use them for this edition.

Default source builds leave telemetry destinations empty. Existing explicit environment or `.env` overrides still apply. Release publishing and Pages deployment are opt-in (`ROBOTS_PUBLISH_RELEASES` and `ROBOTS_PUBLISH_DOCS` repository variables), after independent signing and hosting are configured. Tests and docs builds run without those publishing flags.

The generated `no-mistakes` skill includes the evidence-first instruction. To use the template in another project, copy `.github/pull_request_template.md` to that project, set `pr.template: .github/pull_request_template.md` and `pr.appendix: collapsed` in its `.no-mistakes.yaml`, and land both on its trusted default branch. Template filling is agent-driven; reviewers still verify the media and its accuracy.
