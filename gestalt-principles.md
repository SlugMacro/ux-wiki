# Gestalt Principles

> Các nguyên tắc tri giác giải thích cách não bộ nhóm và tổ chức visual elements (yếu tố thị giác).

## Overview

Gestalt (tiếng Đức = "hình dạng/tổng thể") là lý thuyết tâm lý học giải thích cách con người nhìn nhận tổng thể trước chi tiết. Não bộ tự động nhóm, kết nối, và hoàn thiện hình ảnh — designer khai thác điều này để tạo layout rõ ràng mà không cần borders hay dividers nặng nề.

## Key Points

### 7 Nguyên tắc cốt lõi

1. **Proximity** (sự gần gũi) — Elements gần nhau được perceived (nhận biết) là một nhóm. Spacing > borders để phân nhóm
2. **Similarity** (sự tương đồng) — Elements giống nhau (color, size, shape) được perceived là related. Dùng consistent styling cho cùng một loại element
3. **Closure** (tính đóng kín) — Não tự "đóng" hình không hoàn chỉnh. Icons có thể simplified vì não tự fill gaps
4. **Continuity** (tính liên tục) — Mắt follow đường liên tục. Align elements theo line/curve để tạo flow
5. **Figure-Ground** (hình và nền) — Não tự tách foreground (tiền cảnh) và background (nền). Modal overlay (lớp phủ hộp thoại) dùng nguyên tắc này
6. **Common region** (vùng chung) — Elements trong cùng một bounded area được grouped. Cards, containers
7. **Symmetry** (đối xứng) — Não prefer đối xứng, perceived as stable và pleasant

### Áp dụng thực tế

| Principle | Áp dụng trong UI |
|-----------|-----------------|
| Proximity | Form field labels gần input, xa field khác |
| Similarity | Tất cả clickable items cùng màu accent |
| Closure | Progress bars, partially visible carousels |
| Continuity | Horizontal scrolling lists, timeline layouts |
| Figure-Ground | Modals darkening background, dropdown menus |
| Common region | Card-based layouts, grouped form sections |

## Examples

- **Proximity**: Airbnb listing card — price, rating, location gần nhau = 1 info group, tách biệt với description
- **Figure-Ground**: Apple sử dụng whitespace (khoảng trắng) cực rộng để foreground product nổi bật
- **Common region**: Notion dùng subtle background để group related blocks

## Related
- [[design-principles]]
- [[layout-and-grid]]
- [[spacing-system]]
- [[cognitive-biases]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Gestalt | Lý thuyết tâm lý học từ Đức giải thích cách não bộ tự động nhóm các yếu tố thị giác thành tổng thể có ý nghĩa, thay vì nhìn từng chi tiết riêng lẻ |
| Proximity | Nguyên tắc cho rằng các phần tử đặt gần nhau sẽ được não bộ nhận biết là thuộc cùng một nhóm |
| Similarity | Nguyên tắc cho rằng các phần tử có hình dạng, màu sắc, kích thước giống nhau sẽ được coi là có liên quan với nhau |
| Closure | Khả năng não bộ tự "đóng kín" và hoàn thiện những hình ảnh chưa hoàn chỉnh. Ví dụ: nhìn nửa vòng tròn vẫn hiểu đó là hình tròn |
| Continuity | Nguyên tắc cho rằng mắt người có xu hướng đi theo đường liên tục, giúp tạo luồng thị giác trong thiết kế |
| Figure-Ground | Nguyên tắc não bộ tự động tách biệt đối tượng chính (hình) khỏi phần nền phía sau. Modal overlay là ứng dụng phổ biến |
| Common region | Nguyên tắc cho rằng các phần tử nằm trong cùng một vùng được bao quanh sẽ được coi là một nhóm |
| Perceived | Được nhận biết, cảm nhận bởi người dùng — cách não bộ diễn giải thông tin thị giác, có thể khác với thực tế |
| Whitespace | Khoảng trắng hay không gian trống trong thiết kế, giúp nội dung "thở" và tạo sự tập trung vào phần tử chính |

## Sources
- [Gestalt Principles in UI Design](https://www.nngroup.com/articles/gestalt-proximity/) — NNGroup
- [Laws of UX — Law of Proximity](https://lawsofux.com/law-of-proximity/) — Jon Yablonski
