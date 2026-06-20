# Design System

OpsFlow Lab uses a normalized design system instead of a collage of component libraries.

## Hierarchy

- shadcn/ui is the base component layer.
- Radix provides accessibility primitives.
- Tailwind tokens are the visual source of truth.
- Motion powers reusable animation primitives.
- React Bits provides high-impact visual effects.
- Motion Primitives provides reusable animated interaction patterns.
- Kokonut UI is selective inspiration only.

## Component Ownership

Base components live in:

- `src/components/ui`

Motion wrappers live in:

- `src/components/motion`

Visual effect wrappers live in:

- `src/components/effects`

Layout components live in:

- `src/components/layout`

Feature-specific components live inside their feature folder.

## Rule

No random component-library collage.

Everything must feel like OpsFlow Lab.

## Visual Direction

The interface should feel:

- fast
- technical
- premium
- dark-mode excellent
- clean in light mode
- dense when useful
- motion-rich but not noisy

## shadcn/ui Role

shadcn/ui provides the base component foundation.

Components should be customized through:

- Tailwind classes
- variants
- CSS variables
- wrapper components
- design tokens

## React Bits Role

React Bits provides visual impact.

React Bits components should be wrapped so the project can control:

- performance behavior
- reduced-motion behavior
- styling consistency
- import boundaries
- future replacement if needed

## Accessibility

The design system should maintain:

- semantic HTML
- keyboard access
- visible focus states
- reduced-motion support
- color contrast
- screen-reader-friendly labels where needed
