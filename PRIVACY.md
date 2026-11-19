# UniverseOS Privacy Principles

**Privacy is a default system property, not a premium feature or an account setting.**

This document records the project's intended requirements. It is not a claim that the current repository or a released operating system already implements them.

## Non-negotiable defaults

1. **No advertising ID.** UniverseOS will not create or expose an OS-level advertising identifier.
2. **No advertising.** The operating system will not include ad networks, ad SDKs, sponsored placements, or behavioral ad profiling.
3. **No non-essential telemetry by default.** Usage analytics, crash uploads, diagnostics uploads, and product-improvement reporting must be disabled unless a user explicitly opts in after a clear explanation.
4. **No mandatory cloud account.** Ordinary local use, setup, and system administration must not require a UniverseOS account.
5. **No hidden data collection.** Data collection and network behavior must be documented, reviewable, and limited to a stated purpose.
6. **Local-first operation.** Personal files, settings, and app data remain on the device unless the user chooses a network-backed feature or sharing action.

## Network behavior

- Maintain a public inventory of first-party network endpoints and explain why each exists.
- Avoid background connections that are not needed for a user-requested or essential system function.
- Make update checks configurable without compromising security updates; clearly explain the trade-off when users disable them.
- Do not sell, rent, or share user data for advertising.
- Optional diagnostics must be separate from essential update and security infrastructure.
- Do not silently enable cloud sync, remote backups, or account-linked services.

## Permissions and transparency

- Apps should receive only the permissions they need.
- Sensitive permissions should be understandable, visible, and revocable where technically possible.
- Provide a dashboard showing app permissions, background services, and network activity.
- Explain what optional modules install, their dependencies, their approximate size, and whether they add services or network connections.
- Give users a clear way to uninstall optional modules and remove associated data, with a confirmation when removal is destructive.

## Open source and verification

- Keep privacy-relevant system components open to public review.
- Document third-party components and inherited defaults, including telemetry behavior.
- Audit packages, services, and network traffic before releases.
- Prefer reproducible builds and signed release artifacts as the project matures.
- Publish known limitations and privacy review findings rather than making unverifiable "perfect privacy" claims.

## Threat-model boundaries

An operating system cannot automatically control every data practice of software a user installs, websites they visit, network providers, hardware firmware, or upstream services. UniverseOS should isolate applications where practical, explain these boundaries, and avoid claiming that the OS can guarantee anonymity or prevent all tracking.

## Change control

Any proposal to add telemetry, advertising-related code, cloud accounts, analytics, or new background network behavior must include:
- The exact data involved.
- The purpose and recipients.
- Whether it is required for core operation.
- How users are informed and how they can decline.
- Security and privacy risks.
- A review discussion before merge.

A proposal that adds an advertising ID or behavioral advertising is out of scope for UniverseOS.
