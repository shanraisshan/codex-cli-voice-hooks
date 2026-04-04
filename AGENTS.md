# AGENTS.md

This file provides guidance to Codex CLI when working with code in this repository.

## Git Commit Rules

When committing changes, **create separate commits per file**. Do NOT bundle multiple file changes into a single commit. Each file gets its own commit with a descriptive message specific to that file's changes.

For example, if `README.md`, `install/settings.json`, and a test file all changed:
- Commit 1: `git add README.md` → commit with README-specific message
- Commit 2: `git add install/settings.json` → commit with settings-specific message
- Commit 3: `git add tests/test-hooks.py` → commit with test-specific message

This makes the git history cleaner and easier to review, revert, or cherry-pick individual changes.
