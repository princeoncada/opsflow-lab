# Git Workflow

OpsFlow Lab uses granular Git history as part of the portfolio story.

## Core Loop

Plan -> Implement -> Verify -> Commit -> Log -> Handoff

## Commit Rule

One logical edit = one commit.

## Why This Matters

The Git history should show how the project was built:

- architecture decisions
- foundation setup
- UI system work
- performance work
- feature slices
- tests
- documentation
- polish

## Commit Format

Use Conventional Commit-style messages.

Examples:

- docs: add architecture decision record
- chore: initialize next app shell
- style: add design tokens
- feat: add intent link prefetch wrapper
- feat: add hyper catalog data model
- feat: add dexie catalog cache
- test: add catalog filter tests
- docs: log hyper catalog implementation notes
- fix: resolve mobile navigation overflow

## Required Rhythm

Before committing:

- run `git status`
- stage only the files for the logical edit
- commit with a specific message
- run `git status` again

## PowerShell Commit Pattern

git status
git add <specific-file-or-folder>
git commit -m "<type>: <specific change>"
git status

## Branch Model

Current branch is `master`.

Use feature branches later when a slice becomes large enough to review separately.

Suggested branch naming:

- feature/hyper-catalog
- feature/process-simulator
- feature/workflow-builder
- docs/architecture
- fix/mobile-layout

## PR Model

Even as a solo project, use PRs for meaningful feature slices once the base is stable.

A PR should include:

- summary
- files changed
- screenshots or visual notes when UI changes
- tests/checks run
- performance notes when relevant
- follow-up tasks

## Do Not Use

Avoid vague commits:

- update files
- changes
- fix stuff
- wip
- misc
