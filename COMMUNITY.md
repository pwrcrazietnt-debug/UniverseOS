# UniverseOS Community

**Want to help build UniverseOS? You're welcome here.**

UniverseOS is an open-source project exploring a lightweight, highly customizable, privacy-first desktop operating system that brings multiple application ecosystems together under one consistent experience.

## What is UniverseOS?

The goal is to build an operating system that gives people control over their computer instead of forcing everyone into the same heavy setup.

UniverseOS is planned around a Linux foundation, with a small built-in graphical desktop that makes the computer usable right after installation. The core desktop should stay lightweight and provide the essentials: launching applications, managing settings, connecting to networks, handling updates, and controlling permissions.

Beyond that small core, users should choose what they want:
- **Desktop environments:** keep the built-in desktop or add another supported desktop environment.
- **Application ecosystems:** native Linux applications first, with optional Windows compatibility through technologies such as Wine/Proton and an Android runtime based on established projects.
- **Optional tools:** gaming, development, multimedia, accessibility, and other feature groups can be installed separately.
- **Custom setup:** an installer should explain what each option does, its dependencies, approximate storage needs, and any additional services or network access before asking the user to install it.

The long-term ambition is to make installing and managing applications from different ecosystems feel consistent. Compatibility will be tested and reported honestly. Recognizing a Windows, Android, or macOS package does not automatically mean its application can run. macOS compatibility is particularly experimental and is not promised.

## Privacy is a core requirement

UniverseOS aims to be privacy-first by design:
- No operating-system advertising ID.
- No built-in advertising, ad profiling, or ad SDKs.
- No non-essential telemetry enabled by default.
- No mandatory cloud account for ordinary local use.
- No hidden data collection or unexplained background connections.
- Local-first storage and clear app permissions.
- Transparent update and network behavior.
- Optional diagnostics only with informed user consent.

These are project requirements we intend to implement and verify, not claims that a finished OS already exists. Read [PRIVACY.md](PRIVACY.md) for the current principles and limitations.

## What can you help with?

You do not need to be an expert or write code to contribute. We're interested in help with:

- **Linux and systems engineering:** boot process, drivers, services, packaging, and system integration.
- **Desktop and UI design:** layouts, accessibility, themes, settings, and installer experience.
- **Privacy and security:** threat modeling, permission design, audits, and safe defaults.
- **Application compatibility:** researching runtimes, testing applications, and documenting results.
- **Testing:** hardware reports, bug reproduction, performance measurements, and usability feedback.
- **Documentation and community:** guides, diagrams, translations, issue triage, and helping new contributors.

## Project status

UniverseOS is currently in its early planning and repository-scaffolding stage. It is **not yet a bootable operating system**, and its planned desktop and compatibility runtimes are not implemented. The project needs architecture research, prototypes, tests, and contributors before it can become an installable OS.

You can follow development in the [GitHub repository](https://github.com/pwrcrazietnt-debug/UniverseOS), read the [roadmap](docs/ROADMAP.md), and see how to contribute in [CONTRIBUTING.md](CONTRIBUTING.md).

## Contact the project lead

You can reach the project lead on social media:

- **Instagram:** [@driftkingdropthecrown](https://www.instagram.com/driftkingdropthecrown/)
- **TikTok:** [@driftkingdropthecrown](https://www.tiktok.com/@driftkingdropthecrown)

When reaching out, introduce yourself, say what part of UniverseOS interests you, and share examples of your work if you have any. Please don't send passwords, private keys, account recovery codes, or other sensitive information.

Social media is for introductions and general coordination, not for reporting security vulnerabilities. Please use the repository's security reporting instructions for security issues.

## Contribute on GitHub

- Read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.
- Check the [roadmap](docs/ROADMAP.md) to see what's planned.
- Open an issue to suggest a feature, report a reproducible bug, or discuss an architectural decision.
- Submit a pull request for focused changes with a clear explanation and relevant tests.

## Community expectations

- Be respectful, patient, and constructive.
- Explain disagreements with evidence and alternatives.
- Respect other contributors' privacy and boundaries.
- Do not share someone else's personal information without permission.
- Keep discussions focused on making the project better.

UniverseOS is a community project: ideas and contributions are welcome, and major technical decisions should be discussed openly.
