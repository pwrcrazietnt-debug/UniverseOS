# UniverseOS

**One operating system. Multiple application ecosystems.**

UniverseOS is an open-source research and engineering project exploring a unified desktop operating system that can discover, install, launch, and manage applications from multiple ecosystems through a consistent user experience.

> **Project status: early planning / scaffold.** This repository does not yet contain a bootable operating system or working cross-platform application runtimes. Compatibility will be developed and tested incrementally. No universal-compatibility claim is made.

## Vision

Build a practical OS platform with:

- A coherent desktop, settings experience, application library, and package manager.
- Native support for Linux applications and system components.
- A Windows compatibility layer based on established projects such as Wine and, where appropriate, Proton.
- An Android application environment using established Android runtime technology.
- A macOS compatibility research track. macOS application support is especially constrained by proprietary frameworks, platform assumptions, signing, licensing, and hardware requirements; it is an investigation, not a promised feature.
- A format-aware installer that identifies packages safely, explains what they require, and routes them to the correct installer or runtime.

## Important distinction

Recognizing a file is not the same as running its application. For example, extracting a `.dmg` does not make a macOS app runnable on Linux. UniverseOS will report what it can actually support, what dependencies are missing, and when a format is unsupported.

## Initial technical direction

UniverseOS will begin with a Linux-based foundation rather than attempting to write a new kernel and every application runtime from scratch. This lets the project focus on integration, security, usability, and compatibility while relying on mature upstream work.

See:
- [Architecture](docs/ARCHITECTURE.md)
- [Roadmap](docs/ROADMAP.md)
- [Contributing](CONTRIBUTING.md)
- [Security policy](SECURITY.md)

## Guiding principles

1. **Honest compatibility:** never label an app as supported until it has been tested.
2. **Upstream first:** reuse and contribute to mature projects instead of unnecessarily duplicating them.
3. **Security by default:** inspect packages, isolate untrusted apps, and require consent for privileged changes.
4. **Modular design:** runtimes and format handlers should be independently maintainable.
5. **Open development:** document decisions, limitations, tests, and hardware coverage.
6. **Accessible hardware targets:** keep the base system efficient and make optional features opt-in.

## Current status

| Area | Status |
|---|---|
| Project structure and design docs | Started |
| Bootable base system | Not started |
| Desktop shell | Not started |
| Package / format detection | Not started |
| Linux application integration | Planned |
| Windows runtime integration | Research / planned |
| Android runtime integration | Research / planned |
| macOS compatibility research | Exploratory |
| Automated compatibility testing | Not started |

## Getting involved

Start with the roadmap and open an issue to propose a feature, report a concern, or volunteer for a subsystem. Please discuss major architectural changes before building large dependent components.

## Name

UniverseOS is the current project name. Branding and naming can evolve as the project develops.
