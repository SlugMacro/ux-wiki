# Navigation Patterns

> Information Architecture + Navigation = user tìm được cái họ cần.

## Overview

Navigation (điều hướng) là cách user di chuyển trong app. IA (Information Architecture — kiến trúc thông tin) là cách bạn tổ chức content. Navigation tốt = user KHÔNG BAO GIỜ cảm thấy lạc. Nếu user phải nghĩ "tôi đang ở đâu?" — navigation đã fail.

## Key Points

### Navigation Types
- **Global nav** — Luôn visible, access main sections (top bar, sidebar)
- **Local nav** — Navigate within a section (tabs, sub-menu)
- **Contextual nav** — Links inline trong content
- **Utility nav** — Settings, profile, help (usually top-right)
- **Search** — Fallback khi nav structure không đủ

### Mobile Navigation
- **Bottom tabs** (3-5 items): iOS/Android standard. Thumb-friendly
- **Hamburger menu** (menu ba gạch ngang): Controversial — hides options. Dùng khi >5 sections
- **Tab bar + More**: 4 tabs + "More" tab cho items còn lại
- **Gesture-based**: Swipe between sections (có learning curve)

### Desktop Patterns
- **Persistent sidebar**: Best cho complex apps (Notion, Slack, Figma)
- **Collapsible sidebar**: Maximize content area khi cần
- **Top horizontal nav**: Best cho marketing sites, simple apps
- **Command palette** (bảng lệnh nhanh) **(Cmd+K):** Power user navigation, search-first

### IA Principles
- **Progressive disclosure** (tiết lộ dần dần): Show high-level first, drill down for details
- **Card sorting** (sắp xếp thẻ): Let users organize content → reveals their mental model (mô hình nhận thức)
- **3-click rule**: Myth, nhưng ý tốt — reduce depth where possible
- **Flat > Deep**: Nhiều top-level categories tốt hơn nested 5 levels

## Examples

- **Notion**: Sidebar với nested pages — infinite depth nhưng always oriented
- **Linear**: Sidebar + Cmd+K — hybrid approach, best of both worlds
- **Spotify**: Bottom tabs mobile, sidebar desktop — platform-adaptive

## Related
- [[common-ui-patterns]]
- [[design-principles]]
- [[gestalt-principles]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Information Architecture (IA) | Kiến trúc thông tin — cách tổ chức, phân loại, và cấu trúc nội dung sao cho người dùng dễ tìm thấy điều họ cần |
| Global nav | Điều hướng toàn cục — menu chính luôn hiển thị trên mọi trang, cho phép truy cập các phần chính của ứng dụng |
| Local nav | Điều hướng cục bộ — menu phụ giúp di chuyển trong một phần cụ thể (tabs, sub-menu bên trong một section) |
| Hamburger menu | Menu ba gạch ngang — biểu tượng ba dòng kẻ ngang, nhấn vào mở ra menu ẩn. Tiết kiệm không gian nhưng ẩn lựa chọn |
| Command palette | Bảng lệnh nhanh (Cmd+K) — giao diện tìm kiếm và thực hiện mọi thao tác bằng cách gõ, dành cho power users |
| Card sorting | Phương pháp nghiên cứu cho người dùng tự sắp xếp nội dung vào nhóm, giúp khám phá cách họ tư duy về cấu trúc |
| Mental model | Mô hình nhận thức — cách người dùng hiểu và hình dung hệ thống hoạt động trong đầu họ, ảnh hưởng đến kỳ vọng khi sử dụng |
| Progressive disclosure | Kỹ thuật hiển thị thông tin tổng quan trước, chi tiết sau khi người dùng cần. Giảm tình trạng quá tải thông tin |
| Persistent sidebar | Thanh bên cố định — sidebar luôn hiển thị, phù hợp cho ứng dụng phức tạp có nhiều phần (Notion, Slack) |

## Sources
- [Information Architecture](https://www.nngroup.com/articles/ia-vs-navigation/) — NNGroup
- [Navigation Design](https://www.smashingmagazine.com/2017/04/overview-responsive-navigation-patterns/) — Smashing Magazine
