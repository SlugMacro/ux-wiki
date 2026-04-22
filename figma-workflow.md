# Figma Workflow

> Tips và workflow để dùng Figma hiệu quả — từ solo designer đến team lớn.

## Overview

Figma là industry standard cho UI design. Nhưng tool chỉ tốt khi workflow tốt. Page này tập trung vào cách tổ chức file, auto-layout, variables, và plugins giúp tăng tốc workflow.

## Key Points

### File Structure
```
📁 Project
├── 📄 Cover (thumbnail + status)
├── 📄 Design System (components + tokens)
├── 📄 Wireframes (lo-fi explorations)
├── 📄 Design (final screens)
├── 📄 Prototype (interactive flows)
└── 📄 Archive (old versions, không xoá)
```

### Page Naming Convention
- `✅ Feature Name` — Done
- `🔄 Feature Name` — In progress
- `📐 Feature Name` — Wireframe
- `🗄️ Archive` — Old stuff

### Auto Layout (mastery tier)
- **Mọi thứ phải trong auto-layout** — absolute positioning là last resort
- Nesting: Frame > auto-layout Frame > auto-layout Frame (như Flexbox nesting)
- **Fill container** cho fluid width, **Hug contents** cho intrinsic sizing
- **Min/Max width** trên auto-layout frames = responsive components
- `Shift + A` — Shortcut thần thánh: wrap selection trong auto-layout

### Components Best Practices
- **Variant properties**: Size (sm/md/lg), State (default/hover/active/disabled), Type
- **Boolean properties**: showIcon, showBadge, isLoading
- **Instance swap**: Icon slots, avatar slots
- **Component sets**: Group related variants (Button/sm/primary/default)
- Naming: `Category/Component/Variant` (e.g., `Input/TextField/Default`)

### Variables (modern approach)
- **Color variables** → Map to design tokens
- **Number variables** → Spacing, border-radius, sizing
- **Modes** → Light/Dark theme, Desktop/Mobile breakpoints
- Variables > local styles cho token-based systems

### Essential Plugins
| Plugin | Purpose |
|--------|---------|
| **Stark** | Accessibility checker (contrast, vision sim) |
| **Content Reel** | Realistic placeholder content |
| **Figma to Code** | Export to React/Tailwind |
| **Batch Styler** | Bulk edit styles |
| **Contrast** | Quick contrast ratio check |

### Shortcuts (must-know)
- `Cmd + /` — Quick actions (search commands)
- `Shift + A` — Add auto-layout
- `Cmd + G` — Group / `Cmd + Shift + G` — Ungroup
- `Alt + drag` — Duplicate
- `I` — Color picker
- `Cmd + D` — Duplicate in place
- `Cmd + Shift + H` — Flip horizontal

## Examples

- **Uber design system**: Exemplary Figma file structure với component documentation inline
- **Shopify Polaris**: Public Figma library — great reference cho variable setup

## Related
- [[design-tokens]]
- [[component-api-design]]
- [[design-to-dev-handoff]]
- [[atomic-design]]

## Sources
- [Figma Best Practices](https://www.figma.com/best-practices/) — Figma Official
- [Auto Layout Playground](https://www.figma.com/community/file/784448220678228461) — Figma Community
