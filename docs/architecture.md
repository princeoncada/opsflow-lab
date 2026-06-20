# Architecture

OpsFlow Lab uses a frontend-first architecture optimized for speed, motion quality, and portfolio-grade interaction design.

## Core Principle

Static first.
Client-fast second.
Backend last.

## Locked Stack

- Next.js App Router
- TypeScript
- Tailwind CSS
- shadcn/ui
- Radix primitives
- Motion
- React Bits
- Motion Primitives
- Kokonut UI selectively
- Zustand
- Dexie
- Zod
- React Hook Form
- MSW
- TanStack Table
- TanStack Virtual
- Recharts or Visx
- React Flow via @xyflow/react
- Vitest
- Playwright

## Deferred Stack

The following are deferred unless approved through ADR:

- Supabase
- tRPC
- Redis
- Auth
- Database-backed user accounts
- Realtime backend
- AI backend
- Prisma
- GraphQL
- Redux

## System Layers

src/app:
Routes, layouts, route boundaries, metadata, and page-level composition.

src/components/ui:
shadcn-owned base components.

src/components/motion:
Reusable motion wrappers and animation primitives.

src/components/effects:
React Bits wrappers and high-impact decorative visuals.

src/components/layout:
App shell, navigation, command surfaces, and shared layout pieces.

src/features:
Feature-owned modules such as Hyper Catalog, Process Simulator, Workflow Builder, Analytics Dashboard, and Design System Playground.

src/lib:
Shared utilities, formatting, constants, and route registry.

src/stores:
Global Zustand stores only.

src/data:
Static portfolio data, catalog seeds, and mock records.

src/mocks:
MSW handlers and mock API contracts.

src/db:
Dexie schema and browser persistence helpers.

src/types:
Shared TypeScript types.

src/styles:
Shared styling helpers outside Tailwind globals.

## Feature Boundary Rule

A feature should be removable without breaking the rest of the app.

Each feature should own its own components, hooks, library helpers, stores, schemas, and types when they are feature-specific.

## Data Strategy

Version 1 uses:

- static data
- mock data
- MSW
- Dexie
- local browser state
- cacheable Next routes

Version 1 does not use a real backend unless an ADR approves it.

## Performance Strategy Summary

OpsFlow Lab should feel instant through:

- static/cacheable routes
- intent-based prefetching
- stable layout dimensions
- reduced-motion support
- virtualized large lists
- browser-side Dexie caching
- lazy-loaded expensive visual effects
- minimal backend dependency

## Architecture Governance

No architecture change is allowed without an ADR.

Architecture changes include adding backend infrastructure, changing state management, changing caching strategy, replacing major libraries, or introducing auth/database/realtime systems.
