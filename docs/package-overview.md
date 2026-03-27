# Package Overview

## Why This Repository Is Artifact-First

`nbot-tracker-openclaw` currently stores a packaged skill file, `nbot-tracker.skill`, at the repository root.
That packaging choice makes the project portable for direct distribution, but it also means reviewers cannot immediately browse an unpacked source tree from the GitHub landing page.

This document exists to make the repository easier to understand without changing the current artifact-first layout.

## What The Package Contains

The zip archive currently exposes the following internal paths:

- `SKILL.md`
- `scripts/setup-tracker.sh`
- `references/nbot-format.md`
- `references/platform-setup.md`

These files indicate that the package is organized around three layers:

- a top-level skill definition
- a small setup helper script
- reference documents for message formatting and platform setup

## What Reviewers Should Understand First

If someone visits this repository for portfolio review, the most important things to understand are:

1. The repository is not empty. Its main implementation guidance is inside the `.skill` archive.
2. The skill targets a specific automation workflow: polling `nbot.ai` updates and sending formatted digests through OpenClaw-supported messaging channels.
3. The package includes both behavioral instructions and operational references, not just a single binary blob with no context.

## Why Keep The `.skill` File

Keeping the packaged file at the root is still useful because:

- it represents the distributable artifact
- it preserves the actual installation unit used by the workflow
- it keeps the repository aligned with how the skill is intended to be shared

For portfolio readability, the README now explains the package clearly instead of pretending this is a conventional source-first repository.

## Current Tradeoff

This layout favors portability over inspectability.

- Advantage: one file is easy to move, archive, and reuse
- Drawback: GitHub visitors cannot inspect the structure without extra explanation

That tradeoff is acceptable for this version of the repository as long as the README and documentation explain the package honestly and precisely.

## Suggested Future Upgrade

If the unpacked source becomes available later, a stronger repository version would include:

- an unpacked mirror of the package files
- example configuration inputs
- a minimal OpenClaw integration example
- test fixtures for formatting and scheduling behavior
