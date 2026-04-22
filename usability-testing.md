# Usability Testing

> Watch real users use your design. Humble yourself. Fix what's broken.

## Overview

Usability testing (kiểm thử khả năng sử dụng) là cho real users thử dùng design/prototype (bản mẫu thử nghiệm) và quan sát họ. Đây là cách nhanh nhất để phát hiện vấn đề mà bạn (designer) không thấy vì bạn biết quá rõ sản phẩm. 5 users, 30 min mỗi người = phát hiện ~85% issues.

## Key Points

### Testing Methods
| Method | Fidelity | When |
|--------|---------|------|
| Paper prototype test | Low | Early concept |
| Figma prototype test | Medium | After wireframes |
| Staged environment test | High | Before launch |
| Live product test | Production | Post-launch |

### Running a Test
1. **Define tasks**: 3-5 realistic scenarios ("Book a flight from HCM to Hanoi for next Friday")
2. **Recruit participants**: Match your personas, 5 per round
3. **Facilitate**: "Think out loud" protocol. ĐỪNG giúp, ĐỪNG giải thích
4. **Observe**: Note where they hesitate, get confused, or fail
5. **Debrief**: Ask follow-up questions after tasks
6. **Synthesize**: Group findings, prioritize by severity

### Metrics
- **Task success rate** — % users complete the task
- **Time on task** — How long it takes
- **Error rate** — Number of wrong actions
- **SUS score** — System Usability Scale (thang đo khả năng sử dụng) (quick survey, score /100)
- **NPS** — Net Promoter Score (chỉ số sẵn lòng giới thiệu) (would you recommend?)

### Remote vs In-person
- **Remote unmoderated** (Maze, UserTesting): Scale, cheap, async. Less insight depth
- **Remote moderated** (Zoom): Good balance, can follow up
- **In-person**: Richest data, see body language. Expensive, hard to recruit

### Common Findings (almost always)
- Users don't read — they scan
- Users don't use nav the way you expect
- Naming/labels confuse people
- Users find creative workarounds you didn't imagine

## Related
- [[user-research-methods]]
- [[personas-and-jtbd]]
- [[design-principles]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Usability testing | Kiểm thử khả năng sử dụng — cho người dùng thật thử dùng sản phẩm/prototype và quan sát để tìm vấn đề |
| Prototype | Bản mẫu thử nghiệm — phiên bản sơ bộ của sản phẩm dùng để test ý tưởng trước khi xây dựng thật |
| Fidelity | Mức độ chi tiết của prototype: low-fi (sơ khai, giấy), medium-fi (Figma), high-fi (gần như thật) |
| Think-aloud protocol | Phương pháp yêu cầu người dùng nói to suy nghĩ khi thực hiện task, giúp hiểu quá trình ra quyết định của họ |
| Task success rate | Tỷ lệ hoàn thành nhiệm vụ — phần trăm người dùng có thể hoàn thành task được giao thành công |
| SUS score | System Usability Scale — bảng khảo sát nhanh 10 câu cho điểm từ 0-100, đánh giá mức độ dễ dùng tổng thể |
| NPS | Net Promoter Score — chỉ số đo lường mức độ sẵn lòng giới thiệu sản phẩm cho người khác, từ -100 đến 100 |
| Remote unmoderated | Test từ xa không có người hướng dẫn — người dùng tự làm task qua tool online, tiết kiệm chi phí nhưng ít insight sâu |
| Remote moderated | Test từ xa có người hướng dẫn — qua Zoom hoặc video call, có thể hỏi thêm và quan sát phản ứng |
| Synthesize | Tổng hợp — gom kết quả từ nhiều phiên test lại, phân nhóm vấn đề và xếp ưu tiên theo mức độ nghiêm trọng |

## Sources
- [Don't Make Me Think](https://sensible.com/dont-make-me-think/) — Steve Krug
- [Rocket Surgery Made Easy](https://sensible.com/rocket-surgery-made-easy/) — Steve Krug
