# Color Theory

> Hệ thống màu sắc — công cụ mạnh nhất để truyền tải emotion, hierarchy, và brand identity.

## Overview

Color trong UI không phải "chọn màu thích". Đó là hệ thống có cấu trúc: primary, secondary, neutral, semantic colors (màu mang ý nghĩa chức năng) — mỗi màu có vai trò rõ ràng. Color system tốt thì scalable (dễ mở rộng) và accessible (dễ tiếp cận cho mọi user).

## Key Points

### Color System Structure

```
Brand colors:    Primary (1) + Secondary (0-2)
Neutral palette: Gray scale (50-950) cho text, borders, backgrounds
Semantic colors: Success (green), Warning (amber), Error (red), Info (blue)
```

### Xây dựng palette
1. **Chọn 1 primary color** — Đại diện brand
2. **Generate neutral scale** — 10 shades từ near-white đến near-black
3. **Thêm semantic colors** — Green/amber/red/blue với 3-5 shades mỗi màu
4. **Test contrast** — Mọi text/bg combo phải pass WCAG AA (4.5:1 body, 3:1 large text)

### Contrast & Accessibility
- **4.5:1** — Minimum cho normal text (WCAG AA)
- **3:1** — Minimum cho large text & UI components
- **7:1** — Enhanced contrast (WCAG AAA)
- Tools: Stark plugin (Figma), WebAIM Contrast Checker

### Dark Mode (chế độ tối)
- KHÔNG đơn giản là invert colors
- Giảm saturation (độ bão hòa) trong dark mode (bright colors chói mắt trên dark bg)
- Dùng elevation (độ nổi bề mặt) thay vì shadow (lighter surface = higher elevation)
- Text dùng ~87% white thay vì pure white (less eye strain)

### Color Psychology (high-level)
| Color | Association | Usage |
|-------|------------|-------|
| Blue | Trust, calm, professional | Finance, tech, healthcare |
| Green | Growth, success, nature | Eco, health, confirmation |
| Red | Urgency, error, passion | Alerts, sales, food |
| Purple | Premium, creative | Luxury, creative tools |
| Orange | Energy, friendly, CTA | E-commerce, entertainment |
| Neutral | Professional, clean | Enterprise, productivity |

### 60-30-10 Rule
- **60%** dominant color (background, large surfaces)
- **30%** secondary color (cards, sections)
- **10%** accent color (màu nhấn) (CTAs (nút kêu gọi hành động), highlights)

## Examples

- **Linear**: Near-monochrome với purple accent duy nhất. Elegant, focused
- **Stripe**: Gradient chuyển sắc subtle + consistent semantic colors
- **Notion**: Almost no color — lets content be the color. Extreme restraint

## Related
- [[typography]]
- [[design-tokens]]
- [[accessibility-basics]]
- [[layout-and-grid]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Semantic colors | Màu mang ý nghĩa chức năng cố định: xanh lá = thành công, đỏ = lỗi, vàng = cảnh báo, xanh dương = thông tin |
| Palette | Bảng màu — tập hợp các màu được chọn có hệ thống để sử dụng xuyên suốt sản phẩm |
| Contrast ratio | Tỷ lệ tương phản giữa màu chữ và màu nền, đo bằng con số (ví dụ 4.5:1). Càng cao càng dễ đọc |
| Saturation | Độ bão hòa màu — mức độ "đậm" hay "rực" của một màu. Màu saturation thấp sẽ nhạt hơn, gần xám hơn |
| Elevation | Trong dark mode, dùng bề mặt sáng hơn để thể hiện lớp cao hơn thay vì dùng bóng đổ như light mode |
| Dark mode | Chế độ giao diện tối, dùng nền tối và chữ sáng. Cần thiết kế riêng, không đơn giản là đảo ngược màu |
| 60-30-10 Rule | Quy tắc phân bổ màu: 60% màu nền chủ đạo, 30% màu phụ, 10% màu nhấn. Giúp giao diện cân bằng và không rối |
| Accent color | Màu nhấn — chiếm tỷ lệ nhỏ nhưng thu hút sự chú ý, thường dùng cho nút bấm quan trọng |
| Scalable | Dễ mở rộng — hệ thống có thể phát triển thêm mà không bị phá vỡ cấu trúc ban đầu |

## Sources
- [Color in Design Systems](https://medium.com/eightshapes-llc/color-in-design-systems-a1c80f65fa3) — Nathan Curtis
- [Refactoring UI — Color](https://www.refactoringui.com/) — Adam Wathan & Steve Schoger
- [Accessible Color Generator](https://www.learnui.design/tools/accessible-color-generator.html) — Erik Kennedy
