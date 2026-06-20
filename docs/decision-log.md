# Decision Log

This file records accepted project decisions that do not require a full ADR.

Architecture-level decisions require ADRs.

## Accepted Decisions

### 2026-06-20 - Use npm

Decision: Use npm as the package manager for OpsFlow Lab.

Reason: Prince prefers npm and the repo was initialized with npm.

Impact: All commands should use `npm`, `npx`, and `package-lock.json`.

### 2026-06-20 - Use master as current branch

Decision: Keep the current branch as `master` for now.

Reason: The repo was initialized this way.

Impact: Commands should reference `master` unless an explicit rename is approved.

### 2026-06-20 - Defer @vitejs/plugin-react

Decision: Do not install `@vitejs/plugin-react` during initial dev tooling setup.

Reason: npm dependency resolution produced a Babel peer dependency conflict, and the project is a Next.js app rather than a Vite app.

Impact: Vitest remains in scope, but test config will be handled later with a clean Next-compatible setup.

### 2026-06-20 - Use shadcn Base preset

Decision: Use the Base component library option from shadcn.

Reason: It keeps the component foundation close to shadcn defaults and avoids premature visual lock-in.

Impact: The visual identity will be built through project tokens, wrappers, React Bits effects, and layout composition.

### 2026-06-20 - Use source-of-truth doc routing

Decision: Use explicit source-of-truth ownership for important project context and route references by repo-relative paths instead of duplicating canonical facts across docs.

Reason: The first documentation pass repeated project identity, stack, deferred stack, timeline, workflow rules, and current state across multiple files, creating drift risk.

Impact: `PROJECT_INSTRUCTIONS.md` owns repo operating rules and the source-of-truth map. `CURRENT_CONTEXT.md` and `docs/handoffs/latest.md` should stay volatile and path-based. Stable strategy docs should not depend on handoffs or current context to be understood.
