# Latest Handoff

Last updated: 2026-06-20

## Project

OpsFlow Lab

## Current Phase

Architecture and foundation lock.

Live phase owner: `../../CURRENT_CONTEXT.md`

## Last Completed

- Public repo created and cloned locally.
- Next.js app initialized.
- shadcn/ui initialized.
- Runtime and dev tooling packages installed.
- Locked project folder structure created.
- Baseline documentation files created.
- Documentation source-of-truth routing added to `../../PROJECT_INSTRUCTIONS.md`.
- `../../CURRENT_CONTEXT.md` reduced to a live-state snapshot.

## Current Target

Finish documentation governance cleanup, then verify the app locally before starting app shell implementation.

## Pending

- Finish compacting duplicated docs content where needed.
- Verify app runs locally.
- Replace starter Next.js README.
- Begin app provider/layout foundation only after docs governance is stable.

## Reference Paths

Use these canonical files instead of duplicating their content here:

```text
Operating rules: ../../PROJECT_INSTRUCTIONS.md
Current state: ../../CURRENT_CONTEXT.md
Architecture and stack: ../architecture.md
Product scope: ../scope.md
Timeline: ../timeline.md
Performance strategy: ../performance-strategy.md
Caching strategy: ../caching-strategy.md
Animation strategy: ../animation-strategy.md
Design system: ../design-system.md
Git workflow: ../git-workflow.md
Decision log: ../decision-log.md
ADRs: ../adr/
```

## Loop Prevention

This handoff may point to canonical docs, but canonical strategy docs should not depend on this handoff to be understood.

Do not recursively fetch every referenced path during startup. Read only the files needed for the current task and avoid fetching the same path twice in one session unless freshness must be confirmed.

## Next Recommended Session Focus

Run local verification, then start the app shell foundation if checks pass.
