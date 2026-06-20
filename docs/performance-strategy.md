# Performance Strategy

OpsFlow Lab should feel instant while still looking visually premium.

## Performance Identity

The project is inspired by McMaster-Carr-style speed:

- fast navigation
- dense information access
- predictable layouts
- aggressive prefetching
- useful caching
- low interaction delay

The project should combine that speed philosophy with React Bits-level visual polish.

## Core Rules

- Default to static or cacheable routes.
- Use intent-based prefetching for likely navigation.
- Use fixed dimensions for cards, media, charts, and skeletons.
- Avoid layout shift.
- Use virtualization for large lists.
- Lazy-load expensive visual effects.
- Keep dense data surfaces readable and responsive.
- Prefer frontend-visible performance wins over backend complexity.
- Measure before adding infrastructure.

## Route Performance

Static or mostly static routes:

- /
- /about
- /lab
- /case-studies/[slug]

Interactive routes:

- /lab/hyper-catalog
- /lab/process-simulator
- /lab/workflow-builder
- /lab/dashboard
- /lab/design-system

Interactive routes should still use cacheable shells where possible.

## Prefetch Strategy

Use normal route prefetching where Next.js provides it.

Add intent prefetching for:

- hover
- focus
- touchstart
- command palette highlight
- search result hover
- card intersection
- related item hover

## Layout Stability

Required:

- fixed aspect ratios for media
- reserved chart dimensions
- skeletons that match final layout
- predictable grid sizing
- no animated element should cause major layout shift

## Performance Budget

- One heavy animated background per route max.
- No heavy animated background behind dense tables.
- Mobile gets lighter visual effects.
- Offscreen effects should be paused or lazy-loaded.
- Reduced-motion mode must be respected.

## Verification

Performance reviews should check:

- route load behavior
- interaction delay
- layout shift
- heavy animation impact
- mobile responsiveness
- unnecessary client components
- avoidable rerenders
