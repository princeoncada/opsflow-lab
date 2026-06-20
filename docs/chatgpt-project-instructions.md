# ChatGPT Project Instructions

You are operating inside Prince's OpsFlow Lab project.

## Canonical Repository

Repository:

https://github.com/princeoncada/opsflow-lab

Repository full name:

princeoncada/opsflow-lab

Local project folder:

opsflow-lab

Package manager:

npm

Current branch:

master

## Repository Access Authorization

Prince authorizes ChatGPT to use the available GitHub-connected tools for this project repository.

When the GitHub connector is available, ChatGPT may directly read, search, inspect, create, update, and delete repository files in `princeoncada/opsflow-lab` as needed to support the project.

This access is for project work only and should be used carefully.

## Read Access

ChatGPT should freely read project files when needed, especially during session startup, planning, debugging, review, and handoff.

Default files to inspect when relevant:

- PROJECT_INSTRUCTIONS.md
- CURRENT_CONTEXT.md
- docs/chatgpt-project-instructions.md
- docs/handoffs/latest.md
- docs/architecture.md
- docs/scope.md
- docs/timeline.md
- docs/performance-strategy.md
- docs/caching-strategy.md
- docs/animation-strategy.md
- docs/design-system.md
- docs/git-workflow.md
- docs/decision-log.md
- docs/adr/
- README.md
- package.json
- src/

## Write Access

ChatGPT may create and update files directly in the repository when Prince asks for implementation, documentation, planning, cleanup, fixes, or session close work.

Allowed write actions include:

- create files
- update files
- create documentation
- update documentation
- create source code
- update source code
- create tests
- update tests
- create GitHub issues or PRs when requested
- update handoffs
- update session logs
- update decision logs
- update ADRs when approved

## Delete Access

ChatGPT may delete files only when clearly needed.

Deletion should be limited to:

- obsolete generated files
- incorrect placeholder files
- duplicate documentation
- unused temporary files
- files explicitly approved for removal by Prince

Before deleting meaningful source code, documentation, architecture records, ADRs, or project history, ChatGPT should explain the reason and ask for confirmation.

## Project Instructions Sync Rule

This file is the canonical copy-paste source for the ChatGPT Project Instructions UI.

Whenever project workflow, access rules, session behavior, architecture governance, or repo operating rules change, update this file first.

Also update related repo docs when needed:

- PROJECT_INSTRUCTIONS.md for repo operating behavior
- docs/decision-log.md for minor accepted decisions
- docs/adr/ for architecture decisions
- docs/handoffs/latest.md when the active workflow changes

## Session Startup Behavior

When Prince says:

let's start a session

ChatGPT should read the repository context first, using the GitHub connector when available.

Startup should summarize:

- current phase
- last completed work
- current target
- pending tasks
- open blockers
- architecture constraints
- recommended session focus
- expected commits

Do not begin implementation automatically unless Prince asks.

## Session Close Behavior

When Prince says:

let's close the session

ChatGPT should prepare or directly update, when appropriate:

- docs/sessions/YYYY/MM/YYYY-MM-DD-session.md
- docs/handoffs/latest.md
- docs/handoffs/archive/YYYY/MM/YYYY-MM-DD-handoff.md
- docs/decision-log.md
- docs/observations/
- docs/adr/
- README.md when public-facing scope changed
- docs/chatgpt-project-instructions.md when workflow rules changed

Close-session output should include:

- session summary
- completed work
- files changed
- commits made
- checks/tests run
- visual review notes
- performance notes
- bugs or regressions
- pending work
- next recommended target
- handoff summary

## Git Discipline

Every meaningful change should follow this project rule:

One logical edit = one commit.

When working locally through Prince, provide exact PowerShell commands for:

git status
git add <specific files>
git commit -m "<type>: <specific change>"
git status

When using GitHub-connected tools directly, keep changes similarly granular and explain what was changed.

## Project Safety Rules

Do not introduce major architecture changes without an ADR.

ADR required for:

- Supabase
- tRPC
- Redis
- auth
- service worker
- backend persistence
- routing strategy changes
- caching strategy changes
- state management changes
- major library replacements

Do not use Codex, Claude, Cursor agents, or other AI coding agents for this project.

This project is scoped as ChatGPT + VS Code + GitHub only.
