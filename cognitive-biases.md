# Cognitive Biases trong Design

> Những thiên lệch nhận thức ảnh hưởng đến cách user ra quyết định và tương tác với sản phẩm.

## Overview

Cognitive biases (thiên lệch nhận thức) là các "shortcuts" trong não bộ giúp con người xử lý thông tin nhanh hơn, nhưng đôi khi dẫn đến quyết định không hợp lý. Designer cần hiểu biases để: (1) thiết kế thuận theo cách não bộ hoạt động, và (2) tránh manipulate user một cách phi đạo đức.

## Key Points

### Biases quan trọng nhất cho UX

- **Anchoring** (hiệu ứng mỏ neo) — Thông tin đầu tiên user thấy sẽ "neo" mọi đánh giá sau đó. Pricing pages đặt plan đắt nhất trước để plan giữa trông "hợp lý"
- **Loss aversion** (sợ mất mát) — Mất mát đau gấp 2x so với niềm vui khi được. "Your trial expires in 3 days" mạnh hơn "Subscribe to keep features"
- **Serial position effect** (hiệu ứng vị trí) — User nhớ item đầu và cuối danh sách rõ nhất. Đặt actions quan trọng ở đầu/cuối nav
- **Hick's Law** (luật Hick) — Nhiều lựa chọn = thời gian quyết định lâu hơn = drop-off cao hơn. Giảm options
- **Fitts's Law** (luật Fitts) — Target lớn hơn + gần hơn = dễ click hơn. CTA buttons phải to và dễ reach
- **Peak-end rule** (quy tắc đỉnh-kết) — User đánh giá trải nghiệm dựa trên peak moment và ending, không phải average. Nail the ending
- **Bandwagon effect** (hiệu ứng đám đông) — "10,000 people signed up today" — social proof (bằng chứng xã hội) works
- **Default bias** (thiên lệch mặc định) — Phần lớn user giữ nguyên default. Chọn defaults cẩn thận, ethically
- **Von Restorff effect** (hiệu ứng nổi bật) — Item khác biệt trong nhóm sẽ được nhớ. Highlight CTA bằng color contrast

### Ethical considerations
- Biases có thể bị lạm dụng thành **dark patterns** (thủ thuật lừa người dùng)
- Dùng biases để giúp user đạt MỤC TIÊU CỦA HỌ, không phải mục tiêu business thuần túy
- Ví dụ tốt: default opt-in 2FA (security). Ví dụ xấu: default opt-in spam emails

## Examples

- **Anchoring**: Basecamp hiện "$299/month for everything" — một price duy nhất, anchored against "enterprise pricing" phức tạp của competitors
- **Peak-end**: Mailchimp hiện high-five animation sau khi gửi campaign — memorable ending
- **Hick's Law**: Linear chỉ có 1 CTA trên landing page thay vì 5 options

## Related
- [[design-principles]]
- [[gestalt-principles]]
- [[user-research-methods]]
- [[ai-ux-patterns]] — Automation bias, anchoring bias, Trust Trap trong AI products

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Cognitive biases | Thiên lệch nhận thức — các "đường tắt" trong não bộ giúp xử lý thông tin nhanh nhưng đôi khi dẫn đến quyết định sai lệch |
| Anchoring | Hiệu ứng mỏ neo — thông tin đầu tiên nhận được sẽ ảnh hưởng mạnh đến mọi đánh giá sau đó |
| Loss aversion | Tâm lý sợ mất mát — con người cảm nhận nỗi đau mất mát mạnh gấp 2 lần niềm vui khi được. Rất hiệu quả trong marketing |
| Hick's Law | Luật Hick — càng nhiều lựa chọn, người dùng càng mất nhiều thời gian quyết định và càng dễ bỏ cuộc |
| Fitts's Law | Luật Fitts — phần tử càng lớn và càng gần con trỏ thì càng dễ click. Ảnh hưởng trực tiếp đến kích thước nút bấm |
| Peak-end rule | Quy tắc đỉnh-kết — người dùng đánh giá trải nghiệm dựa trên khoảnh khắc cảm xúc mạnh nhất và khoảnh khắc cuối cùng |
| Serial position effect | Hiệu ứng vị trí — người dùng nhớ rõ nhất item đầu tiên và cuối cùng trong danh sách, hay quên phần giữa |
| Bandwagon effect | Hiệu ứng đám đông — xu hướng làm theo số đông. "10.000 người đã đăng ký" tạo social proof mạnh |
| Von Restorff effect | Hiệu ứng nổi bật — item khác biệt so với phần còn lại sẽ được ghi nhớ tốt hơn. Dùng để highlight CTA |
| Dark patterns | Thủ thuật lừa người dùng — thiết kế cố tình đánh lừa để người dùng làm điều họ không muốn (ví dụ: nút hủy bé xíu) |
| Social proof | Bằng chứng xã hội — sử dụng hành vi của người khác (đánh giá, số lượng user) để tạo niềm tin |
| Default bias | Thiên lệch mặc định — phần lớn người dùng giữ nguyên giá trị mặc định mà không thay đổi |

## Sources
- [Cognitive Biases in UX](https://www.nngroup.com/articles/cognitive-biases/) — NNGroup
- [Laws of UX](https://lawsofux.com/) — Jon Yablonski
- [Growth.Design Psychology](https://growth.design/psychology) — Dan Benoni & Louis-Xavier Lavallée
