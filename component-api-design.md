# Component API Design

> API tốt = developer dùng đúng mà không cần đọc docs. API tệ = bugs everywhere.

## Overview

Component API là interface mà developer dùng để sử dụng component: props, slots, events, variants. API design tốt giúp component dễ dùng, khó dùng sai, và flexible enough cho edge cases.

## Key Points

### Core Principles
- **Pit of success** — Easy to use correctly, hard to use incorrectly
- **Minimal API surface** — Ít props nhất có thể, thêm khi có real use case
- **Composition over configuration** — `<Button><Icon /> Label</Button>` > `<Button icon="check" label="Label" />`
- **Consistent naming** — size, variant, disabled dùng giống nhau across ALL components

### Common Prop Patterns
```tsx
// Size
size: "xs" | "sm" | "md" | "lg" | "xl"

// Variant (visual style)
variant: "primary" | "secondary" | "ghost" | "destructive"

// State
disabled?: boolean
loading?: boolean

// Polymorphic (render as different element)
as?: "button" | "a" | "div"
```

### Slots Pattern (Composition)
```tsx
// Bad: config explosion
<Card title="..." subtitle="..." icon="..." badge="..." footer="..." />

// Good: composition
<Card>
  <CardHeader>
    <CardTitle>...</CardTitle>
    <CardBadge>...</CardBadge>
  </CardHeader>
  <CardContent>...</CardContent>
  <CardFooter>...</CardFooter>
</Card>
```

### When to split components
- >10 props → probably doing too much, split it
- Boolean props that are mutually exclusive → use variant enum instead
- Component has distinct modes → split into separate components

## Examples

- **shadcn/ui**: Gold standard cho composition-based API
- **Radix UI**: Headless primitives with excellent API design
- **Chakra UI**: Good balance giữa convenience props và composition

## Related
- [[atomic-design]]
- [[design-tokens]]
- [[design-to-dev-handoff]]

## Sources
- [API Design Principles](https://www.nngroup.com/articles/developer-experience/) — NNGroup
- [Radix Primitives](https://www.radix-ui.com/primitives) — Radix
