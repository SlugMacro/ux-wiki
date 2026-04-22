# Spacing System

> Consistent spacing tạo visual rhythm — mắt cảm nhận được dù không ý thức.

## Overview

Spacing system dùng base unit (thường 4px hoặc 8px) và chỉ sử dụng các bội số. Loại bỏ "magic numbers" — không còn 13px, 17px, hay 23px random. Consistent spacing là khác biệt lớn nhất giữa amateur và professional UI.

## Key Points

### 4px Base Grid
```
4   — Tight: icon-to-label gap
8   — Compact: inline elements, small padding
12  — Default gap: between related items
16  — Standard padding: cards, inputs, buttons
20  — Medium gap: between form fields
24  — Section padding: card padding, list items
32  — Large gap: between groups
40  — Extra: section separators
48  — Layout spacing
64  — Major sections
80  — Page sections
96  — Hero spacing
```

### Khi nào dùng spacing nào
- **Tight (4-8px)**: Elements thuộc cùng nhóm chặt — icon + label, badge + text
- **Default (12-16px)**: Padding bên trong containers, gap giữa sibling elements
- **Medium (20-32px)**: Phân tách groups, form sections
- **Large (40-64px)**: Page sections, major visual breaks
- **Hero (80-96px)**: Landing pages, hero sections, breathing room

### Relationship to Gestalt
- Proximity principle: items **gần nhau = related**
- Spacing between related items < spacing between unrelated items
- Heading spacing: **more space above than below** (heading thuộc content phía dưới)

## Examples

- **Tailwind spacing scale**: `space-1 (4px)` đến `space-24 (96px)` — follows 4px base
- **Linear**: Incredibly tight spacing system, mọi gap đều intentional

## Related
- [[layout-and-grid]]
- [[gestalt-principles]]
- [[design-tokens]]
- [[typography]]

## Sources
- [Space in Design Systems](https://medium.com/eightshapes-llc/space-in-design-systems-188bcbae0d62) — Nathan Curtis
- [The 8-Point Grid](https://spec.fm/specifics/8-pt-grid) — Spec.fm
