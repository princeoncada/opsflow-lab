# ADR-001: Frontend-First Architecture

## Status

Accepted

## Context

OpsFlow Lab is a frontend portfolio and systems lab. The goal is to demonstrate speed, interaction design, caching, prefetching, motion systems, and business workflow visualization.

The project should be impressive without becoming backend-heavy too early.

## Decision

Use a frontend-first architecture with Next.js App Router, TypeScript, Tailwind CSS, shadcn/ui, Motion, React Bits, Zustand, and Dexie.

Defer Supabase, tRPC, Redis, auth, and backend persistence until they create visible portfolio value.

## Consequences

The project remains fast to build, easier to reason about, and focused on frontend excellence.

Backend infrastructure can still be added later, but only through a formal ADR.

## Alternatives Considered

- Full-stack app from day one
- Supabase-first architecture
- tRPC-first architecture
- Redis-backed cache from day one
