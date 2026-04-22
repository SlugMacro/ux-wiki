# Design Principles

> Những nguyên tắc nền tảng định hình mọi quyết định thiết kế UX/UI.

## Overview

Design principles là bộ "la bàn" giúp designer đưa ra quyết định nhất quán. Thay vì thiết kế theo cảm tính, principles cho phép bạn có framework để evaluate và justify mọi design choice.

Có 2 loại principles: **universal principles** (áp dụng mọi nơi) và **product-specific principles** (riêng cho từng sản phẩm — ví dụ Material Design principles của Google).

## Key Points

### 10 Heuristics (nguyên tắc đánh giá nhanh) của Nielsen Norman
1. **Visibility of system status** — Luôn cho user biết đang xảy ra gì
2. **Match between system and real world** — Dùng ngôn ngữ user hiểu, không phải jargon hệ thống
3. **User control and freedom** — Luôn có "emergency exit" (undo, back, cancel)
4. **Consistency and standards** — Cùng một action phải hoạt động giống nhau khắp nơi
5. **Error prevention** — Thiết kế để user KHÔNG THỂ mắc lỗi, tốt hơn là thông báo lỗi
6. **Recognition rather than recall** — Hiển thị options thay vì bắt user nhớ
7. **Flexibility and efficiency** — Shortcuts cho expert, simplicity cho newbie
8. **Aesthetic and minimalist design** — Mỗi element phải earn its place
9. **Help users recognize, diagnose, and recover from errors** — Error messages rõ ràng, actionable
10. **Help and documentation** — Có nhưng không nên cần dùng đến

### Principles bổ sung
- **Hierarchy** — Mắt user đọc theo pattern (F-pattern, Z-pattern). Design phải guide visual flow
- **Affordance** (khả năng gợi ý cách sử dụng) — Object phải "trông giống" cách nó hoạt động (button trông bấm được)
- **Feedback** (phản hồi) — Mọi action đều cần response. Silence is confusing
- **Progressive disclosure** (tiết lộ dần dần) — Chỉ show thông tin cần thiết, hide complexity cho đến khi cần

## Examples

- **Visibility**: Stripe checkout hiển thị step indicator (1/3, 2/3, 3/3)
- **Consistency**: iOS dùng swipe-back gesture nhất quán trong toàn hệ thống
- **Error prevention**: Gmail hỏi "Did you mean to attach?" khi detect từ "attached" mà không có file
- **Progressive disclosure**: Notion mặc định clean, hover mới hiện controls

## Related
- [[cognitive-biases]]
- [[gestalt-principles]]
- [[common-ui-patterns]]
- [[accessibility-basics]]
- [[ai-ux-patterns]] — Nielsen's Heuristics trong context AI: visibility of system status cho streaming, error recovery cho hallucinations

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Heuristics | Bộ nguyên tắc đánh giá nhanh dùng để kiểm tra chất lượng thiết kế mà không cần test với người dùng thật |
| Affordance | Đặc tính thiết kế giúp người dùng hiểu ngay cách sử dụng. Ví dụ: nút bấm trông lồi lên khiến người ta muốn nhấn vào |
| Progressive disclosure | Kỹ thuật chỉ hiện thông tin cần thiết trước, giấu phần phức tạp cho đến khi người dùng cần. Giúp giao diện đỡ rối |
| Feedback | Phản hồi — mọi hành động của người dùng đều cần response từ hệ thống. Im lặng = người dùng bối rối |
| Visibility of system status | Nguyên tắc luôn cho người dùng biết hệ thống đang ở trạng thái nào (đang tải, đã lưu, có lỗi) |
| F-pattern / Z-pattern | Mẫu đọc tự nhiên của mắt người trên trang web. F-pattern cho trang nhiều text, Z-pattern cho trang ít nội dung |
| Error prevention | Thiết kế ngăn lỗi xảy ra từ đầu thay vì chỉ thông báo lỗi sau khi người dùng mắc sai lầm |
| Recognition over recall | Nguyên tắc hiển thị lựa chọn sẵn thay vì bắt người dùng phải nhớ. Dropdown tốt hơn text field trống |

## Sources
- [10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — Nielsen Norman Group
- [Laws of UX](https://lawsofux.com/) — Jon Yablonski
- [Principles of Design](https://www.interaction-design.org/literature/topics/design-principles) — IxDF
