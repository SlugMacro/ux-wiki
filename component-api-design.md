# Component API Design

> API tốt = developer dùng đúng mà không cần đọc docs. API tệ = bugs everywhere.

## Overview

Component API (giao diện lập trình thành phần) là interface mà developer dùng để sử dụng component: props (thuộc tính), slots (khe cắm nội dung), events, variants (biến thể). API design tốt giúp component dễ dùng, khó dùng sai, và flexible enough cho edge cases (trường hợp ngoại lệ).

## Key Points

### Core Principles
- **Pit of success** (hố thành công — dễ làm đúng) — Easy to use correctly, hard to use incorrectly
- **Minimal API surface** (bề mặt API tối thiểu) — Ít props nhất có thể, thêm khi có real use case
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

// Polymorphic (đa hình — hiển thị dạng phần tử khác)
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
- [[design-systems]]
- [[atomic-design]]
- [[design-tokens]]
- [[design-to-dev-handoff]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Component API | Giao diện lập trình thành phần — tập hợp props, slots, events mà developer dùng để sử dụng và tùy chỉnh component |
| Pit of success | Nguyên tắc "hố thành công" — thiết kế API sao cho developer dễ dùng đúng và khó dùng sai |
| API surface | Bề mặt API — tổng số props và options mà component cung cấp. Càng nhỏ càng dễ học và ít lỗi |
| Composition over configuration | Nguyên tắc ưu tiên ghép nối component con linh hoạt thay vì dồn mọi tùy chọn vào props của component cha |
| Polymorphic | Đa hình — component có thể render ra nhiều loại HTML element khác nhau (button, a, div) qua prop "as" |
| Slots pattern | Mẫu thiết kế dùng khe cắm nội dung cho phép developer chèn component con tùy ý, thay vì truyền mọi thứ qua props |
| Edge cases | Trường hợp ngoại lệ — tình huống hiếm gặp nhưng cần xử lý (text quá dài, dữ liệu rỗng, lỗi mạng) |
| Variants | Biến thể — các phiên bản visual khác nhau của cùng một component (primary, secondary, ghost, destructive) |

## Sources
- [API Design Principles](https://www.nngroup.com/articles/developer-experience/) — NNGroup
- [Radix Primitives](https://www.radix-ui.com/primitives) — Radix
