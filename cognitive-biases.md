# Cognitive Biases trong Design

> Những thiên lệch nhận thức ảnh hưởng đến cách user ra quyết định và tương tác với sản phẩm.

## Overview

Cognitive biases là các "shortcuts" trong não bộ giúp con người xử lý thông tin nhanh hơn, nhưng đôi khi dẫn đến quyết định không hợp lý. Designer cần hiểu biases để: (1) thiết kế thuận theo cách não bộ hoạt động, và (2) tránh manipulate user một cách phi đạo đức.

## Key Points

### Biases quan trọng nhất cho UX

- **Anchoring** — Thông tin đầu tiên user thấy sẽ "neo" mọi đánh giá sau đó. Pricing pages đặt plan đắt nhất trước để plan giữa trông "hợp lý"
- **Loss aversion** — Mất mát đau gấp 2x so với niềm vui khi được. "Your trial expires in 3 days" mạnh hơn "Subscribe to keep features"
- **Serial position effect** — User nhớ item đầu và cuối danh sách rõ nhất. Đặt actions quan trọng ở đầu/cuối nav
- **Hick's Law** — Nhiều lựa chọn = thời gian quyết định lâu hơn = drop-off cao hơn. Giảm options
- **Fitts's Law** — Target lớn hơn + gần hơn = dễ click hơn. CTA buttons phải to và dễ reach
- **Peak-end rule** — User đánh giá trải nghiệm dựa trên peak moment và ending, không phải average. Nail the ending
- **Bandwagon effect** — "10,000 people signed up today" — social proof works
- **Default bias** — Phần lớn user giữ nguyên default. Chọn defaults cẩn thận, ethically
- **Von Restorff effect** — Item khác biệt trong nhóm sẽ được nhớ. Highlight CTA bằng color contrast

### Ethical considerations
- Biases có thể bị lạm dụng thành **dark patterns**
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

## Sources
- [Cognitive Biases in UX](https://www.nngroup.com/articles/cognitive-biases/) — NNGroup
- [Laws of UX](https://lawsofux.com/) — Jon Yablonski
- [Growth.Design Psychology](https://growth.design/psychology) — Dan Benoni & Louis-Xavier Lavallée
