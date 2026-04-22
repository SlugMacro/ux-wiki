# Accessibility Basics

> Inclusive design — thiết kế cho MỌI NGƯỜI, không chỉ "average user".

## Overview

Accessibility (a11y) không phải feature bổ sung — nó là baseline. 15% dân số thế giới có disability. Thiết kế accessible = thiết kế tốt hơn cho TẤT CẢ users (curb cuts principle). WCAG (Web Content Accessibility Guidelines) là tiêu chuẩn quốc tế.

## Key Points

### WCAG 4 Principles — POUR
1. **Perceivable** — User phải nhận biết được content (alt text, captions, contrast)
2. **Operable** — User phải thao tác được (keyboard nav, no time limits, no seizure triggers)
3. **Understandable** — Content phải dễ hiểu (clear language, predictable, error help)
4. **Robust** — Content phải hoạt động với assistive tech (semantic HTML, ARIA)

### Contrast Minimums
- **Normal text**: 4.5:1 ratio (WCAG AA)
- **Large text** (18px+ bold, 24px+ regular): 3:1 ratio
- **UI components & graphics**: 3:1 ratio
- **AAA level**: 7:1 (enhanced, cho body text ideal)

### Keyboard Navigation
- **Tab** order phải logical (follow visual flow)
- **Focus indicators** phải visible — ĐỪNG BAO GIỜ `outline: none` mà không thay thế
- **Skip links** — "Skip to main content" cho screen reader users
- Mọi interactive element phải reachable bằng keyboard

### Screen Readers
- Dùng **semantic HTML** (`<nav>`, `<main>`, `<button>`, `<h1-h6>`)
- **Alt text** cho images có meaning. `alt=""` cho decorative images
- **aria-label** khi visual context không đủ (icon-only buttons)
- **Live regions** (`aria-live`) cho dynamic content updates

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

## Sources
- [WCAG 2.2 Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/) — W3C
- [A11y Project Checklist](https://www.a11yproject.com/checklist/) — A11y Project
- [Inclusive Components](https://inclusive-components.design/) — Heydon Pickering
