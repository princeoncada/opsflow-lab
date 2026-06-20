# ADR-002: Caching Strategy

## Status

Accepted

## Context

OpsFlow Lab should practice aggressive caching and prefetching inspired by McMaster-Carr-style speed.

The caching strategy should be visible in the frontend experience rather than hidden behind premature backend infrastructure.

## Decision

Use static/cacheable routes, intent-based prefetching, browser memory, and Dexie/IndexedDB for local-first persistence.

Defer service worker until route and data behavior stabilizes.

Defer Redis until server-side caching becomes a visible portfolio feature.

## Consequences

The caching story remains frontend-visible and avoids premature backend infrastructure.

Hyper Catalog becomes the first major module proving this strategy.

## Alternatives Considered

- Redis from day one
- Supabase persistence from day one
- Service worker from day one
- No persistent browser cache
