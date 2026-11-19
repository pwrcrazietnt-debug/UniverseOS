# UniverseOS

**One operating system. Multiple application ecosystems. Privacy by design.**

UniverseOS is an open-source research and engineering project exploring a unified desktop operating system that can discover, install, launch, and manage applications from multiple ecosystems through a consistent user experience.

> **Project status: early planning / scaffold.** This repository does not yet contain a bootable operating system or working cross-platform application runtimes. Compatibility will be developed and tested incrementally. No universal-compatibility claim is made.

## Vision

Build a practical OS platform with:

- A coherent, lightweight built-in desktop, settings experience, application library, and package manager.
- Optional desktop environments and components that users can choose to install.
- Native support for Linux applications and system components.
- A Windows compatibility layer based on established projects such as Wine and, where appropriate, Proton.
- An Android application environment using established Android runtime technology.
- A macOS compatibility research track. macOS application support is especially constrained by proprietary frameworks, platform assumptions, signing, licensing, and hardware requirements; it is an investigation, not a promised feature.
- A format-aware installer that identifies packages safely, explains what they require, and routes them to the correct installer or runtime.
- A privacy-first system with no advertising ID, no advertising, and no non-essential telemetry enabled by default.

## Important distinction

Recognizing a file is not the same as running its application. For example, extracting a `.dmg` does not make a macOS app runnable on Linux. UniverseOS will report what it can actually support, what dependencies are missing, and when a format is unsupported.

## Initial technical direction

UniverseOS will begin with a Linux-based foundation rather than attempting to write a new kernel and every application runtime from scratch. This lets the project focus on integration, security, usability, privacy, and compatibility while relying on mature upstream work.

The built-in desktop will be deliberately small and usable on modest hardware. It will provide a reliable first-boot experience without forcing users into a command line. Larger desktop environments, runtimes, utilities, and feature groups will remain optional and independently manageable.

See:
- [Architecture](docs/ARCHITECTURE.md)
- [Roadmap](docs/ROADMAP.md)
- [Privacy principles](PRIVACY.md)
- [Contributing](CONTRIBUTING.md)
- [Community and contact](COMMUNITY.md)
- [Security policy](SECURITY.md)

## Guiding principles

1. **Privacy by default:** no advertising ID, advertising, or non-essential telemetry; explain and ask before optional data sharing.
2. **Honest compatibility:** never label an app as supported until it has been tested.
3. **Upstream first:** reuse and contribute to mature projects instead of unnecessarily duplicating them.
4. **Security by default:** inspect packages, isolate untrusted apps, and require consent for privileged changes.
5. **Modular design:** runtimes and format handlers should be independently maintainable and optional.
6. **Lightweight and customizable:** keep the built-in desktop lean and let users choose what else is installed.
7. **Open development:** document decisions, limitations, tests, and hardware coverage.

## Current status

| Area | Status |
|---|---|
| Project structure and design docs | Started |
| Privacy requirements | Initial principles documented |
| Bootable base system | Not started |
| Minimal built-in desktop | Planned |
| Optional desktop environments | Planned |
| Package / format detection | Not started |
| Linux application integration | Planned |
| Windows runtime integration | Research / planned |
| Android runtime integration | Research / planned |
| macOS compatibility research | Exploratory |
| Automated compatibility testing | Not started |

## Getting involved

Want to help build UniverseOS? Read [CONTRIBUTING.md](CONTRIBUTING.md), check the [roadmap](docs/ROADMAP.md), and visit [COMMUNITY.md](COMMUNITY.md) for ways to get in touch. Code, testing, documentation, design, accessibility feedback, and thoughtful issue reports are all valuable.

## Name

UniverseOS is the current project name. Branding and naming can evolve as the project develops.
