# Changelog

All notable changes to this project will be documented in this file.

The format is based on Keep a Changelog.

## [0.1.2] - 2026-02-07

### Changed

- Unified submit behavior into a single workflow without a mode-selection step.
- Standardized release scope analysis to always use the last version tag to `HEAD`.
- Moved `AGENTS.md` synchronization to run before commit and push, aligned with README sync timing.
- Updated commit staging guidance to include optional `AGENTS.md` changes when applicable.

## [0.1.1] - 2026-02-07

### Changed

- Added a brief introduction section to improve skill onboarding guidance.
- Clarified submit workflow rules so commit messages are derived from staged diff intent.
- Prohibited version-only commit subjects such as `feat: vX.Y.Z`.
- Added release-only commit message guidance and examples in commit message references.

[0.1.1]: https://github.com/LaiTszKin/submit-changes/compare/v0.1.0...v0.1.1
[0.1.2]: https://github.com/LaiTszKin/submit-changes/compare/v0.1.1...v0.1.2
