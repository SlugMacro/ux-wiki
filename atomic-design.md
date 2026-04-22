# Atomic Design

> Methodology xây dựng design systems từ nhỏ đến lớn — atoms → molecules → organisms.

## Overview

Atomic Design (Brad Frost) chia UI thành 5 levels, từ elements nhỏ nhất đến full pages. Giúp build design systems scalable (dễ mở rộng) và maintainable (dễ bảo trì) — thay đổi ở atom level cascade (lan truyền) lên toàn bộ system.

## Key Points

### 5 Levels
1. **Atoms** — Smallest units: button, input, label, icon, avatar
2. **Molecules** — Groups of atoms: search bar (input + button), form field (label + input + error)
3. **Organisms** — Complex components: header (logo + nav + search + avatar), card (image + title + meta + CTA)
4. **Templates** — Page layouts with placeholder content
5. **Pages** — Templates filled with real content

### Practical Application
- Đừng quá rigid — đây là mental model, không phải folder structure bắt buộc
- **Components library**: Atoms + Molecules + Organisms
- **Layouts**: Templates
- **Screens**: Pages
- Focus on **composability** (khả năng kết hợp) — components nên compose được với nhau

### Component API Design Tips
- **Props clear**: `size="sm" | "md" | "lg"` not `small={true}`
- **Composition > Configuration** (kết hợp hơn cấu hình): Slots (khe cắm nội dung)/children thay vì 50 props (thuộc tính)
- **Sensible defaults** (giá trị mặc định hợp lý): Button mặc định `variant="primary" size="md"`
- **Consistent API**: Tất cả components dùng cùng prop names (size, variant, disabled)

## Examples

- **shadcn/ui**: Atomic approach — primitive components bạn own và customize
- **Radix UI**: Headless (không có giao diện sẵn) atoms/molecules, bạn style lên
- **Ant Design**: Full organism-level library

## Related
- [[design-systems]]
- [[design-tokens]]
- [[component-api-design]]
- [[figma-workflow]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Atomic Design | Phương pháp luận chia giao diện thành 5 cấp từ nhỏ đến lớn (atoms, molecules, organisms, templates, pages) để xây dựng design system có hệ thống |
| Atoms | Đơn vị nhỏ nhất trong Atomic Design — button, input, label, icon. Không thể chia nhỏ hơn |
| Molecules | Nhóm atoms kết hợp tạo thành chức năng cụ thể. Ví dụ: thanh tìm kiếm = input + button |
| Organisms | Các component phức tạp kết hợp nhiều molecules. Ví dụ: header = logo + navigation + search + avatar |
| Composability | Khả năng kết hợp — thiết kế component sao cho chúng có thể ghép nối linh hoạt với nhau như xếp LEGO |
| Cascade | Sự lan truyền — khi thay đổi ở cấp thấp (atom) tự động ảnh hưởng lên tất cả cấp cao hơn dùng atom đó |
| Headless | Component không có giao diện sẵn — chỉ cung cấp logic và hành vi, developer tự thiết kế giao diện bên ngoài |
| Slots | Khe cắm nội dung — vùng trong component cho phép chèn nội dung tùy ý từ bên ngoài, tăng tính linh hoạt |
| Props | Thuộc tính truyền vào component để điều khiển hành vi và hiển thị (ví dụ: size, variant, disabled) |
| Sensible defaults | Giá trị mặc định hợp lý — component tự hoạt động tốt mà không cần cấu hình thêm |

## Sources
- [Atomic Design](https://atomicdesign.bradfrost.com/) — Brad Frost
- [Design Systems Handbook](https://www.designbetter.co/design-systems-handbook) — InVision
