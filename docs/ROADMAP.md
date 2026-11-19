# UniverseOS Roadmap

This roadmap is directional. Items are not complete until code, tests, and documentation demonstrate the result.

## Phase 0 — Project foundation
- [x] Create repository and initial documentation.
- [x] Record project scope and compatibility caveats.
- [x] Record initial privacy-first principles.
- [x] Choose a minimal built-in desktop as the default experience.
- [ ] Choose a license after community discussion.
- [ ] Set up issue templates and project discussions.
- [ ] Agree on contribution and review process.

## Phase 1 — Architecture decisions
- [ ] Compare candidate Linux base distributions.
- [ ] Choose desktop toolkit and compositor for the minimal built-in desktop.
- [ ] Define optional module format, dependency model, and removal behavior.
- [ ] Define first-boot Minimal, Balanced, and Custom installation profiles.
- [ ] Define supported hardware and CPU architecture for the first prototype.
- [ ] Define application metadata schema.
- [ ] Define runtime adapter interface.
- [ ] Write threat model and package-install security requirements.
- [ ] Define telemetry-free defaults, network endpoint inventory, and privacy review process.

## Phase 2 — Minimal bootable prototype
- [ ] Produce a reproducible bootable image.
- [ ] Boot on a documented x86_64 test machine.
- [ ] Provide networking, storage, audio, and graphics basics.
- [ ] Provide a minimal built-in desktop and first-boot setup.
- [ ] Make optional components opt-in and show dependencies before installation.
- [ ] Add system update and rollback strategy.
- [ ] Publish build instructions and checksums.

## Phase 3 — Native application experience
- [ ] Build format identification library.
- [ ] Implement safe archive inspection.
- [ ] Integrate native package management.
- [ ] Build a basic application library UI.
- [ ] Add install confirmation, logs, and uninstall flow.
- [ ] Add automated tests for malformed and unexpected packages.

## Phase 4 — Privacy and security controls
- [ ] Verify that no advertising ID, ad SDK, or advertising service is included.
- [ ] Audit services and packages for telemetry and unexpected network traffic.
- [ ] Ensure optional diagnostics are off by default and require informed consent.
- [ ] Build a privacy dashboard for app permissions, background services, and network activity.
- [ ] Document data flows, update endpoints, and third-party component behavior.
- [ ] Publish a threat model and security review process.

## Phase 5 — Windows compatibility
- [ ] Prototype a managed Wine prefix.
- [ ] Define runtime installation and update policy.
- [ ] Add per-app compatibility metadata.
- [ ] Test a small, legally obtained application suite.
- [ ] Document unsupported cases and known limitations.

## Phase 6 — Android compatibility
- [ ] Evaluate Android runtime options.
- [ ] Prototype on supported hardware.
- [ ] Test input, graphics, audio, networking, and lifecycle integration.
- [ ] Document service and app compatibility limits.

## Phase 7 — Experimental macOS research
- [ ] Document technical and legal constraints.
- [ ] Identify a narrowly scoped, lawful research target.
- [ ] Publish findings before proposing an implementation.
- [ ] Do not advertise general macOS application support without a working, lawful, tested runtime.

## Phase 8 — Community-ready release
- [ ] Automated build and test pipeline.
- [ ] Hardware compatibility reports.
- [ ] Signed release artifacts and verification instructions.
- [ ] Installation, recovery, and troubleshooting documentation.
- [ ] Security response and supported release policy.

## How to contribute to the roadmap

Open an issue with the problem, proposed outcome, alternatives considered, risks, and a test plan. Large changes should begin with an architecture discussion.
