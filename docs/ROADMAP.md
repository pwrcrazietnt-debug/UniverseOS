# UniverseOS Roadmap

This roadmap is directional. Items are not complete until code, tests, and documentation demonstrate the result.

## Phase 0 — Project foundation
- [x] Create repository and initial documentation.
- [x] Record project scope and compatibility caveats.
- [ ] Choose a license after community discussion.
- [ ] Set up issue templates and project discussions.
- [ ] Agree on contribution and review process.

## Phase 1 — Architecture decisions
- [ ] Compare candidate Linux base distributions.
- [ ] Choose initial desktop technology.
- [ ] Define supported hardware and CPU architecture for the first prototype.
- [ ] Define application metadata schema.
- [ ] Define runtime adapter interface.
- [ ] Write threat model and package-install security requirements.

## Phase 2 — Minimal bootable prototype
- [ ] Produce a reproducible bootable image.
- [ ] Boot on a documented x86_64 test machine.
- [ ] Provide networking, storage, audio, and graphics basics.
- [ ] Add system update and rollback strategy.
- [ ] Publish build instructions and checksums.

## Phase 3 — Native application experience
- [ ] Build format identification library.
- [ ] Implement safe archive inspection.
- [ ] Integrate native package management.
- [ ] Build a basic application library UI.
- [ ] Add install confirmation, logs, and uninstall flow.
- [ ] Add automated tests for malformed and unexpected packages.

## Phase 4 — Windows compatibility
- [ ] Prototype a managed Wine prefix.
- [ ] Define runtime installation and update policy.
- [ ] Add per-app compatibility metadata.
- [ ] Test a small, legally obtained application suite.
- [ ] Document unsupported cases and known limitations.

## Phase 5 — Android compatibility
- [ ] Evaluate Android runtime options.
- [ ] Prototype on supported hardware.
- [ ] Test input, graphics, audio, networking, and lifecycle integration.
- [ ] Document service and app compatibility limits.

## Phase 6 — Experimental macOS research
- [ ] Document technical and legal constraints.
- [ ] Identify a narrowly scoped, lawful research target.
- [ ] Publish findings before proposing an implementation.
- [ ] Do not advertise general macOS application support without a working, lawful, tested runtime.

## Phase 7 — Community-ready release
- [ ] Automated build and test pipeline.
- [ ] Hardware compatibility reports.
- [ ] Signed release artifacts and verification instructions.
- [ ] Installation, recovery, and troubleshooting documentation.
- [ ] Security response and supported release policy.

## How to contribute to the roadmap

Open an issue with the problem, proposed outcome, alternatives considered, risks, and a test plan. Large changes should begin with an architecture discussion.
