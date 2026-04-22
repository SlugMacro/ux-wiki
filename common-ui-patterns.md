# Common UI Patterns

> Các pattern UI đã được chứng minh — đừng reinvent the wheel, hãy master the wheel.

## Overview

UI patterns là các giải pháp thiết kế đã được validate qua hàng triệu users. Dùng pattern quen thuộc giảm cognitive load (tải nhận thức) — user không cần "học" cách dùng app của bạn. Sáng tạo ở chỗ khác, không phải ở navigation hay form layout.

## Key Points

### Navigation Patterns
| Pattern | Khi nào dùng | Ví dụ |
|---------|-------------|-------|
| **Top nav** | Marketing sites, <7 items | Stripe, Linear landing |
| **Sidebar** | Apps phức tạp, nhiều sections | Notion, Slack, Figma |
| **Bottom tabs** | Mobile apps, 3-5 main sections | Instagram, Spotify |
| **Breadcrumbs** (thanh đường dẫn phân cấp) | Deep hierarchy, e-commerce | Amazon, docs sites |
| **Command palette** | Power users, many actions | Linear (Cmd+K), VS Code |

### Form Patterns
- **Single column forms** > multi-column (đọc dễ hơn)
- **Labels above inputs** > inline labels (accessible hơn)
- **Inline validation** (kiểm tra ngay tại chỗ) — Validate ngay khi blur (rời khỏi ô nhập), không đợi submit
- **Smart defaults** — Pre-fill gì có thể (country from IP, etc.)
- **Progressive disclosure** — Show advanced options chỉ khi cần

### Feedback Patterns
- **Toast/Snackbar** (thông báo tạm thời) — Temporary, non-blocking success/info
- **Modal/Dialog** (hộp thoại chặn) — Blocking, cần user decision (confirm delete, etc.)
- **Inline message** — Contextual, gần element liên quan
- **Empty state** (trạng thái trống) — Khi không có data, guide user to first action
- **Skeleton loading** (khung xương tải trang) — Perceived performance > spinner

### Data Display Patterns
- **Cards** — Discrete items với mixed content (image + text + actions)
- **Tables** — Structured data cần comparison/sorting
- **Lists** — Sequential items, timeline, feeds
- **Kanban** (bảng quản lý theo trạng thái) — Status-based workflow (Trello, Linear)

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
- [[ai-ux-patterns]] — AI-specific patterns: suggestion chips, streaming responses, AI cards, confidence indicators

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Cognitive load | Tải nhận thức — lượng nỗ lực tinh thần cần thiết để xử lý thông tin. Giao diện tốt giảm thiểu cognitive load |
| Breadcrumbs | Thanh đường dẫn phân cấp — hiển thị vị trí hiện tại trong cấu trúc trang (Home > Category > Product) |
| Command palette | Bảng lệnh nhanh (Cmd+K) — cho phép tìm kiếm và thực hiện mọi thao tác bằng cách gõ, rất mạnh cho power users |
| Inline validation | Kiểm tra ngay tại chỗ — hiển thị lỗi hoặc xác nhận ngay khi người dùng rời khỏi ô nhập, không đợi bấm Submit |
| Toast / Snackbar | Thông báo tạm thời — xuất hiện vài giây rồi tự biến mất, không chặn thao tác. Dùng cho thông báo thành công |
| Modal / Dialog | Hộp thoại chặn — popup yêu cầu người dùng ra quyết định (xác nhận xóa, đăng nhập) trước khi tiếp tục |
| Empty state | Trạng thái trống — giao diện khi không có dữ liệu, cần hướng dẫn người dùng thực hiện hành động đầu tiên |
| Skeleton loading | Khung xương tải trang — hiển thị bố cục xám nhạt giống nội dung thật trong lúc đang tải, tạo cảm giác nhanh hơn spinner |
| Kanban | Bảng quản lý công việc theo cột trạng thái (To Do, In Progress, Done). Trello và Linear là ví dụ điển hình |
| Bulk actions | Thao tác hàng loạt — chọn nhiều item rồi thực hiện một hành động chung (xóa, di chuyển, gán nhãn) |
| Destructive actions | Hành động phá hủy — thao tác không thể hoàn tác như xóa tài khoản, cần xác nhận rõ ràng trước khi thực hiện |

## Sources
- [UI Patterns](https://ui-patterns.com/) — Anders Toxboe
- [Mobbin](https://mobbin.com/) — Real-world UI patterns library
- [Page Flows](https://pageflows.com/) — User flow recordings
