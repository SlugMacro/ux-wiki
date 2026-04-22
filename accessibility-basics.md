# Accessibility Basics

> Inclusive design — thiết kế cho MỌI NGƯỜI, không chỉ "average user".

## Overview

Accessibility (a11y) (khả năng tiếp cận) không phải feature bổ sung — nó là baseline. 15% dân số thế giới có disability (khuyết tật). Thiết kế accessible = thiết kế tốt hơn cho TẤT CẢ users (curb cuts principle — nguyên tắc lề đường: thiết kế cho người khuyết tật cũng giúp ích mọi người). WCAG (Web Content Accessibility Guidelines — hướng dẫn tiếp cận nội dung web) là tiêu chuẩn quốc tế.

## Key Points

### WCAG 4 Principles — POUR
1. **Perceivable** (nhận biết được) — User phải nhận biết được content (alt text (mô tả thay thế hình ảnh), captions, contrast (độ tương phản))
2. **Operable** (thao tác được) — User phải thao tác được (keyboard nav, no time limits, no seizure triggers)
3. **Understandable** (dễ hiểu) — Content phải dễ hiểu (clear language, predictable, error help)
4. **Robust** (bền vững) — Content phải hoạt động với assistive tech (công nghệ hỗ trợ) (semantic HTML (HTML có ngữ nghĩa), ARIA)

### Contrast Minimums
- **Normal text**: 4.5:1 ratio (WCAG AA)
- **Large text** (18px+ bold, 24px+ regular): 3:1 ratio
- **UI components & graphics**: 3:1 ratio
- **AAA level**: 7:1 (enhanced, cho body text ideal)

### Keyboard Navigation
- **Tab** order phải logical (follow visual flow)
- **Focus indicators** (chỉ báo đang chọn) phải visible — ĐỪNG BAO GIỜ `outline: none` mà không thay thế
- **Skip links** (liên kết nhảy cóc) — "Skip to main content" cho screen reader (trình đọc màn hình) users
- Mọi interactive element phải reachable bằng keyboard

### Screen Readers
- Dùng **semantic HTML** (`<nav>`, `<main>`, `<button>`, `<h1-h6>`)
- **Alt text** cho images có meaning. `alt=""` cho decorative images
- **aria-label** (nhãn cho trình đọc màn hình) khi visual context không đủ (icon-only buttons)
- **Live regions** (vùng nội dung động) (`aria-live`) cho dynamic content updates

### Common Mistakes
- Color là cách DUY NHẤT truyền tải meaning (color blind users)
- Placeholder text thay cho label
- Auto-playing video/audio
- Tiny touch targets (<44x44px mobile)
- Text trong images thay vì real text

## Examples

- **GOV.UK**: Gold standard accessibility. Semantic, keyboard-friendly, simple language
- **Stripe**: Excellent contrast ratios, keyboard navigation throughout dashboard
- **Apple**: VoiceOver integration deep trong mọi product

## Related
- [[design-principles]]
- [[color-theory]]
- [[typography]]
- [[common-ui-patterns]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Accessibility (a11y) | Khả năng tiếp cận — thiết kế sao cho mọi người đều dùng được, bao gồm người khuyết tật. "a11y" là viết tắt (a + 11 ký tự + y) |
| WCAG | Web Content Accessibility Guidelines — bộ hướng dẫn quốc tế về tiếp cận nội dung web, chia thành 3 mức A, AA, AAA |
| POUR | Bốn nguyên tắc cốt lõi của WCAG: Perceivable (nhận biết được), Operable (thao tác được), Understandable (dễ hiểu), Robust (bền vững) |
| Screen reader | Trình đọc màn hình — phần mềm đọc to nội dung trang web cho người khiếm thị, dựa vào HTML có ngữ nghĩa |
| Semantic HTML | HTML có ngữ nghĩa — dùng đúng thẻ cho đúng mục đích (nav cho điều hướng, button cho nút bấm) giúp máy hiểu cấu trúc trang |
| Focus indicators | Chỉ báo đang chọn — viền hoặc highlight hiển thị phần tử đang được focus khi dùng bàn phím điều hướng |
| Skip links | Liên kết nhảy cóc — link ẩn cho phép người dùng screen reader nhảy thẳng đến nội dung chính, bỏ qua menu |
| Alt text | Mô tả thay thế cho hình ảnh, được screen reader đọc lên. Hình trang trí dùng alt rỗng |
| ARIA | Bộ thuộc tính HTML bổ sung giúp screen reader hiểu các phần tử tương tác phức tạp mà HTML thường không diễn tả đủ |
| Live regions | Vùng nội dung động trên trang, dùng aria-live để screen reader tự động thông báo khi nội dung thay đổi |
| Assistive tech | Công nghệ hỗ trợ — thiết bị hoặc phần mềm giúp người khuyết tật sử dụng máy tính (screen reader, switch device, eye tracking) |
| Curb cuts principle | Nguyên tắc lề đường — thiết kế ban đầu cho người khuyết tật nhưng mang lại lợi ích cho tất cả mọi người |

## Sources
- [WCAG 2.2 Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/) — W3C
- [A11y Project Checklist](https://www.a11yproject.com/checklist/) — A11y Project
- [Inclusive Components](https://inclusive-components.design/) — Heydon Pickering
