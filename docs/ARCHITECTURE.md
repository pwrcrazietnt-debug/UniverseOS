# UniverseOS Architecture

## 1. Overview

UniverseOS is planned as a Linux-based operating-system distribution with a custom integration layer and desktop experience. It is not initially a new kernel. A Linux foundation provides hardware support, drivers, security primitives, filesystems, networking, and a large native application ecosystem.

The system is divided into layers so that the base OS can remain usable even when an optional compatibility runtime is absent or broken. A small built-in desktop provides a friendly first-boot and recovery experience; larger desktop environments and feature groups are opt-in.

## 2. Layer model

```text
+------------------------------------------------------+
|          Minimal built-in Universe Desktop           |
|     shell | settings | app library | permissions     |
+------------------------------------------------------+
|            Optional desktop / feature modules        |
|       alternate desktops | tools | integrations      |
+------------------------------------------------------+
|              App discovery and management            |
|       catalog | format detection | install UX        |
+------------------------------------------------------+
|             Compatibility / execution                |
|  Linux | Windows (Wine/Proton) | Android (ART-based)  |
|                 macOS research track                  |
+------------------------------------------------------+
|              Isolation and permissions               |
|       sandboxing | portals | policies | identities   |
+------------------------------------------------------+
|              Linux distribution foundation           |
|       kernel | drivers | core services | packages    |
+------------------------------------------------------+
|                       Hardware                       |
+------------------------------------------------------+
```

This is a conceptual architecture, not an implementation diagram for existing code.

## 3. Base operating system

Initial direction:
- Linux kernel and a maintained distribution base.
- Standard Linux userspace and system service management.
- Native package management inherited from the selected base.
- Reproducible build and image-generation tooling.
- Secure boot support where feasible, with signed boot artifacts as a design goal.
- A minimal built-in desktop and essential setup/recovery tools.
- Optional components installed only after the user reviews what they add and what dependencies they require.

The base distribution has not yet been selected. That decision should be made through a documented comparison of maintenance burden, package availability, image tooling, security updates, and hardware support.

## 4. Lightweight desktop and modular installation

The built-in Universe Desktop is the default graphical experience. It should be small, accessible, and sufficient for setup, launching apps, changing settings, managing updates, and recovering from common problems.

The desktop is not intended to become a mandatory bundle of every feature. Alternate desktop environments, compatibility runtimes, gaming tools, developer tools, multimedia applications, and optional services should be separately installable and removable.

The installer and first-boot setup should:
- Offer clear Minimal, Balanced, and Custom choices.
- Explain the purpose, approximate size, dependencies, and network requirements of optional components.
- Never silently install optional runtimes or third-party services.
- Allow users to skip optional components and add them later.
- Keep a working minimal desktop if an optional module fails or is removed.

## 5. Application catalog and format detection

A format handler should identify a file by content and validated metadata, not just its filename extension. It should return a structured result containing:
- Detected format and confidence.
- Target ecosystem and architecture.
- Required runtime or installer.
- Whether the package is signed or has verifiable provenance.
- Required permissions and privileged operations.
- Supported, experimental, or unsupported status.

The detector must not execute an unknown file merely to identify it.

Examples of intended routing:
- `.deb`: native Debian-family package tooling, if compatible with the selected base.
- `.rpm`: RPM package tooling or a supported conversion/build path; never assume conversion is lossless.
- `.AppImage`: Linux application path, subject to permission and sandbox policy.
- `.flatpak`: Flatpak, if selected and configured.
- `.exe` / `.msi`: Windows compatibility runtime such as Wine; not a Windows kernel.
- `.apk`: Android runtime environment; not a native Linux executable.
- `.dmg` / `.pkg`: identify and inspect where possible; do not imply that extraction enables execution. macOS app execution remains an exploratory compatibility problem.
- `.tar.gz`: generic archive until its contents and installation metadata are inspected.

## 6. Runtime adapters

Each ecosystem should implement a common adapter contract:
1. Detect whether the runtime is installed and healthy.
2. Validate the package type and architecture.
3. Explain dependencies and limitations before installation.
4. Install into a defined location or managed prefix.
5. Launch with explicit environment and permission policy.
6. Report exit status, logs, and compatibility metadata.
7. Support clean uninstall and runtime updates.

### Linux

Linux is the first target for native application support. The selected distribution's package manager remains authoritative for system packages. User applications should use a managed application path where possible.

### Windows

Investigate Wine and Proton rather than reimplementing Windows APIs. Compatibility depends on the app, graphics stack, architecture, libraries, anti-cheat, DRM, and version. Some software will not work.

### Android

Investigate established Android runtime approaches, including ART-based environments and containerized integration. Hardware acceleration, Google services, device APIs, app integrity checks, and licensing can affect support.

### macOS

This is a research-only track. macOS apps can depend on Darwin/XNU behavior, Apple frameworks, code signing, entitlements, proprietary services, and Apple-specific hardware. File extraction or API stubs are not equivalent to a supported runtime. Any work must respect applicable licenses and platform restrictions.

## 7. Security and privacy model

Security and privacy are architectural requirements, not marketing claims.

- Never run installers automatically after detection.
- Separate package inspection from installation and execution.
- Require explicit user approval for privileged operations.
- Prefer per-application isolation and least privilege.
- Keep runtime prefixes and app data separate from the base OS.
- Verify signatures and hashes when trustworthy metadata is available.
- Make provenance and verification status visible.
- Do not silently disable OS security controls.
- Provide clear uninstall and data-removal behavior.
- Ship without advertising IDs, ad SDKs, or advertising services.
- Disable non-essential telemetry and analytics by default; no hidden collection.
- Do not require a cloud account for ordinary local OS use.
- Keep diagnostics local by default. Any optional sharing must be clearly described, separately consented to, and easy to decline.
- Minimize network connections and document the purpose of required endpoints.
- Provide controls to inspect app permissions, background services, and network activity.

See [PRIVACY.md](../PRIVACY.md) for the detailed privacy requirements. The threat model must also document limits: installed applications, hardware firmware, network providers, and upstream components can have their own data practices. UniverseOS must not claim that it can guarantee privacy beyond the controls it can verify.

Sandboxing is a design requirement, not a claim that every proposed runtime is already safely sandboxed.

## 8. Desktop experience

The built-in desktop should provide:
- A lightweight shell with launcher, settings, status area, and basic window management.
- A unified application library with ecosystem and compatibility labels.
- Clear install, launch, update, and uninstall flows.
- Runtime health and dependency reporting.
- Permission prompts with understandable explanations.
- Search across installed apps and available catalogs.
- A fallback path to native package tools for advanced users.
- A privacy dashboard for permissions, background services, and network activity.

The desktop must not hide ecosystem differences that affect reliability or security.

## 9. Hardware and architecture strategy

The first development target should be x86_64 PCs. ARM64 can be considered after the build and runtime model is stable. GPU acceleration and graphics translation should use established upstream components wherever possible.

Low-resource operation is a goal, but performance claims must be backed by repeatable measurements on documented hardware.

## 10. Decisions still open

These decisions require issues and documented trade-off discussions:
- Base distribution and release model.
- Desktop toolkit and compositor.
- Package catalog and metadata format.
- Default sandbox technology.
- Update and rollback design.
- Image build and installation system.
- Minimum hardware requirements.
- Supported CPU architectures.
