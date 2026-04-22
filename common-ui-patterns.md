# Common UI Patterns

> Các pattern UI đã được chứng minh — đừng reinvent the wheel, hãy master the wheel.

## Overview

UI patterns là các giải pháp thiết kế đã được validate qua hàng triệu users. Dùng pattern quen thuộc giảm cognitive load — user không cần "học" cách dùng app của bạn. Sáng tạo ở chỗ khác, không phải ở navigation hay form layout.

## Key Points

### Navigation Patterns
| Pattern | Khi nào dùng | Ví dụ |
|---------|-------------|-------|
| **Top nav** | Marketing sites, <7 items | Stripe, Linear landing |
| **Sidebar** | Apps phức tạp, nhiều sections | Notion, Slack, Figma |
| **Bottom tabs** | Mobile apps, 3-5 main sections | Instagram, Spotify |
| **Breadcrumbs** | Deep hierarchy, e-commerce | Amazon, docs sites |
| **Command palette** | Power users, many actions | Linear (Cmd+K), VS Code |

### Form Patterns
- **Single column forms** > multi-column (đọc dễ hơn)
- **Labels above inputs** > inline labels (accessible hơn)
- **Inline validation** — Validate ngay khi blur, không đợi submit
- **Smart defaults** — Pre-fill gì có thể (country from IP, etc.)
- **Progressive disclosure** — Show advanced options chỉ khi cần

### Feedback Patterns
- **Toast/Snackbar** — Temporary, non-blocking success/info
- **Modal/Dialog** — Blocking, cần user decision (confirm delete, etc.)
- **Inline message** — Contextual, gần element liên quan
- **Empty state** — Khi không có data, guide user to first action
- **Skeleton loading** — Perceived performance > spinner

### Data Display Patterns
- **Cards** — Discrete items với mixed content (image + text + actions)
- **Tables** — Structured data cần comparison/sorting
- **Lists** — Sequential items, timeline, feeds
- **Kanban** — Status-based workflow (Trello, Linear)

### Action Patterns
- **Primary/Secondary CTA** — 1 primary action rõ ràng per screen
- **Destructive actions** — Red color + confirm dialog
- **Bulk actions** — Select multiple → action bar appears
- **Undo > Confirm** — "Undo" toast thay vì "Are you sure?" dialog

## Examples

- **Linear**: Command palette (Cmd+K) làm trung tâm navigation — power user dream
- **Notion**: Empty state luôn có clear CTA: "Press / for commands" hoặc template suggestions
- **Stripe Dashboard**: Table pattern với inline expand, không cần navigate away

## Related
- [[design-principles]]
- [[navigation-patterns]]
- [[micro-interactions]]
- [[gestalt-principles]]

## Sources
- [UI Patterns](https://ui-patterns.com/) — Anders Toxboe
- [Mobbin](https://mobbin.com/) — Real-world UI patterns library
- [Page Flows](https://pageflows.com/) — User flow recordings
