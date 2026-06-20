# Caching Strategy

OpsFlow Lab uses a frontend-first caching strategy.

## Core Principle

Cache what improves user-perceived speed without creating premature backend complexity.

## Approved v1 Caching Layers

### Layer 1 - Static and Render Caching

Use static or cacheable routes wherever possible.

Applies to:

- landing page
- lab index
- about page
- case studies
- catalog shell

### Layer 2 - Browser Memory

Use in-memory state for active session UI state.

Applies to:

- command palette state
- current filters
- active selected records
- temporary hover-prefetch state
- active module configuration

### Layer 3 - Dexie / IndexedDB

Dexie owns local-first persistence.

Approved uses:

- recently viewed catalog items
- saved workflow drafts
- saved simulator scenarios
- prefetched catalog detail records
- offline demo data
- local user preferences

### Layer 4 - Service Worker

Deferred until route and data behavior are stable.

Potential future uses:

- static asset caching
- offline shell
- visual asset caching
- fallback route

### Layer 5 - Redis

Deferred until a server-side caching feature creates visible portfolio value.

Potential future uses:

- server-side catalog cache
- AI response cache
- rate limiting
- cache visualization lab
- external API response cache

## Explicit v1 Decision

No Redis in v1.

No Supabase persistence in v1.

No tRPC API cache in v1.

## Hyper Catalog Caching

Hyper Catalog should demonstrate:

- instant repeat access
- recently viewed records
- cached detail payloads
- virtualized results
- intent-prefetched records
- local cache inspection or visible cache status where useful

## Cache Safety

Avoid:

- hiding stale data bugs
- caching form submissions
- caching user-specific future auth data
- adding service worker too early
- introducing backend cache before frontend cache is visible
