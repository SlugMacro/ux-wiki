# Design Systems

> Bộ quy chuẩn thiết kế toàn diện — từ tokens, components, patterns đến documentation — giúp team xây dựng sản phẩm nhất quán và hiệu quả.

## Overview

Design System (hệ thống thiết kế) là tập hợp các reusable components (thành phần tái sử dụng), design tokens (biến thiết kế), patterns (mẫu thiết kế), guidelines (hướng dẫn), và documentation (tài liệu) — tất cả được tổ chức thành một single source of truth (nguồn dữ liệu duy nhất) cho toàn bộ team product. Nó không chỉ là component library — mà là cả ngôn ngữ chung giữa designer, developer, PM, và content writer.

Tại sao cần Design System? Khi sản phẩm scale (mở rộng), không có hệ thống thiết kế sẽ dẫn đến inconsistency (không nhất quán): mỗi designer tạo button khác nhau, mỗi developer code padding khác nhau, mỗi page nhìn như một app khác. Design System giải quyết vấn đề này bằng cách cung cấp shared vocabulary (từ vựng chung) và building blocks (khối xây dựng) để mọi người cùng "nói một ngôn ngữ". Kết quả: ship nhanh hơn, consistent hơn, onboard người mới dễ hơn.

Không phải lúc nào cũng cần build Design System đầy đủ. Nếu team chỉ có 1-2 người, một Figma library nhỏ + shared component folder là đủ. Design System nên được invest khi: team >= 3 designers hoặc >= 5 developers, sản phẩm có nhiều surfaces (web, mobile, internal tools), hoặc khi inconsistency đã trở thành pain point rõ ràng.

## Key Points

### Thành phần của Design System

```
Design System
├── 🎨 Design Tokens — Colors, spacing, typography, shadows, motion
├── 🧱 Components — Button, Input, Card, Modal, Table...
├── 📐 Patterns — Form patterns, navigation patterns, data display
├── 📝 Documentation — Usage guidelines, do/don't, accessibility notes
├── 🔧 Tooling — Figma library, Storybook, token pipeline
└── 📏 Guidelines — Brand, voice & tone, iconography, illustration
```

### Design Tokens — Nền tảng

Design tokens là layer thấp nhất, định nghĩa mọi visual decision:

- **Global tokens**: Giá trị raw — `blue-500: #3B82F6`, `spacing-4: 16px`
- **Alias/Semantic tokens**: Gán ý nghĩa — `color-primary: {blue-500}`, `color-bg-surface: {white}`
- **Component tokens**: Gắn vào component — `button-bg: {color-primary}`

Chi tiết xem [[design-tokens]].

### Components — Building Blocks

Components trong Design System phải:

- **Accessible** (truy cập được): ARIA roles, keyboard navigation, focus management
- **Themeable** (tùy chỉnh giao diện được): Dùng tokens, không hardcode colors
- **Composable** (kết hợp được): Slots/children pattern, không config-heavy
- **Well-documented**: Props table, examples, do/don't, edge cases

Chi tiết về API design xem [[component-api-design]], về cấu trúc phân cấp xem [[atomic-design]].

### Patterns — Giải pháp cho bài toán lặp lại

Patterns khác components ở chỗ chúng mô tả **cách kết hợp** components:

- **Form pattern**: Layout, validation messages, error states, submit flow
- **Empty state pattern**: Illustration + message + CTA
- **Loading pattern**: Skeleton, spinner, progressive loading
- **Data table pattern**: Sorting, filtering, pagination, bulk actions

### Documentation — Yếu tố sống còn

Không có docs = không có adoption. Docs tốt cần:

- **Usage guidelines**: Khi nào dùng component A thay vì B
- **Do / Don't**: Visual examples rõ ràng
- **Code examples**: Copy-paste ready
- **Accessibility notes**: WCAG requirements cho từng component
- **Changelog**: Breaking changes, migration guides

### Xây dựng Design System — Bắt đầu từ đâu

**Bước 1: UI Audit (kiểm tra giao diện hiện tại)**
- Screenshot toàn bộ screens hiện có
- Nhóm các elements tương tự (bao nhiêu kiểu button? bao nhiêu shade of blue?)
- Identify inconsistencies và redundancies

**Bước 2: Define Foundations**
- Thiết lập color palette, typography scale, spacing scale
- Tạo design tokens từ các giá trị đã audit
- Setup Figma variables / CSS custom properties

**Bước 3: Build Core Components**
- Bắt đầu từ các components dùng nhiều nhất: Button, Input, Select, Card, Modal
- Mỗi component cần: Figma component + Code component + Documentation
- Đừng build hết một lúc — ship incrementally (từng bước)

**Bước 4: Document & Publish**
- Setup Storybook hoặc docs site
- Viết usage guidelines cho mỗi component
- Tạo contribution guide (hướng dẫn đóng góp)

### Governance — Ai quản lý, ai contribute

**Ownership models:**

| Model | Mô tả | Phù hợp khi |
|-------|--------|-------------|
| **Centralized** (tập trung) | Dedicated DS team own everything | Company lớn, >= 50 devs |
| **Federated** (liên bang) | Core team + contributors từ product teams | Mid-size, 10-50 devs |
| **Community** (cộng đồng) | Mọi người contribute, core team review | Startup, open source |

**Contribution workflow:**
1. Proposal (đề xuất): Mô tả component mới / thay đổi + use cases
2. Design review: Design team approve visual + UX
3. Implementation: Code + tests + docs
4. Review: Core team review code + accessibility
5. Release: Versioned release + changelog

**Versioning (quản lý phiên bản):**
- Semantic versioning: `MAJOR.MINOR.PATCH`
- MAJOR = breaking changes (thay đổi không tương thích ngược)
- MINOR = new features, backwards compatible (tính năng mới, tương thích ngược)
- PATCH = bug fixes

### Adoption — Rollout và đo lường

**Rollout strategy:**
1. **Pilot** (thử nghiệm): Chọn 1 team/feature áp dụng trước
2. **Early adopters**: Mở rộng ra 2-3 teams, thu thập feedback
3. **Broad adoption**: Company-wide, migration guides cho legacy code
4. **Enforcement**: Lint rules, PR checks, deprecation warnings

**Measure success (đo lường thành công):**
- **Adoption rate**: % components sử dụng DS vs custom
- **Design consistency score**: Visual audit định kỳ
- **Developer satisfaction**: Survey quarterly
- **Time to build**: So sánh thời gian build feature trước/sau DS
- **Bug reduction**: Fewer UI bugs liên quan đến inconsistency

**Handle resistance (xử lý phản đối):**
- "DS quá rigid" → Cho phép customization thông qua tokens + composition
- "Tốn thời gian quá" → Show metrics về time saved sau adoption
- "Không fit use case của tôi" → Tạo escape hatch (lối thoát), nhưng track usage
- "Component thiếu feature" → Contribution process rõ ràng, response time nhanh

## Examples

### Design Systems nổi tiếng

| Design System | Company | Đặc điểm nổi bật |
|---------------|---------|-------------------|
| **Material Design 3** | Google | Comprehensive, dynamic color, cross-platform. Quá lớn — dễ bị "mọi app nhìn giống Google" |
| **Apple HIG** | Apple | Platform-native guidelines, không phải component library. Focus on principles hơn implementation |
| **Ant Design** | Ant Group | Full-featured React library, enterprise-focused. Token system mạnh từ v5 |
| **Polaris** | Shopify | Excellent documentation, clear guidelines. Gold standard cho DS docs |
| **Carbon** | IBM | Accessibility-first, enterprise scale. Grid system xuất sắc |
| **Chakra UI** | Community | Developer experience tuyệt vời, style props approach |
| **shadcn/ui** | Community | Copy-paste components, bạn own the code. Không phải npm package — bạn customize trực tiếp |
| **Radix UI** | WorkOS | Headless primitives, accessibility baked in. Foundation cho shadcn/ui |
| **Atlassian Design System** | Atlassian | Mature system, design tokens mạnh, real-world tested ở scale lớn |
| **Spectrum** | Adobe | Cross-platform (web + React Native), accessible, token-based theming |

### Real Product Examples

**Shopify Polaris — Mẫu mực về Documentation:**
- Mỗi component có: purpose, best practices, content guidelines, accessibility, related components
- "Do / Don't" examples rất trực quan
- Public Figma library sync với code 1:1

**shadcn/ui — Paradigm shift:**
- Không install package — chạy CLI copy component vào project
- Bạn own code, customize thoải mái
- Built on Radix primitives + Tailwind CSS
- Trend 2024-2025: nhiều teams chuyển từ traditional DS sang approach này

**Material Design 3 — Dynamic Color:**
- Tạo color palette từ 1 seed color
- Material You: user wallpaper → auto-generate app theme
- Token structure: `md.sys.color.primary` → `md.ref.palette.primary40`

### Tools Ecosystem

**Design side:**
- **Figma** — Component library + Variables (tokens) + Prototyping
- **Token Studio** (Figma plugin) — Quản lý design tokens nâng cao, sync với code
- **Supernova** — DS documentation platform, auto-generate docs từ Figma

**Development side:**
- **Storybook** — Component development + documentation + visual testing
- **Chromatic** — Visual regression testing (kiểm tra thay đổi giao diện), review tool cho Storybook
- **Style Dictionary** (Amazon) — Transform tokens từ JSON sang CSS, iOS, Android
- **Turbo/Nx** — Monorepo tools cho DS packages

**Documentation:**
- **Storybook Docs** — Auto-generate docs từ component code
- **Docusaurus** — Custom docs site
- **Zeroheight** — Design system documentation platform

**Token pipeline example:**
```
Figma Variables
    ↓ (Token Studio export)
tokens.json
    ↓ (Style Dictionary transform)
├── CSS variables
├── Tailwind theme
├── iOS Swift constants
└── Android XML resources
```

## Related
- [[design-tokens]]
- [[atomic-design]]
- [[component-api-design]]
- [[figma-workflow]]
- [[design-to-dev-handoff]]
- [[color-theory]]
- [[typography]]
- [[spacing-system]]
- [[accessibility-basics]]

## Thuật ngữ

| Thuật ngữ | Giải thích |
|-----------|-----------|
| Design System | Hệ thống thiết kế — tập hợp các thành phần, quy tắc, và tài liệu giúp xây dựng sản phẩm nhất quán |
| Design Tokens | Biến thiết kế — các giá trị được đặt tên đại diện cho quyết định thiết kế (màu sắc, spacing, typography) |
| Component Library | Thư viện thành phần — tập hợp các UI components tái sử dụng đã được code sẵn |
| Pattern Library | Thư viện mẫu — tập hợp các giải pháp thiết kế cho bài toán UX lặp lại (form, empty state, loading) |
| Governance | Quản trị — quy trình quản lý, đóng góp, và ra quyết định cho Design System |
| Semantic Versioning | Quản lý phiên bản theo ngữ nghĩa — MAJOR.MINOR.PATCH, giúp tracking breaking changes |
| Headless Components | Thành phần không có giao diện sẵn — chỉ cung cấp logic và accessibility, bạn tự style |
| Composition Pattern | Mẫu kết hợp — xây dựng component phức tạp bằng cách lồng các component nhỏ hơn thay vì dùng nhiều props |
| UI Audit | Kiểm tra giao diện — quá trình screenshot và phân loại tất cả UI elements hiện có để tìm inconsistency |
| Style Dictionary | Công cụ của Amazon chuyển đổi design tokens từ định dạng JSON sang các platform khác nhau (CSS, iOS, Android) |
| Storybook | Công cụ phát triển và tài liệu hóa components trong môi trường isolated (tách biệt) |
| Visual Regression Testing | Kiểm tra hồi quy trực quan — so sánh screenshot trước/sau để phát hiện thay đổi giao diện không mong muốn |
| Contribution Model | Mô hình đóng góp — quy trình để thành viên ngoài core team đề xuất và thêm components mới |

## Sources
- [Design Systems Handbook](https://www.designbetter.co/design-systems-handbook) — InVision, tổng quan toàn diện về DS
- [Atomic Design](https://atomicdesign.bradfrost.com/) — Brad Frost, methodology nền tảng
- [Material Design 3](https://m3.material.io/) — Google, design system reference lớn nhất
- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/) — Apple, platform-native guidelines
- [Polaris](https://polaris.shopify.com/) — Shopify, mẫu mực về documentation
- [Carbon Design System](https://carbondesignsystem.com/) — IBM, enterprise-grade DS
- [shadcn/ui](https://ui.shadcn.com/) — Copy-paste component approach
- [Radix UI](https://www.radix-ui.com/) — Headless primitives, accessibility-first
- [Design Tokens W3C Draft](https://www.w3.org/community/design-tokens/) — W3C, token specification
- [Storybook](https://storybook.js.org/) — Component development environment
- [The State of Design Systems 2024](https://www.figma.com/blog/design-systems/) — Figma blog, trends và insights
- [Style Dictionary](https://amzn.github.io/style-dictionary/) — Amazon, token transformation tool
