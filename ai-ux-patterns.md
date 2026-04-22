# AI UX Patterns — Thiết kế cho sản phẩm AI

> Tổng hợp principles, patterns, và best practices để thiết kế interface cho AI products: chatbots, copilots, autonomous agents, và conversational UI.

## Overview

AI UX là lĩnh vực thiết kế đang phát triển nhanh nhất trong UX/UI (2024-2026). Khác với traditional UI nơi user click button và nhận kết quả deterministic, AI products yêu cầu designer xử lý **uncertainty** (kết quả không chắc chắn), **trust** (niềm tin), và **collaboration** (cộng tác human-AI). Khác với deterministic UI (giao diện cho kết quả cố định), AI output có thể thay đổi.

Sự chuyển đổi lớn nhất năm 2025-2026 là từ **Conversational UI** (giao diện hội thoại) sang **Delegative UI** (giao diện ủy quyền). User không còn chỉ "chat" với AI — họ **delegate** (ủy quyền) tasks cho AI agents (tác nhân AI tự hành) hoạt động tự chủ.

Ba nguồn tài liệu quan trọng nhất cho AI UX: **Google PAIR Guidebook**, **Microsoft HAX Toolkit** (18 Guidelines for Human-AI Interaction), và **Apple HIG Machine Learning**. Mỗi framework tiếp cận vấn đề từ góc độ khác nhau nhưng converge vào cùng core principles.

---

## 1. AI Interaction Models — Phổ tương tác Human-AI

### Automation Spectrum (phổ tự động hóa)

Có 4 mức độ AI interaction, từ passive đến fully autonomous (tự chủ hoàn toàn):

| Level | Model | Mô tả | Ví dụ thực tế |
|-------|-------|--------|----------------|
| **Assist** | Tool | AI gợi ý, user quyết định mọi thứ | Grammarly suggestions, autocomplete |
| **Copilot** | Collaborative partner | AI làm cùng user, user vẫn "lái" | GitHub Copilot, Notion AI, Figma AI |
| **Autopilot** | Supervised autonomy | AI tự thực hiện, user approve/reject | Linear auto-triage, email drafts |
| **Agent** | Delegated autonomy | AI tự lên kế hoạch + thực thi, user giám sát | Claude Computer Use, Devin, OpenAI Codex |

**Key insight**: Mức độ autonomy (tự chủ) càng cao thì yêu cầu về **transparency** (minh bạch), **control**, và **trust design** càng lớn. Không phải lúc nào "more autonomous" cũng tốt hơn — phải match với risk level của task.

### Ba mô hình kiến trúc UX (Microsoft)

Microsoft chia copilot UX thành 3 framework tích hợp:

1. **Immersive** (toàn màn hình) — Full-screen, toàn bộ canvas dành cho AI. Phù hợp dashboard, data analysis, deep exploration. Ví dụ: ChatGPT canvas mode, Microsoft Copilot for Security.
2. **Assistive** (hỗ trợ bên cạnh) — Side-panel hoặc sidebar, AI hỗ trợ bên cạnh workflow hiện tại. Ví dụ: GitHub Copilot Chat panel, Notion AI sidebar, Microsoft 365 Copilot.
3. **Embedded** (nhúng trong ngữ cảnh) — Single entry point, inline trong context. Ví dụ: Cursor inline suggestions, Gmail "Help me write", Linear AI auto-complete.

**Best practice**: Kết hợp **Assistive + Embedded** — dùng sidebar cho complex tasks và inline suggestions cho quick actions. Microsoft 365 Copilot thành công với 70% Fortune 500 nhờ mô hình **inline-style interaction** enhance workflow thay vì replace nó.

---

## 2. Trust & Transparency — Xây dựng niềm tin

### Tại sao trust quan trọng

Nghiên cứu (Smashing Magazine, 2025) chỉ ra **Trust Trap** (bẫy niềm tin) — sự mất cân bằng giữa confidence của user và capability thực sự của AI:
- **Under-trust** (tin quá ít): User không dùng feature hữu ích vì không tin AI
- **Over-trust** (tin quá nhiều): User phụ thuộc quá mức, không verify output

Nghiên cứu học thuật xác nhận: transparency levels cao hơn cải thiện trust (beta = .667), perceived reliability (beta = .595), confidence (beta = .553), và ease of understanding (beta = 1.161) — tất cả đều significant (p < .001).

### Patterns xây dựng Trust

#### a) Explainability (khả năng giải thích) — Giải thích quyết định
- **"Because you..." pattern**: "Vì bạn thường đọc về UX research, tôi gợi ý bài viết này" (Netflix, Spotify)
- **Source attribution** (dẫn nguồn): Hiển thị citations và direct quotes từ data sources (Perplexity AI, Microsoft Copilot)
- **Decision reasoning**: Show logic đằng sau recommendation, không chỉ kết quả (Google PAIR: "Explain for understanding, not completeness")

#### b) Confidence Indicators (chỉ báo độ tin cậy)
- Hiển thị uncertainty: "70% confident", "I might be wrong"
- Highlight phần output ít chắc chắn hơn
- Dùng visual cues (color coding, opacity) cho confidence levels
- **Ví dụ**: Claude sử dụng language hedging ("I think", "I'm not certain") thay vì assert mọi thứ

#### c) Error Handling (xử lý lỗi) — Xử lý lỗi gracefully (một cách mượt mà)
- Acknowledge errors humbly — không pretend AI luôn đúng
- Provide easy paths to correction
- Show "AI-generated — please review before sharing" disclaimers (tuyên bố miễn trừ)
- **Ví dụ**: ChatGPT disclaimer ở mỗi response, Notion AI cho phép undo/redo ngay lập tức

#### d) Appropriate Friction (ma sát có chủ đích)
Microsoft khuyến nghị **thêm friction** (không phải bớt!) tại những điểm quan trọng:
- Khi user save, share, copy AI-generated content
- Prompt user review trước khi "own" content
- Khuyến khích edit để thêm personal context
- **Ví dụ**: Microsoft Copilot hiện dialog "Be sure to review carefully before inserting — responses may contain inaccuracies"

### Microsoft HAX 18 Guidelines (4 giai đoạn)

**Initially (Lúc đầu):**
- G1: Make clear what the system can do
- G2: Make clear how well the system can do it

**During Interaction (Trong quá trình tương tác):**
- Match relevant social norms
- Mitigate social biases

**When Wrong (Khi sai):**
- Support efficient correction
- Make clear why the system did what it did

**Over Time (Theo thời gian):**
- Learn from user behavior
- Update and adapt cautiously
- Encourage granular feedback
- Provide global controls
- Convey consequences of user actions
- Notify users about changes

---

## 3. Human-AI Interaction Design

### Google PAIR Guidebook — 4 trụ cột

#### a) Mental Models (mô hình nhận thức)
- Hỏi: "User đang cố làm gì?" và "Mental model nào đã tồn tại?"
- Set realistic expectations từ đầu
- **Mô tả user benefits thay vì technology** — nói "tự động tóm tắt email dài" thay vì "sử dụng transformer-based NLP"
- Introduce features khi user thực sự cần dùng

#### b) Explainability + Trust
- Mức giải thích phù hợp giúp user hiểu system hoạt động thế nào
- Khi user có clear mental models → họ biết khi nào nên trust
- **Pattern**: "Explain for understanding, not completeness" — share info user cần để ra quyết định, không phải technical details

#### c) Feedback + Control
- User cần **control** AI dựa trên situation của họ
- Luôn cung cấp cách hoàn thành task **không dùng AI** (manual failsafe)
- Feedback từ user là critical để improve AI

#### d) Errors + Graceful Failure (thất bại mượt mà)
- Phát triển strategies để identify, diagnose, và communicate solutions cho errors
- AI sẽ sai — thiết kế cho failure, không phải chỉ success path (đường dẫn thành công)

### Prompt Design & Input Patterns

**Vấn đề**: Natural language typing chưa phải habit phổ biến. Nhiều user không biết phải type gì.

**Solutions** (Microsoft UX Guidance):
1. **Suggestion chips** (thẻ gợi ý): Hiển thị 3-4 example prompts (câu lệnh mẫu) ngay từ đầu (ChatGPT, Claude)
2. **Structured multi-step inputs**: Thay vì "Ask me anything", chia thành multiple fields (title, details, tone, audience)
3. **Smart defaults**: Pre-fill dựa trên usage history
4. **Prompt preview**: Cho user xem prompt trước khi submit
5. **Tone/style selectors**: Predefined options cho tone, length, format
6. **Multimodal input** (đầu vào đa phương thức): Voice + text + image upload + file attachment

**Ví dụ thực tế**:
- **ChatGPT**: 4 suggestion chips ở empty state, support image/file upload
- **Claude**: Project knowledge, conversation context, artifacts panel
- **Cursor**: Inline code context tự động, tab completion với preview
- **Notion AI**: Slash commands ("/summarize", "/translate"), tone selector

### Feedback Loops (vòng phản hồi)

**Collaborative UX** (Microsoft) = user guide AI qua continuous feedback loop giữa inputs và outputs:
- Thumbs up/down (ChatGPT, Claude)
- Quick-action buttons: "Make shorter", "Add detail", "More formal" (Notion AI)
- Inline editable output — user sửa trực tiếp result
- Show input + output together để user thấy correlation
- Keep history of prompts + outputs cho user quay lại
- **Ví dụ**: Claude Artifacts cho phép iterate trên cùng một output, giữ version history

---

## 4. AI Agent UX — Thiết kế cho Autonomous Agents

### Sự khác biệt căn bản

| Traditional UX | Agentic AI UX |
|---|---|
| User initiates, system responds | User delegates, system acts independently |
| Focus: usability | Focus: accountability, ethics, explainability |
| Errors: local, reversible | Errors: propagated, consequential |
| Control: assumed | Control: must be designed and perceived |
| Design screens | Design agency |

### Smashing Magazine Framework — 3 giai đoạn

#### Pre-Action (Consent — Đồng ý trước)
- **Intent Preview** (xem trước ý định): Show plan trước khi thực thi, với clear action options (approve/modify/reject)
- **Autonomy Dial** (nút chỉnh mức tự chủ): Cho user set mức độ independence của agent
- **Configuration design**: Prompt user suy nghĩ về desired outcomes, constraints, forbidden actions, risk levels

#### In-Action (Transparency — Minh bạch trong quá trình)
- **Explainable Rationale** (lý do giải thích được): Justify decisions dựa trên preferences của user
- **Confidence Signal** (tín hiệu độ tin cậy): Surface uncertainty để prevent automation bias (thiên lệch tự động hóa)
- **Progress signals**: Thay generic loaders bằng meaningful status ("Searching the web...", "Analyzing 3 documents...", "Writing draft...")

#### Post-Action (Safety — An toàn sau khi hoàn thành)
- **Action Audit & Undo** (nhật ký hành động & hoàn tác): Chronological log với easy reversal
- **Escalation Pathway** (đường dẫn leo thang): Agent hỏi clarification thay vì guess

### 7 UX Principles cho Agentic AI (UXmatters)

1. **Clarity of Intent**: Enable user communicate direction, limitations, exceptions — không chỉ goals
2. **Transparency as Affordance** (minh bạch như gợi ý sử dụng): Explanations trở thành primary interface. Dùng honest human language, tránh information overload (quá tải thông tin)
3. **Perceived Control**: User cần intervention capability dù hiếm khi dùng. "Control does not weaken autonomy, it legitimizes it"
4. **Continuous Feedback**: Transform invisible processing thành visible narrative
5. **Behavioral Personality Design**: Timing, intervention approach, risk escalation pace — tất cả tạo nên "personality" của agent
6. **Ethical Design as Operational Design**: Embed ethical constraints vào workflows, không chỉ policy documents. Audit logs, permission flows, action reversibility
7. **Human-Machine Collaboration**: AI suggest, human judge. Pause moments cho user engagement

### Phased Implementation

1. **Phase 1 — Foundational Safety**: AI chỉ suggest/propose, không tự action
2. **Phase 2 — Calibrated Autonomy**: Actions cần user confirmation
3. **Phase 3 — Proactive Delegation**: Pre-approved autonomous tasks cho low-risk operations

**Success Metrics**: >85% plan acceptance rate, <5% action reversal rate, calibration scores correlating confidence với user acceptance.

### Risk-based Authorization

- **Low-risk tasks** (formatting, summarizing): Auto-execute, notify after
- **Medium-risk tasks** (sending emails, editing documents): Preview + confirm
- **High-risk tasks** (financial transactions, data deletion): Multi-step approval + undo window

---

## 5. Conversational UI — Chat Interface Design

### Patterns hiện đại (2025-2026)

#### AI Assistant Cards
Thay vì traditional chat bubbles back-and-forth, dùng **separate cards/panels** cho complex outputs. Cards hỗ trợ: text, interactive elements, rich media, structured data, code blocks.
- **Ví dụ**: Claude Artifacts, ChatGPT Canvas, Cursor inline diffs

#### Streaming Responses (phản hồi truyền dần)
- Show text xuất hiện từng token — tạo cảm giác "AI đang suy nghĩ"
- Component states cần thiết: **loading**, **streaming**, **complete**, **error**, **confidence variants**
- Figma component system phù hợp cho multiple states này

#### Multimodal Interaction
Multimodal trở thành default expectation (2026):
- **Input**: Text + voice + image upload + file attachment + screen sharing
- **Output**: Text + code + images + charts + interactive widgets
- Kết hợp immediacy of voice với clarity of visual information
- **Ví dụ**: ChatGPT voice mode + vision, Claude file analysis, Gemini multimodal

#### Progressive Disclosure (tiết lộ dần dần)
- Reveal information step-by-step thay vì overwhelm
- Collapsible sections cho detailed explanations
- "Show more" cho sources/citations
- Summary first, details on demand

### Anti-patterns cần tránh

#### Over-Humanization (nhân hóa quá mức)
Microsoft cảnh báo **không** dùng ngôn ngữ anthropomorphic (nhân hóa):
- Tránh: "I understand", "I think", "I feel"
- Dùng: "Processing", "Analyzing", "Based on the data"
- First-person singular (I, me) OK vì conversational
- **Không** dùng "we" để đại diện company — AI không nên "speak on behalf of" tổ chức

#### "Ask Me Anything" Trap
Empty text field không hướng dẫn = user paralysis. Luôn cung cấp:
- Suggestion chips với example prompts
- Contextual suggestions dựa trên current content
- Quick actions (summarize, translate, explain)

#### Hidden Uncertainty
Không bao giờ để AI sound 100% confident khi không phải. Luôn include:
- AI-generated disclaimers
- Confidence indicators khi applicable
- Links to sources

---

## 6. AI Onboarding — Dạy user dùng AI

### Empty State Design cho AI

Empty state (trạng thái trống) là **critical moment** cho AI products — user mới không biết AI có thể làm gì.

**Best practices**:
1. **4 diverse example prompts**: Showcase variety of actions AI có thể thực hiện. Ví dụ ChatGPT hiển thị 4 chips covering different use cases
2. **Capability overview**: "I can help you with..." list rõ ràng
3. **Progressive onboarding**: Introduce features khi user thực sự cần, không dump tất cả lúc đầu
4. **Sample/pre-loaded data**: Cho user thấy AI output trước khi phải type anything
5. **Interactive walkthrough**: Guided tour showing capability ranges

### Teaching Prompt Craft

- **Show before-after**: Hiển thị "basic prompt" vs "detailed prompt" và difference in output quality
- **Prompt templates**: Pre-built templates cho common tasks
- **Inline suggestions**: "Try adding more context about..." khi prompt quá vague
- **Capability boundaries**: Nói rõ AI KHÔNG THỂ làm gì, không chỉ có thể làm gì

### Calibration (hiệu chỉnh ban đầu) (Apple HIG)

Apple khuyến nghị:
- Dùng **calibration** chỉ khi feature không thể hoạt động thiếu initial information
- Ưu tiên **implicit feedback** (observe user behavior) hơn **explicit feedback** (hỏi user trực tiếp)
- Khi cần explicit feedback: cho user explicit goal + show progress towards it
- Evolve user model over time mà không cần re-calibrate

---

## 7. Emerging Concepts (2026)

### Machine Experience (MX) Design (thiết kế trải nghiệm cho máy)
Thiết kế không chỉ cho humans mà còn cho **AI agents as users**:
- APIs, data structures, documentation optimized cho AI consumption
- NNGroup đã bắt đầu viết về "AI Agents as Users" — AI cần navigate systems, consume content, take actions
- MX sẽ trở thành discipline riêng song song với UX

### Delegative UI
Shift từ "asking AI a question" sang "assigning AI a goal":
- Users express **intentions** thay vì **instructions**
- UI cần support goal-setting, constraint-defining, và progress-monitoring
- **Ví dụ**: Claude Projects (set context + goals), Cursor background agents, Devin autonomous coding

### Multi-Agent Orchestration (điều phối đa tác nhân)
Khi nhiều AI agents cộng tác:
- Task distribution visibility
- Agent conflict resolution
- Responsibility recognition
- System overview maintenance
- Shift từ interaction design sang **systems thinking** và **orchestration architecture**

---

## Examples — Sản phẩm thực tế

### ChatGPT (OpenAI)
- **UI**: Minimalist chat window, collapsible sidebar, suggestion chips
- **Trust**: Disclaimer mỗi response, model selector, memory controls
- **Innovation**: Canvas mode (collaborative editing), voice mode, image generation inline
- **Onboarding**: 4 example prompts, capability hints

### Claude (Anthropic)
- **UI**: Two-column layout, purple accents, Artifacts panel cho rich output
- **Trust**: Language hedging, source citations, honest about limitations
- **Innovation**: Projects (persistent context), extended thinking visibility, computer use
- **Adoption**: #2 weekly tool trong design workflows sau Figma (2026)

### GitHub Copilot
- **Model**: Embedded (inline suggestions) + Assistive (chat panel)
- **Trust**: Tab to accept, easy dismiss, diff preview
- **Pattern**: Ghost text (chữ mờ gợi ý) suggestions — không intrusive (xâm phạm), user opt-in mỗi suggestion

### Cursor
- **Model**: Embedded + Immersive
- **Innovation**: Inline diffs (so sánh thay đổi ngay tại chỗ), multi-file edits, background agents, tab completion với context awareness
- **Trust**: Clear diff view showing exactly what changes, easy accept/reject per change

### Notion AI
- **Model**: Embedded (slash commands) + Assistive (sidebar)
- **Pattern**: Context-aware — AI biết content hiện tại, database structure
- **Innovation**: AI Agents (2025-2026) tự execute work, không chỉ suggest
- **Onboarding**: Slash command discoverable trong existing workflow

### Linear
- **Model**: Autopilot — AI tự triage, label, assign issues
- **Pattern**: AI works in background, user reviews results
- **Trust**: Transparent labeling of AI-generated content, easy override

---

## Related
- [[design-principles]] — Nielsen's Heuristics áp dụng cho AI (visibility of system status, error recovery)
- [[common-ui-patterns]] — Traditional patterns được adapt cho AI context
- [[micro-interactions]] — Streaming animations, loading states, confidence indicators
- [[accessibility-basics]] — AI features phải accessible (screen readers, keyboard navigation)
- [[cognitive-biases]] — Automation bias, anchoring bias trong AI context
- [[navigation-patterns]] — Conversation history, agent task navigation

---

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Deterministic UI | Giao diện cho kết quả cố định — cùng input luôn cho cùng output. Khác với AI nơi kết quả có thể thay đổi |
| Automation Spectrum | Phổ tự động hóa — 4 mức độ từ Assist (gợi ý) đến Agent (tự chủ hoàn toàn), mỗi mức yêu cầu thiết kế trust khác nhau |
| Copilot | Mô hình AI làm cùng người dùng như đối tác, người dùng vẫn kiểm soát và ra quyết định chính |
| Agentic AI | AI tự chủ — AI có khả năng tự lên kế hoạch và thực thi nhiệm vụ, người dùng giám sát thay vì điều khiển trực tiếp |
| Delegative UI | Giao diện ủy quyền — người dùng giao mục tiêu cho AI thay vì chỉ dẫn từng bước. Xu hướng chính 2025-2026 |
| Trust Trap | Bẫy niềm tin — sự mất cân bằng giữa mức tin tưởng của người dùng và khả năng thực sự của AI (tin quá nhiều hoặc quá ít) |
| Explainability | Khả năng giải thích — AI cho người dùng biết tại sao đưa ra quyết định/gợi ý đó, không chỉ hiện kết quả |
| Confidence indicators | Chỉ báo độ tin cậy — tín hiệu trực quan cho người dùng biết AI chắc chắn đến đâu về câu trả lời |
| Source attribution | Dẫn nguồn — hiển thị trích dẫn và link nguồn gốc của thông tin AI cung cấp, giúp người dùng xác minh |
| Suggestion chips | Thẻ gợi ý — các nút nhỏ hiển thị câu prompt mẫu, giúp người dùng mới biết phải bắt đầu từ đâu |
| Streaming responses | Phản hồi truyền dần — text xuất hiện từng phần thay vì đợi hoàn thành rồi hiện một lúc, tạo cảm giác AI đang suy nghĩ |
| Ghost text | Chữ mờ gợi ý — text nhạt hiện trước cho người dùng xem trước gợi ý của AI, nhấn Tab để chấp nhận |
| Multimodal | Đa phương thức — hỗ trợ nhiều loại input/output cùng lúc: text, giọng nói, hình ảnh, file, code |
| Hallucination | Hiện tượng AI tạo ra thông tin sai nhưng trình bày rất tự tin như thật. Cần disclaimers và source citation để giảm thiểu |
| Calibration | Hiệu chỉnh ban đầu — quá trình thu thập thông tin từ người dùng lần đầu để AI cá nhân hóa trải nghiệm |
| Mental model | Mô hình nhận thức — cách người dùng hình dung hệ thống hoạt động trong đầu. AI cần set đúng kỳ vọng từ đầu |
| Machine Experience (MX) | Thiết kế trải nghiệm cho máy — discipline mới thiết kế API và data structures tối ưu cho AI agents sử dụng |
| Orchestration | Điều phối đa tác nhân — quản lý nhiều AI agents cùng phối hợp thực hiện một nhiệm vụ phức tạp |
| Dark patterns | Thủ thuật thiết kế lừa người dùng làm điều họ không muốn. Trong AI context: che giấu uncertainty hoặc over-humanize |
| Anthropomorphic | Nhân hóa — gán đặc tính con người cho AI (nói "tôi cảm thấy", "tôi hiểu"). Microsoft khuyến cáo nên tránh |

## Sources

### Frameworks & Guidelines chính thức
- [Google PAIR Guidebook](https://pair.withgoogle.com/guidebook/) — Comprehensive toolkit cho human-centered AI design
- [Google PAIR Patterns](https://pair.withgoogle.com/guidebook/patterns) — Design patterns từ Google PAIR
- [Microsoft HAX Toolkit](https://www.microsoft.com/en-us/haxtoolkit/) — 18 Guidelines for Human-AI Interaction
- [Microsoft HAX Design Patterns](https://www.microsoft.com/en-us/haxtoolkit/design-patterns/) — Actionable solutions cho recurring human-AI interaction problems
- [Microsoft Copilot UX Guidance](https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/ux-guidance) — Dynamic UX cho generative AI applications
- [Apple HIG — Machine Learning](https://developer.apple.com/design/human-interface-guidelines/machine-learning) — Apple guidelines cho ML features
- [Guidelines for Human-AI Interaction (CHI 2019 Paper)](https://dl.acm.org/doi/10.1145/3290605.3300233) — Original research paper, 18 guidelines

### Articles & Analysis
- [Designing For Agentic AI: Practical UX Patterns — Smashing Magazine (Feb 2026)](https://www.smashingmagazine.com/2026/02/designing-agentic-ai-practical-ux-patterns/) — Pre-Action, In-Action, Post-Action patterns
- [Identifying Necessary Transparency Moments in Agentic AI — Smashing Magazine (Apr 2026)](https://www.smashingmagazine.com/2026/04/identifying-necessary-transparency-moments-agentic-ai-part1/) — Transparency decision framework
- [The Psychology of Trust in AI — Smashing Magazine (Sep 2025)](https://www.smashingmagazine.com/2025/09/psychology-trust-ai-guide-measuring-designing-user-confidence/) — Trust Trap, measuring confidence
- [Designing for Autonomy: UX Principles for Agentic AI — UXmatters (Dec 2025)](https://www.uxmatters.com/mt/archives/2025/12/designing-for-autonomy-ux-principles-for-agentic-ai.php) — 7 UX principles cho agentic AI
- [AI Copilot UX Best Practices — Groto (2025-26)](https://www.letsgroto.com/blog/mastering-ai-copilot-design) — Trust, collaboration, anti-patterns
- [State of UX 2026 — NNGroup](https://www.nngroup.com/articles/state-of-ux-2026/) — AI trends trong UX landscape
- [AI Agents as Users — NNGroup](https://www.nngroup.com/articles/ai-agents-as-users/) — Machine Experience design
- [NNGroup AI Topic](https://www.nngroup.com/topic/ai/) — Tổng hợp articles về AI UX
- [Conversational UI Design Patterns — AI UX Design Guide](https://www.aiuxdesign.guide/patterns/conversational-ui) — Chat interface patterns
- [AI-driven UX Design Patterns — LogRocket](https://blog.logrocket.com/ux-design/ai-driven-ux-design-patterns/) — Practical AI feature design
- [Designing UX for AI Agents — Aubergine (2025)](https://www.aubergine.co/insights/designing-for-ai-agents) — Human-centered approach cho agents
- [Designing UX for AI Agents That Act on Behalf of Users — Bootcamp/Medium (2026)](https://medium.com/design-bootcamp/designing-ux-for-ai-agents-that-act-on-behalf-of-users-2256bf02949c) — Delegation UX patterns
- [Predictions for Conversation Design 2026 — Conversation Design Institute](https://www.conversationdesigninstitute.com/blog/predictions-for-conversation-design-2026-and-beyond) — Future of conversational UI
- [Jakob Nielsen 18 Predictions for 2026](https://jakobnielsenphd.substack.com/p/2026-predictions) — AI agents, delegative UI trends
