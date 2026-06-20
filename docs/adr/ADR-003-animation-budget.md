# ADR-003: Animation Budget

## Status

Accepted

## Context

OpsFlow Lab should use jaw-breaking React Bits visuals without sacrificing speed, accessibility, or readability.

Animation should support the product identity, not damage performance.

## Decision

Use React Bits through wrappers in `src/components/effects`.

Use Motion through reusable patterns in `src/components/motion`.

Limit heavy animated backgrounds to one per route.

Require reduced-motion support.

## Consequences

The project can be visually impressive while remaining maintainable and performant.

Feature modules stay protected from direct dependency on decorative visual effects.

## Alternatives Considered

- Directly scattering React Bits components across features
- Animation-first architecture
- CSS-only animation system
- No animation budget
