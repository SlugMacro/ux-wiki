# Design Tokens

> Single source of truth cho colors, spacing, typography — bridge giữa design và code.

## Overview

Design tokens là các named values đại diện cho design decisions: `color-primary-500`, `spacing-md`, `font-size-body`. Thay vì hardcode `#3B82F6` khắp nơi, bạn dùng token `color-primary-500` — đổi 1 chỗ, update everywhere. Tokens là ngôn ngữ chung giữa designer (Figma variables) và developer (CSS variables/theme).

## Key Points

### Token Hierarchy (3 levels)
```
Global tokens    →  blue-500: #3B82F6
                     gray-100: #F3F4F6

Alias tokens     →  color-primary: {blue-500}
                     color-bg-subtle: {gray-100}

Component tokens →  button-bg: {color-primary}
                     card-bg: {color-bg-subtle}
```

### Naming Convention
```
{category}-{property}-{variant}-{state}

color-bg-primary          # Background primary
color-text-secondary      # Text secondary
color-border-default      # Border default
spacing-sm                # Spacing small
radius-md                 # Border radius medium
shadow-lg                 # Box shadow large
font-size-body            # Font size body
```

### Token Categories
- **Color**: bg, text, border, fill, stroke
- **Spacing**: padding, margin, gap
- **Typography**: font-family, font-size, font-weight, line-height
- **Border**: radius, width
- **Shadow**: elevation levels
- **Motion**: duration, easing

### Implementation
```css
/* CSS Custom Properties */
:root {
  --color-primary: #3B82F6;
  --spacing-md: 16px;
  --radius-md: 8px;
}

/* Tailwind config */
theme: {
  colors: { primary: 'var(--color-primary)' }
}
```

### Theming with Tokens
- Light/Dark mode = swap alias tokens, keep component tokens unchanged
- Brand theming = swap global tokens, aliases auto-update
- Figma Variables map 1:1 with CSS Custom Properties

## Examples

- **Tailwind**: Config file IS the token system. `colors.blue.500`, `spacing.4`
- **Radix Colors**: Semantic color tokens with automatic dark mode
- **Shopify Polaris tokens**: Public token system with clear naming

## Related
- [[color-theory]]
- [[typography]]
- [[spacing-system]]
- [[atomic-design]]
- [[figma-workflow]]

## Sources
- [Design Tokens W3C Draft](https://www.w3.org/community/design-tokens/) — W3C
- [Tokens in Design Systems](https://medium.com/eightshapes-llc/tokens-in-design-systems-25dd82d58421) — Nathan Curtis
