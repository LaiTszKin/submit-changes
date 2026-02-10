# submit-changes

A Codex skill that standardizes how code changes are submitted and released.

## Brief introduction

`submit-changes` is an agent skill for repositories that need a predictable submit process. It helps agents inspect local changes, apply version/release updates, and publish commits/tags with consistent conventions.

## What this skill does

The skill guides an agent through a safe, repeatable submit workflow:

1. Inspect current git changes and staging state.
2. Identify version/tag baseline and always read release scope from last tag to `HEAD`.
3. Propose a preferred semantic version bump/version, confirm with the user, then apply updates.
4. Update release documentation (`CHANGELOG.md`, `README.md` when needed).
5. Update `AGENTS.md` before commit/push when workflow rules need syncing.
6. Commit, tag, and push changes.

## Repository layout

- `SKILL.md` - core workflow and operating instructions.
- `references/` - supporting standards for semantic versioning, commit messages, changelog format, branch naming, and README updates.

## Usage

Place this skill under your Codex skills directory and invoke it when you want the agent to:

- submit code changes
- prepare a release
- commit + tag + push

Common trigger phrases include: `submit changes`, `提交`, `送出`, and `提交變更`.

## Example

Example user request:

```text
submit changes, it is a initial commit.
write a readme.
publish to a public repo with using github cli
```

Expected agent behavior:

1. Inspect git status and detect staged/unstaged files.
2. Create or update `README.md` as requested.
3. Commit with a concise Conventional Commit message.
4. Publish to GitHub using `gh repo create ... --public --source=. --push`.
5. Optionally create and push a version tag.

## Notes

This repository contains only the skill definition and references. It does not ship runnable application code.
