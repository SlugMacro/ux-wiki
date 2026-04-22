# Design Tokens

> Single source of truth cho colors, spacing, typography — bridge giữa design và code.

## Overview

Design tokens (biến thiết kế) là các named values đại diện cho design decisions: `color-primary-500`, `spacing-md`, `font-size-body`. Thay vì hardcode (ghi cứng giá trị) `#3B82F6` khắp nơi, bạn dùng token `color-primary-500` — đổi 1 chỗ, update everywhere. Tokens là ngôn ngữ chung giữa designer (Figma variables) và developer (CSS variables/theme).

## Key Points

### Token Hierarchy (phân cấp biến) (3 levels)
```
Global tokens (biến toàn cục)    →  blue-500: #3B82F6
                                     gray-100: #F3F4F6

Alias tokens (biến bí danh)     →  color-primary: {blue-500}
                                     color-bg-subtle: {gray-100}

Component tokens (biến thành phần) →  button-bg: {color-primary}
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
- **Motion** (chuyển động): duration, easing (đường cong tốc độ)

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

### Theming (tùy chỉnh giao diện) with Tokens
- Light/Dark mode = swap alias tokens, keep component tokens unchanged
- Brand theming = swap global tokens, aliases auto-update
- Figma Variables map 1:1 with CSS Custom Properties

## Examples

- **Tailwind**: Config file IS the token system. `colors.blue.500`, `spacing.4`
- **Radix Colors**: Semantic color tokens with automatic dark mode
- **Shopify Polaris tokens**: Public token system with clear naming

## Related
- [[design-systems]]
- [[color-theory]]
- [[typography]]
- [[spacing-system]]
- [[atomic-design]]
- [[figma-workflow]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Design tokens | Biến thiết kế — các giá trị được đặt tên (màu, khoảng cách, font) dùng chung giữa Figma và code. Đổi một chỗ, cập nhật khắp nơi |
| Hardcode | Ghi cứng giá trị trực tiếp (ví dụ: #3B82F6) thay vì dùng biến. Khó bảo trì vì phải sửa từng chỗ |
| Global tokens | Biến toàn cục — lớp token thấp nhất, chứa giá trị gốc như blue-500, gray-100. Không mang ngữ nghĩa sử dụng |
| Alias tokens | Biến bí danh — lớp token giữa, gán ý nghĩa cho global tokens (ví dụ: color-primary trỏ đến blue-500) |
| Component tokens | Biến thành phần — lớp token cao nhất, gắn với component cụ thể (ví dụ: button-bg trỏ đến color-primary) |
| Theming | Tùy chỉnh giao diện — khả năng thay đổi diện mạo toàn bộ ứng dụng bằng cách hoán đổi bộ token (Light/Dark, brand A/B) |
| CSS Custom Properties | Biến CSS gốc (dạng --ten-bien) cho phép lưu trữ và tái sử dụng giá trị trong stylesheet. Là cách phổ biến nhất để implement tokens trong code |
| Easing | Đường cong tốc độ — kiểm soát tốc độ animation thay đổi theo thời gian (nhanh đầu chậm cuối, hoặc ngược lại) |

## Sources
- [Design Tokens W3C Draft](https://www.w3.org/community/design-tokens/) — W3C
- [Tokens in Design Systems](https://medium.com/eightshapes-llc/tokens-in-design-systems-25dd82d58421) — Nathan Curtis
