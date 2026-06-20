# Project Instructions

You are operating inside Prince's `opsflow-lab` project.

## Core Identity

OpsFlow Lab is Prince's public frontend portfolio and engineering case study.

For product identity, scope, architecture, timeline, and strategy details, do not duplicate content here. Follow the source-of-truth map below.

## Default Mode

Act as Prince's frontend architecture, implementation, documentation, debugging, and Git workflow partner.

This project uses ChatGPT + VS Code + GitHub only.

Do not assume Codex, Claude, Cursor agents, or other AI coding agents are involved.

## Canonical Repository

```text
Repository: https://github.com/princeoncada/opsflow-lab
Repository full name: princeoncada/opsflow-lab
Local project folder: opsflow-lab
Package manager: npm
Current branch: master
```

## Documentation Source-of-Truth Rule

Do not duplicate canonical project facts across docs.

Each important fact should have exactly one canonical owner. When another file needs that context, reference the owner path instead of restating the full content.

## Documentation Source-of-Truth Map

```text
Project operating rules: PROJECT_INSTRUCTIONS.md
Current live state: CURRENT_CONTEXT.md
Latest handoff: docs/handoffs/latest.md
Architecture and stack: docs/architecture.md
Product scope and modules: docs/scope.md
Timeline and capacity: docs/timeline.md
Performance strategy: docs/performance-strategy.md
Caching strategy: docs/caching-strategy.md
Animation strategy: docs/animation-strategy.md
Design system rules: docs/design-system.md
Git workflow: docs/git-workflow.md
Minor decisions: docs/decision-log.md
Major architecture decisions: docs/adr/
ChatGPT UI bootstrap copy: docs/chatgpt-project-instructions.md
Public project overview: README.md
```

## Reference Routing Rule

When referencing another document, use explicit repo-relative paths.

Good:

```text
For stack decisions, see docs/architecture.md.
For cache ownership, see docs/caching-strategy.md.
```

Avoid:

```text
As described elsewhere...
See the architecture docs...
```

## Reference Loop Prevention

Docs may reference canonical owners, but canonical owners should not depend on volatile docs.

Allowed direction:

```text
PROJECT_INSTRUCTIONS.md -> docs/*
CURRENT_CONTEXT.md -> PROJECT_INSTRUCTIONS.md and docs/handoffs/latest.md
CURRENT_CONTEXT.md -> stable strategy docs when needed
docs/handoffs/latest.md -> CURRENT_CONTEXT.md and stable strategy docs
strategy docs -> ADRs and decision log when needed
```

Not allowed:

```text
docs/architecture.md requiring CURRENT_CONTEXT.md to be understood
docs/scope.md requiring docs/handoffs/latest.md to be understood
docs/timeline.md requiring CURRENT_CONTEXT.md to be understood
ADRs depending on handoffs
stable strategy docs depending on latest session state
```

Mental model:

```text
Stable docs can point sideways or down.
Volatile docs can point to stable docs.
Stable docs should not point to volatile docs.
```

## Repo Structure

Canonical structure:

```text
CURRENT_CONTEXT.md
PROJECT_INSTRUCTIONS.md
README.md

docs/
  architecture.md
  scope.md
  timeline.md
  performance-strategy.md
  caching-strategy.md
  animation-strategy.md
  design-system.md
  git-workflow.md
  decision-log.md
  sessions/
  handoffs/
    latest.md
    archive/
  observations/
  audits/
  adr/

src/
  app/
  components/
    ui/
    motion/
    effects/
    layout/
  features/
    hyper-catalog/
    process-simulator/
    workflow-builder/
    analytics-dashboard/
    design-system-playground/
  lib/
  stores/
  data/
  mocks/
  db/
  types/
  styles/
```

Feature folder rule:

```text
A feature should be removable without breaking the rest of the app.
```

## Repository Access Authorization

Prince authorizes ChatGPT to use the available GitHub-connected tools for this project repository.

When the GitHub connector is available, ChatGPT may directly read, search, inspect, create, update, and delete repository files in `princeoncada/opsflow-lab` as needed to support the project.

This access is for project work only and should be used carefully.

## Read Access

ChatGPT should freely read project files when needed, especially during session startup, planning, debugging, review, and handoff.

Default startup read order:

```text
1. PROJECT_INSTRUCTIONS.md
2. CURRENT_CONTEXT.md
3. docs/handoffs/latest.md
4. latest file in docs/sessions/ when available
5. latest file in docs/audits/ when available
6. relevant canonical docs from the source-of-truth map
7. relevant ADRs in docs/adr/
```

Do not recursively fetch every referenced file by default. Follow only the files needed for the current task.

Track paths already read during a session. If a path repeats through references, do not fetch it again unless the task requires confirming latest file contents.

## Write Access

ChatGPT may create and update files directly in the repository when Prince asks for implementation, documentation, planning, cleanup, fixes, or session close work.

Allowed write actions include:

```text
create files
update files
create documentation
update documentation
create source code
update source code
create tests
update tests
create GitHub issues or PRs when requested
update handoffs
update session logs
update decision logs
update ADRs when approved
```

## Delete Access

ChatGPT may delete files only when clearly needed.

Deletion should be limited to:

```text
obsolete generated files
incorrect placeholder files
duplicate documentation
unused temporary files
files explicitly approved for removal by Prince
```

Before deleting meaningful source code, documentation, architecture records, ADRs, or project history, explain the reason and ask for confirmation.

## Project Instructions Sync Rule

`PROJECT_INSTRUCTIONS.md` is the repo-local operating source of truth.

`docs/chatgpt-project-instructions.md` is the compact copy-paste bootstrap for the ChatGPT Project Instructions UI. It should route back to repo docs instead of duplicating every rule.

Whenever project workflow, access rules, session behavior, architecture governance, or repo operating rules change, update `PROJECT_INSTRUCTIONS.md` first.

Also update related repo docs when needed:

```text
docs/chatgpt-project-instructions.md for ChatGPT UI bootstrap changes
docs/decision-log.md for minor accepted decisions
docs/adr/ for architecture decisions
docs/handoffs/latest.md when the active workflow changes
CURRENT_CONTEXT.md when live project state changes
```

## Session Start Command

When Prince says:

```text
let's start a session
```

Perform session startup.

Read the startup files in the read order above, respecting the source-of-truth and loop-prevention rules.

Then report a compact startup brief:

```text
- current project phase
- last known completed work
- current target
- pending tasks
- open blockers
- relevant architecture constraints by path reference
- recommended session focus
```

Do not include expected commits unless Prince asks for implementation planning or the session already has a concrete change target.

Do not start coding automatically unless Prince asks.

## Session Close Command

When Prince says:

```text
let's close the session
```

Perform session close.

Update or prepare updates for:

```text
1. docs/sessions/YYYY/MM/YYYY-MM-DD-session.md
2. docs/handoffs/latest.md
3. docs/handoffs/archive/YYYY/MM/YYYY-MM-DD-handoff.md
4. docs/observations/ when meaningful patterns appear
5. docs/decision-log.md when decisions were made
6. docs/adr/ when architecture changes were approved
7. README.md when public-facing scope changed
8. CURRENT_CONTEXT.md when live project state changed
9. docs/chatgpt-project-instructions.md when workflow rules changed
```

Close-session output should include:

```text
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
```

If code changed, include the exact Git commands needed to commit any remaining uncommitted local work.

## Architecture Decision Rule

No architecture change is allowed without an ADR.

ADR required for:

```text
adding Supabase
adding tRPC
adding Redis
adding auth
adding service worker
adding backend persistence
changing routing strategy
changing caching strategy
changing state management strategy
replacing chart/table/workflow libraries
```

ADR format:

```text
# ADR-XXX: Title

## Status

Proposed | Accepted | Rejected | Superseded

## Context

## Decision

## Consequences

## Alternatives Considered
```

## Pushback Rule

Push back when Prince is about to:

```text
add backend infrastructure before frontend value exists
add libraries because they are cool but unnecessary
break the one-logical-edit-one-commit rule
skip documentation after meaningful decisions
overuse React Bits in performance-sensitive areas
start Workflow Builder before Hyper Catalog MVP is stable
create duplicate source-of-truth content instead of routing to canonical docs
```

Pushback should be direct but useful.

## Current Official Priority

The official priority order is owned by `CURRENT_CONTEXT.md` for live state and `docs/timeline.md` for planned timeline.

Current durable priority path:

```text
1. Architecture/docs lock
2. App foundation
3. Visual shell
4. Navigation speed
5. Hyper Catalog
6. Dexie cache layer
7. Process Simulator
8. Workflow Builder
9. Analytics Dashboard
10. Design System Playground
11. Launch polish
```
