# Typography

> Hệ thống chữ — nền tảng của mọi UI, chiếm 90%+ content trên screen.

## Overview

Typography (nghệ thuật sắp xếp chữ) không chỉ là "chọn font đẹp". Đó là hệ thống hierarchy (phân cấp thị giác), rhythm (nhịp điệu), và readability (độ dễ đọc) quyết định user có đọc được content hay không. Một type system tốt giúp user scan nhanh, đọc thoải mái, và hiểu structure ngay lập tức.

## Key Points

### Type Scale (thang kích cỡ chữ)
- Dùng **modular scale** (thang tỷ lệ theo hệ số) thay vì pick random sizes
- Popular ratios: 1.25 (Major Third), 1.333 (Perfect Fourth), 1.5 (Perfect Fifth)
- Ví dụ scale 1.25 từ base 16px: `12 → 14 → 16 → 20 → 25 → 31 → 39`
- Giới hạn **5-7 sizes** cho toàn bộ app

### Hierarchy
- **Size** — Primary differentiator, nhưng đừng chỉ dựa vào size
- **Weight** — Bold cho headings, regular cho body, medium cho emphasis
- **Color** — Primary text, secondary text, disabled text (3 levels đủ)
- **Spacing** — Headings cần more space above than below (thuộc content phía dưới)

### Readability
- **Line length** (chiều dài dòng): 50-75 characters/line cho body text (desktop). Mobile tự ngắn
- **Line height** (chiều cao dòng): 1.4-1.6 cho body, 1.1-1.3 cho headings
- **Paragraph spacing**: 0.75-1em giữa paragraphs
- **Contrast**: Minimum 4.5:1 cho body text (WCAG AA)

### Font Pairing (ghép cặp phông chữ)
- **Safe bet**: 1 font, vary weight. Inter, SF Pro, hoặc Geist
- **Classic combo**: Serif (chữ có chân) heading + Sans (chữ không chân) body (Playfair Display + Inter)
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

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Typography | Nghệ thuật và kỹ thuật sắp xếp chữ sao cho dễ đọc, đẹp mắt, và truyền tải đúng thông điệp |
| Hierarchy | Hệ thống phân cấp thị giác giúp người dùng biết đâu là nội dung quan trọng nhất thông qua kích cỡ, độ đậm, màu sắc |
| Modular scale | Thang kích cỡ chữ được tính theo tỷ lệ nhân cố định (ví dụ 1.25x) thay vì chọn size ngẫu nhiên. Giúp hệ thống chữ hài hòa |
| Line height | Chiều cao dòng — khoảng cách giữa các dòng chữ. Ảnh hưởng lớn đến khả năng đọc của đoạn văn |
| Line length | Chiều dài dòng chữ, tính bằng số ký tự mỗi dòng. Lý tưởng là 50-75 ký tự cho body text |
| Font pairing | Kỹ thuật ghép cặp hai phông chữ sao cho hài hòa, thường kết hợp một font serif với một font sans-serif |
| Serif | Phông chữ có chân — các nét nhỏ ở đầu và cuối nét chữ. Thường dùng cho tiêu đề hoặc nội dung dài truyền thống |
| Sans-serif | Phông chữ không chân — nét chữ sạch, hiện đại. Phổ biến trong thiết kế giao diện số |
| Readability | Độ dễ đọc — khả năng người dùng đọc và hiểu nội dung một cách thoải mái, không bị mỏi mắt |
| WCAG AA | Tiêu chuẩn tiếp cận web mức AA, yêu cầu tỷ lệ tương phản tối thiểu 4.5:1 cho chữ thường để đảm bảo mọi người đều đọc được |

## Sources
- [Typographic Scale](https://spencermortensen.com/articles/typographic-scale/) — Spencer Mortensen
- [Butterick's Practical Typography](https://practicaltypography.com/) — Matthew Butterick
- [Type Scale Tool](https://typescale.com/) — Jeremy Church
