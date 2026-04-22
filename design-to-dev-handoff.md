# Design-to-Dev Handoff

> Nơi design gặp code — handoff tốt = ít back-and-forth, ship nhanh.

## Overview

Handoff (bàn giao thiết kế) là quá trình chuyển giao design từ designer sang developer. Handoff tệ = dev đoán mò, designer thất vọng, nhiều rounds chỉnh sửa. Handoff tốt = specs (thông số kỹ thuật) rõ ràng, tokens mapped, interactions documented.

## Key Points

### What to Include
- **Specs**: Spacing, sizing, colors (as tokens, not hex)
- **States**: Default, hover, active, disabled, loading, error, empty
- **Responsive**: How it behaves ở mobile, tablet, desktop
- **Interactions**: Transitions, animations, gestures
- **Edge cases** (trường hợp biên): Long text, missing data, error states, empty states (trạng thái trống)
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
- **Storybook** (thư viện tài liệu sống): Living documentation — component in all states, interactive
- **Zeplin**: Dedicated handoff tool (being replaced by Figma Dev Mode)

## Related
- [[figma-workflow]]
- [[design-tokens]]
- [[component-api-design]]
- [[atomic-design]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Handoff | Bàn giao thiết kế — quá trình chuyển giao design từ designer sang developer với đầy đủ thông số để xây dựng |
| Specs | Thông số kỹ thuật — chi tiết về khoảng cách, kích thước, màu sắc, typography cần thiết để developer xây dựng chính xác |
| Edge cases | Trường hợp biên — các tình huống không phải "happy path" cần thiết kế: text quá dài, dữ liệu rỗng, lỗi mạng |
| Empty states | Trạng thái trống — giao diện hiển thị khi không có dữ liệu, cần hướng dẫn người dùng hành động tiếp theo |
| Dev mode | Chế độ dành cho developer trong Figma, tự động hiển thị thông số CSS, khoảng cách, và code snippet |
| Storybook | Thư viện tài liệu sống — công cụ hiển thị component ở tất cả trạng thái, cho phép developer tương tác và kiểm tra |
| Happy path | Đường dẫn lý tưởng — luồng sử dụng chính khi mọi thứ hoạt động đúng, không có lỗi hay ngoại lệ |
| Pixel-perfect | Việc triển khai code khớp chính xác từng pixel với bản thiết kế. Thực tế nên ưu tiên "intention-perfect" (đúng ý đồ) hơn |

## Sources
- [Figma Dev Mode](https://www.figma.com/dev-mode/) — Figma
- [Design Handoff Guide](https://www.smashingmagazine.com/2021/02/design-handoff-collaboration-tools/) — Smashing Magazine
