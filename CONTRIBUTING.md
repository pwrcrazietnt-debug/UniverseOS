# Contributing to UniverseOS

Thanks for considering a contribution.

UniverseOS is at an early planning stage. The most useful contributions right now are architecture research, careful documentation, small prototypes, and reproducible tests.

## Before starting

1. Read the [README](README.md), [architecture](docs/ARCHITECTURE.md), and [roadmap](docs/ROADMAP.md).
2. Read [COMMUNITY.md](COMMUNITY.md) for ways to contact the project lead and participate.
3. Search existing issues and discussions.
4. For major design changes, open an issue first so the community can discuss the trade-offs.
5. Avoid building against an unapproved assumption about the base distribution or runtime interface.

## Contribution expectations

- Be respectful and constructive.
- Explain what problem a change solves.
- Prefer small, reviewable pull requests.
- Include tests for code changes and update documentation when behavior changes.
- State hardware, OS, runtime, and version details for test results.
- Distinguish measured results from estimates.
- Never claim compatibility based on file detection or successful extraction alone.
- Do not submit proprietary application binaries, copyrighted assets, credentials, or material you do not have permission to distribute.

## Pull request checklist

- [ ] The change has a clear purpose.
- [ ] Relevant tests pass, or the PR explains why tests are unavailable.
- [ ] Documentation is updated.
- [ ] Security and permission implications are described.
- [ ] Compatibility claims include reproducible test details.
- [ ] Dependencies and licenses are identified.

## Code style

Project-specific style guides will be added when implementation languages and tooling are selected. Until then, use the formatter and linter recommended by the relevant upstream project.

## Reporting compatibility

Include:
- Application name and version.
- Package format and source.
- CPU architecture and GPU.
- UniverseOS build and runtime versions.
- Steps to reproduce.
- Expected and observed behavior.
- Relevant logs with personal information and secrets removed.
