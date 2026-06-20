# ChatGPT Project Instructions

You are operating inside Prince's OpsFlow Lab project.

This file is the compact copy-paste bootstrap for the ChatGPT Project Instructions UI. The repo-local source of truth is `PROJECT_INSTRUCTIONS.md`.

## Canonical Repository

```text
Repository: https://github.com/princeoncada/opsflow-lab
Repository full name: princeoncada/opsflow-lab
Local project folder: opsflow-lab
Package manager: npm
Current branch: master
```

## Repository Access Authorization

Prince authorizes ChatGPT to use the available GitHub-connected tools for this project repository.

When the GitHub connector is available, ChatGPT may directly read, search, inspect, create, update, and delete repository files in `princeoncada/opsflow-lab` as needed to support the project.

This access is for project work only and should be used carefully.

## Required Operating Source

At the start of project work, read `PROJECT_INSTRUCTIONS.md` first when available.

Follow its:

```text
- documentation source-of-truth map
- reference routing rule
- reference loop-prevention rule
- read/write/delete access rules
- session startup and close behavior
- ADR requirements
- Git discipline
- project safety rules
```

## Default Startup Paths

Read only what is needed for the current task. Do not recursively fetch every referenced file.

Default startup read order:

```text
1. PROJECT_INSTRUCTIONS.md
2. CURRENT_CONTEXT.md
3. docs/handoffs/latest.md
4. relevant canonical docs from the source-of-truth map
5. relevant ADRs in docs/adr/
```

Track paths already read during a session. If a path repeats through references, do not fetch it again unless freshness must be confirmed.

## Session Startup Behavior

When Prince says:

```text
let's start a session
```

Read the repository context first using the GitHub connector when available.

Startup should summarize:

```text
- current project phase
- last completed work
- current target
- pending tasks
- open blockers
- relevant architecture constraints by path reference
- recommended session focus
```

Do not include expected commits unless Prince asks for implementation planning or the session already has a concrete change target.

Do not begin implementation automatically unless Prince asks.

## Session Close Behavior

When Prince says:

```text
let's close the session
```

Follow `PROJECT_INSTRUCTIONS.md` for close-session updates, handoffs, logs, and output structure.

## Project Safety Rules

Do not introduce major architecture changes without an ADR.

ADR required for:

```text
Supabase
tRPC
Redis
auth
service worker
backend persistence
routing strategy changes
caching strategy changes
state management changes
major library replacements
```

Do not use Codex, Claude, Cursor agents, or other AI coding agents for this project.

This project is scoped as ChatGPT + VS Code + GitHub only.
