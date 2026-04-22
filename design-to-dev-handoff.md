# Design-to-Dev Handoff

> Nơi design gặp code — handoff tốt = ít back-and-forth, ship nhanh.

## Overview

Handoff là quá trình chuyển giao design từ designer sang developer. Handoff tệ = dev đoán mò, designer thất vọng, nhiều rounds chỉnh sửa. Handoff tốt = specs rõ ràng, tokens mapped, interactions documented.

## Key Points

### What to Include
- **Specs**: Spacing, sizing, colors (as tokens, not hex)
- **States**: Default, hover, active, disabled, loading, error, empty
- **Responsive**: How it behaves ở mobile, tablet, desktop
- **Interactions**: Transitions, animations, gestures
- **Edge cases**: Long text, missing data, error states, empty states
- **Copy**: Final text content, not lorem ipsum

### Figma-specific Tips
- **Dev mode** — Switch to dev mode for auto-generated specs
- **Component properties** — Document variants, boolean props
- **Auto-layout constraints** — Min/max width tells dev responsive behavior
- **Variables** — Map to CSS custom properties / Tailwind config

### Process
1. Design review meeting — walk through with dev
2. Dev asks questions, designer annotates unclear parts
3. Dev builds, designer reviews (not pixel-perfect, but intention-perfect)
4. Iterate — 1-2 rounds max if handoff was clear

### Common Pitfalls
- Designer hands off 1 happy path, no edge cases → dev makes up the rest
- Specs in absolute pixels, no token references → inconsistent implementation
- No interaction specs → static implementation, feels dead
- Handoff too early (before design is finalized) → wasted dev time

## Examples

- **Figma Dev Mode**: Inspect panel shows CSS, iOS, Android code + spacing
- **Storybook**: Living documentation — component in all states, interactive
- **Zeplin**: Dedicated handoff tool (being replaced by Figma Dev Mode)

## Related
- [[figma-workflow]]
- [[design-tokens]]
- [[component-api-design]]
- [[atomic-design]]

## Sources
- [Figma Dev Mode](https://www.figma.com/dev-mode/) — Figma
- [Design Handoff Guide](https://www.smashingmagazine.com/2021/02/design-handoff-collaboration-tools/) — Smashing Magazine
