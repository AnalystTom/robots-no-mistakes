# Robots No Mistakes 🤖

Your robot checkpoint for software changes. Maintained by **AnalystTom**, adapted from [No Mistakes by Kun Chen](https://github.com/kunchenguid/no-mistakes).

Give the agent a task, validate the change, and review a PR that shows the result first. You are the **Boss**: the gate reports what was checked, what failed, and what still needs your decision.

## Evidence first

Every PR starts with **Before and after**:

- **Visual changes:** real before/after screenshots side by side, followed by a short video of the changed flow working.
- **Nonvisual changes:** a simple text comparison explaining exactly what changed.
- Missing evidence is stated at the top. No invented screenshots, tests or approvals.

Implementation details and the gate's validation appendix follow the comparison. The [policy](skills/robots-check/references/pr-presentation.md), [PR template](.github/pull_request_template.md), and [Robots Checkpoint skill](skills/robots-check/SKILL.md) carry this workflow.

## Start from source

```sh
git clone https://github.com/AnalystTom/robots-no-mistakes.git
cd robots-no-mistakes
make build
./bin/no-mistakes --help
```

Use the Go version specified in [go.mod](go.mod). This is a source edition; there are no Robots-signed binary releases yet. Do not use the inherited upstream installers or self-update command to install this edition. Build locally without replacing an active shared daemon.

Read the [Robots guide](ROBOTS.md) for installation boundaries and how to adopt the evidence template in another project. The inherited command name, Go module path, configuration files and protocol identifiers remain compatible with upstream.

## Development

```sh
make lint
make test
make build
```

`make lint` checks generated files and runs Go vet. `make test` runs the race-enabled Go suite. CI checks formatting and tests across supported platforms. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Credit and ownership

This repository starts with a fresh Git history of adapted upstream source. It is an independent derivative, not a claim that the original implementation was written from scratch or endorsed by its author.

Kun Chen's original copyright and [MIT licence](LICENSE) remain intact. [NOTICE.md](NOTICE.md) records the source revisions and AnalystTom's adaptations. The [inherited reference documentation](docs/src/content/docs/) describes the compatible engine; upstream distribution and signing instructions are historical references, not Robots release instructions.
