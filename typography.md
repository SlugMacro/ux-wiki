# Typography

> Hệ thống chữ — nền tảng của mọi UI, chiếm 90%+ content trên screen.

## Overview

Typography không chỉ là "chọn font đẹp". Đó là hệ thống hierarchy, rhythm, và readability quyết định user có đọc được content hay không. Một type system tốt giúp user scan nhanh, đọc thoải mái, và hiểu structure ngay lập tức.

## Key Points

### Type Scale
- Dùng **modular scale** thay vì pick random sizes
- Popular ratios: 1.25 (Major Third), 1.333 (Perfect Fourth), 1.5 (Perfect Fifth)
- Ví dụ scale 1.25 từ base 16px: `12 → 14 → 16 → 20 → 25 → 31 → 39`
- Giới hạn **5-7 sizes** cho toàn bộ app

### Hierarchy
- **Size** — Primary differentiator, nhưng đừng chỉ dựa vào size
- **Weight** — Bold cho headings, regular cho body, medium cho emphasis
- **Color** — Primary text, secondary text, disabled text (3 levels đủ)
- **Spacing** — Headings cần more space above than below (thuộc content phía dưới)

### Readability
- **Line length**: 50-75 characters/line cho body text (desktop). Mobile tự ngắn
- **Line height**: 1.4-1.6 cho body, 1.1-1.3 cho headings
- **Paragraph spacing**: 0.75-1em giữa paragraphs
- **Contrast**: Minimum 4.5:1 cho body text (WCAG AA)

### Font Pairing
- **Safe bet**: 1 font, vary weight. Inter, SF Pro, hoặc Geist
- **Classic combo**: Serif heading + Sans body (Playfair Display + Inter)
- **Modern combo**: Geometric heading + Humanist body (Poppins + Source Sans)
- **Rule of thumb**: Max 2 fonts. Nếu cần 3, bạn đang làm sai gì đó

### System Fonts
- `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
- Zero download, native feel, perfect rendering
- Dùng khi performance > branding

## Examples

- **Linear**: Inter duy nhất, hierarchy hoàn toàn bằng weight + size + color. Clean, efficient
- **Stripe docs**: Tận dụng whitespace + type hierarchy → scannable dù content dày đặc
- **Medium**: Optimized cho long-form reading — serif body, generous line-height

## Related
- [[color-theory]]
- [[layout-and-grid]]
- [[spacing-system]]
- [[design-tokens]]
- [[accessibility-basics]]

## Sources
- [Typographic Scale](https://spencermortensen.com/articles/typographic-scale/) — Spencer Mortensen
- [Butterick's Practical Typography](https://practicaltypography.com/) — Matthew Butterick
- [Type Scale Tool](https://typescale.com/) — Jeremy Church
