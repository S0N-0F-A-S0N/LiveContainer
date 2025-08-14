# AGENTS

This file tracks outstanding issues and recommended fixes for LiveContainer.
Check items as they are addressed.

## Build & Configuration
- [ ] Vendor submodules or instruct users to run `git submodule update --init --recursive`.
- [ ] Document build prerequisites including submodule initialization, Xcode/macOS versions, and required Python packages.
- [ ] Provide `requirements.txt` for `update_json.py`.
- [ ] Parameterize Catalyst entitlements to remove hard‑coded team identifiers.
- [ ] Document and script OpenSSL build steps.
- [ ] Provide a user‑friendly setup for the 32‑bit translation layer.
- [ ] Move large binary assets (e.g., screenshots) out of Git or use Git LFS.

## Security
- [ ] Clarify security implications of codesign bypass and JIT usage; add disclaimers.
- [ ] Trim entitlement list and remove unnecessary privileges.
- [ ] Validate and sandbox tweak loading with signatures or checksums.
- [ ] Sanitize environment variables and user inputs before use.
- [ ] Enforce HTTPS and certificate validation for JIT API communications.
- [ ] Remove Safari URL overrides or enforce an allow‑list; validate stored launch URLs.
- [ ] Verify guest app bundle signatures before loading.
- [ ] Make certificate paths configurable rather than hard‑coded.
- [ ] Validate instruction parsing in `utils.m`.
- [ ] Audit permissions and remove excessive kernel entitlements.

## Code Quality & Stability
- [ ] Replace private Apple APIs with supported APIs or guard with runtime checks.
- [ ] Replace direct Mach‑O modifications with a robust library (e.g., ChOma).
- [ ] Introduce automated tests and run them in CI.
- [ ] Add linting and static analysis to CI.
- [ ] Improve error handling for network, file, and dynamic loading operations.
- [ ] Replace `abort()` and `SIGKILL` calls with graceful error handling and shutdowns.
- [ ] Enhance `dlopen` error reporting and diagnostics.
- [ ] Track and version changes to `apps.json` to avoid overwriting manual edits.

## Documentation & Community
- [ ] Split README into concise usage guide and separate developer docs; include toolchain version info.
- [ ] Summarize third‑party licenses in a top‑level file.
- [ ] Add `CONTRIBUTING.md` and `CODE_OF_CONDUCT.md`.
- [ ] Provide localized build instructions and restructure long sections.

## Repository Hygiene
- [ ] Remove `screenshots/emptyfile` and audit repository for stray artifacts.
- [ ] Handle network failures gracefully in GitHub Actions workflows.

## TweakLoader Enhancements
- [ ] Allow per‑app configuration of loaded tweaks.
- [ ] Support dependency management for tweaks.
- [ ] Improve tweak error reporting and expose diagnostics.
- [ ] Provide sandboxed or isolated tweak loading options.
- [ ] Support runtime reloading or unloading of tweaks.
- [ ] Add an in‑app UI to manage tweak loading order and enable/disable tweaks.
- [ ] Create an event hook system for inter‑tweak communication.
- [ ] Implement secure remote/OTA tweak installation.

