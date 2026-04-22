# Atomic Design

> Methodology xây dựng design systems từ nhỏ đến lớn — atoms → molecules → organisms.

## Overview

Atomic Design (Brad Frost) chia UI thành 5 levels, từ elements nhỏ nhất đến full pages. Giúp build design systems scalable và maintainable — thay đổi ở atom level cascade lên toàn bộ system.

## Key Points

### 5 Levels
1. **Atoms** — Smallest units: button, input, label, icon, avatar
2. **Molecules** — Groups of atoms: search bar (input + button), form field (label + input + error)
3. **Organisms** — Complex components: header (logo + nav + search + avatar), card (image + title + meta + CTA)
4. **Templates** — Page layouts with placeholder content
5. **Pages** — Templates filled with real content

### Practical Application
- Đừng quá rigid — đây là mental model, không phải folder structure bắt buộc
- **Components library**: Atoms + Molecules + Organisms
- **Layouts**: Templates
- **Screens**: Pages
- Focus on **composability** — components nên compose được với nhau

### Component API Design Tips
- **Props clear**: `size="sm" | "md" | "lg"` not `small={true}`
- **Composition > Configuration**: Slots/children thay vì 50 props
- **Sensible defaults**: Button mặc định `variant="primary" size="md"`
- **Consistent API**: Tất cả components dùng cùng prop names (size, variant, disabled)

## Examples

- **shadcn/ui**: Atomic approach — primitive components bạn own và customize
- **Radix UI**: Headless atoms/molecules, bạn style lên
- **Ant Design**: Full organism-level library

## Related
- [[design-tokens]]
- [[component-api-design]]
- [[figma-workflow]]

## Sources
- [Atomic Design](https://atomicdesign.bradfrost.com/) — Brad Frost
- [Design Systems Handbook](https://www.designbetter.co/design-systems-handbook) — InVision
