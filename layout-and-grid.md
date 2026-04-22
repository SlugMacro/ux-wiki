# Layout & Grid Systems

> Hệ thống grid và layout — xương sống cấu trúc của mọi interface.

## Overview

Grid system tạo ra rhythm và consistency cho layout. Thay vì eyeball mọi thứ, grid cho phép bạn place elements theo hệ thống — kết quả trông "đúng" mà không cần giải thích tại sao. Responsive (tự thích ứng kích thước) design hiện đại dựa trên fluid grids (lưới linh hoạt) kết hợp breakpoints (điểm chuyển đổi bố cục).

## Key Points

### Grid Anatomy
- **Columns**: 12-column phổ biến nhất (chia được cho 2, 3, 4, 6)
- **Gutters** (khoảng cách giữa các cột): Khoảng cách giữa columns (16px-32px typical)
- **Margins** (lề ngoài): Khoảng cách content đến edge (16px mobile, 24-64px desktop)
- **Max-width**: Content container max 1200-1440px

### Responsive Breakpoints (common)
```
Mobile:      0 - 639px     (1-2 columns)
Tablet:      640 - 1023px  (4-8 columns)
Desktop:     1024 - 1439px (12 columns)
Large:       1440px+       (12 columns, centered)
```

### Layout Patterns
- **Single column** — Mobile default, articles, onboarding flows
- **Sidebar + content** — Dashboards, docs, email clients
- **Grid of cards** — Galleries, marketplaces, social feeds
- **Split screen** — Landing pages, comparison views
- **Holy grail** — Header + sidebar + content + aside + footer (classic web)

### Modern CSS Layout
- **Flexbox** (bố cục linh hoạt 1 chiều) — 1D layout (row OR column). Dùng cho component-level layout
- **CSS Grid** (bố cục lưới 2 chiều) — 2D layout (rows AND columns). Dùng cho page-level layout
- **Container queries** (truy vấn theo kích thước phần tử cha) — Responsive based on parent size, not viewport (khung nhìn)
- Kết hợp: Grid cho page structure, Flexbox cho components bên trong

### Spacing System
- Dùng **base unit** (4px hoặc 8px) và chỉ dùng multiples
- 4px base: `4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96`
- Tạo rhythm và consistency, tránh "magic numbers"

## Examples

- **Stripe**: 12-col grid, generous margins, max-width ~1080px. Breathable
- **Dashboard UIs**: Sidebar fixed 240-280px, content fluid
- **Airbnb**: Card grid responsive từ 1 col (mobile) → 4 col (desktop)

## Related
- [[spacing-system]]
- [[typography]]
- [[common-ui-patterns]]
- [[design-tokens]]
- [[gestalt-principles]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Grid system | Hệ thống lưới — khung cấu trúc chia trang thành các cột và hàng, giúp sắp xếp nội dung nhất quán và có nhịp điệu |
| Columns | Các cột dọc trong grid, thường dùng 12 cột vì chia được cho nhiều số (2, 3, 4, 6) |
| Gutters | Khoảng cách giữa các cột trong grid, giúp nội dung không dính sát nhau |
| Margins | Lề ngoài — khoảng cách từ nội dung đến mép màn hình |
| Responsive | Thiết kế tự thích ứng kích thước, tự động điều chỉnh bố cục theo kích thước màn hình khác nhau |
| Breakpoints | Điểm chuyển đổi bố cục — các ngưỡng kích thước màn hình mà tại đó layout thay đổi cách hiển thị |
| Flexbox | Kỹ thuật bố cục một chiều trong CSS, sắp xếp phần tử theo hàng hoặc cột. Phù hợp cho layout bên trong component |
| CSS Grid | Kỹ thuật bố cục hai chiều trong CSS, sắp xếp phần tử theo cả hàng và cột. Phù hợp cho layout cấp trang |
| Container queries | Kỹ thuật responsive mới, thay đổi layout dựa trên kích thước phần tử cha thay vì kích thước cửa sổ trình duyệt |
| Fluid grid | Lưới linh hoạt — grid co giãn theo tỷ lệ phần trăm thay vì pixel cố định |
| Viewport | Khung nhìn — vùng hiển thị nội dung trên trình duyệt, thay đổi theo kích thước thiết bị |

## Sources
- [Grid Systems in Graphic Design](https://www.niggli.ch/en/grid-systems-in-graphic-design.html) — Josef Müller-Brockmann
- [Layout Grid Guide](https://www.figma.com/best-practices/everything-you-need-to-know-about-layout-grids/) — Figma
- [Every Layout](https://every-layout.dev/) — Heydon Pickering & Andy Bell
