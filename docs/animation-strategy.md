# Animation Strategy

OpsFlow Lab should be visually impressive without sacrificing speed, accessibility, or readability.

## Animation Identity

The visual language should feel:

- premium
- futuristic
- fast
- controlled
- purposeful
- technical

React Bits provides high-impact effects, but those effects must be wrapped and normalized into the project design system.

## Core Rules

- React Bits components live behind wrappers in `src/components/effects`.
- Reusable Motion patterns live in `src/components/motion`.
- Feature logic must not directly own decorative visual effects.
- Reduced-motion support is required.
- Expensive effects should be lazy-loaded.
- Offscreen effects should be paused or avoided.
- Animation should support meaning, hierarchy, or delight.

## Motion Budget

- One heavy animated background per route max.
- No heavy animated backgrounds behind data tables.
- No animation should make text harder to read.
- Mobile defaults should be lighter.
- Prefer transform and opacity animations.
- Avoid layout-driven animation unless necessary.
- Avoid endless animation in dense work surfaces.

## Approved Motion Patterns

- page reveal
- staggered cards
- animated numbers
- hover elevation
- focus-visible emphasis
- command palette transitions
- drawer and modal transitions
- detail panel transitions
- queue/process animation
- chart entrance animation, used lightly

## Reduced Motion

Reduced-motion mode should:

- disable decorative loops
- simplify page transitions
- reduce stagger durations
- keep important state changes visible
- preserve usability

## React Bits Usage

React Bits is best suited for:

- landing hero
- lab index
- featured cards
- background accents
- text reveals
- premium showcase sections

React Bits should be avoided for:

- dense tables
- form-heavy sections
- long-reading case studies
- performance-sensitive list rendering
