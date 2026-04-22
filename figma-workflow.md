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

### Auto Layout (tự sắp xếp bố cục) (mastery tier)
- **Mọi thứ phải trong auto-layout** — absolute positioning (định vị tuyệt đối) là last resort
- Nesting: Frame > auto-layout Frame > auto-layout Frame (như Flexbox nesting)
- **Fill container** (lấp đầy khung chứa) cho fluid width, **Hug contents** (ôm sát nội dung) cho intrinsic sizing
- **Min/Max width** trên auto-layout frames = responsive components
- `Shift + A` — Shortcut thần thánh: wrap selection trong auto-layout

### Components Best Practices
- **Variant properties** (thuộc tính biến thể): Size (sm/md/lg), State (default/hover/active/disabled), Type
- **Boolean properties** (thuộc tính đúng/sai): showIcon, showBadge, isLoading
- **Instance swap** (hoán đổi thực thể): Icon slots, avatar slots
- **Component sets** (bộ thành phần): Group related variants (Button/sm/primary/default)
- Naming: `Category/Component/Variant` (e.g., `Input/TextField/Default`)

### Variables (modern approach)
- **Color variables** → Map to design tokens (biến thiết kế)
- **Number variables** → Spacing, border-radius (bo góc), sizing
- **Modes** (chế độ) → Light/Dark theme, Desktop/Mobile breakpoints
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
- [[design-systems]]
- [[design-tokens]]
- [[component-api-design]]
- [[design-to-dev-handoff]]
- [[atomic-design]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Auto Layout | Tính năng trong Figma giúp tự động sắp xếp các phần tử bên trong frame theo hàng hoặc cột, tương tự Flexbox trong CSS |
| Variant properties | Thuộc tính biến thể của component trong Figma, cho phép tạo nhiều phiên bản (ví dụ: size nhỏ/vừa/lớn, trạng thái hover/active) |
| Boolean properties | Thuộc tính đúng/sai trong component, dùng để bật/tắt phần tử con (ví dụ: hiện icon hay không) |
| Instance swap | Tính năng hoán đổi thực thể component trong Figma, cho phép thay đổi nội dung slot (ví dụ: thay icon khác) |
| Component sets | Bộ thành phần trong Figma, nhóm các variant liên quan của một component lại với nhau |
| Variables | Biến trong Figma dùng lưu giá trị tái sử dụng (màu sắc, khoảng cách, bo góc) và hỗ trợ chuyển đổi theme |
| Modes | Chế độ trong Figma Variables, cho phép cùng một biến có giá trị khác nhau tùy ngữ cảnh (Light/Dark, Desktop/Mobile) |
| Fill container | Tùy chọn trong Auto Layout khiến phần tử giãn ra lấp đầy khung chứa, tạo chiều rộng linh hoạt |
| Hug contents | Tùy chọn trong Auto Layout khiến frame co lại vừa khít nội dung bên trong |
| Absolute positioning | Định vị tuyệt đối — đặt phần tử tại vị trí cố định, bỏ qua Auto Layout. Chỉ nên dùng khi thật sự cần thiết |

## Sources
- [Figma Best Practices](https://www.figma.com/best-practices/) — Figma Official
- [Auto Layout Playground](https://www.figma.com/community/file/784448220678228461) — Figma Community
