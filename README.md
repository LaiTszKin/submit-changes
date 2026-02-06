# submit-changes

A Codex skill that standardizes how code changes are submitted and released.

## What this skill does

The skill guides an agent through a safe, repeatable submit workflow:

1. Inspect current git changes and staging state.
2. Choose a submit mode (release-only or staged commit).
3. Identify version/tag baseline and change range.
4. Decide and apply semantic version updates.
5. Update release documentation (`CHANGELOG.md`, `README.md` when needed).
6. Commit, tag, and push changes.
7. Keep `AGENTS.md` aligned with the latest workflow expectations.

## Repository layout

- `SKILL.md` - core workflow and operating instructions.
- `references/` - supporting standards for semantic versioning, commit messages, changelog format, branch naming, and README updates.

## Usage

Place this skill under your Codex skills directory and invoke it when you want the agent to:

- submit code changes
- prepare a release
- commit + tag + push

Common trigger phrases include: `submit changes`, `提交`, `送出`, and `提交變更`.

## Notes

This repository contains only the skill definition and references. It does not ship runnable application code.
