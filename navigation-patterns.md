# Navigation Patterns

> Information Architecture + Navigation = user tìm được cái họ cần.

## Overview

Navigation là cách user di chuyển trong app. IA (Information Architecture) là cách bạn tổ chức content. Navigation tốt = user KHÔNG BAO GIỜ cảm thấy lạc. Nếu user phải nghĩ "tôi đang ở đâu?" — navigation đã fail.

## Key Points

### Navigation Types
- **Global nav** — Luôn visible, access main sections (top bar, sidebar)
- **Local nav** — Navigate within a section (tabs, sub-menu)
- **Contextual nav** — Links inline trong content
- **Utility nav** — Settings, profile, help (usually top-right)
- **Search** — Fallback khi nav structure không đủ

### Mobile Navigation
- **Bottom tabs** (3-5 items): iOS/Android standard. Thumb-friendly
- **Hamburger menu**: Controversial — hides options. Dùng khi >5 sections
- **Tab bar + More**: 4 tabs + "More" tab cho items còn lại
- **Gesture-based**: Swipe between sections (có learning curve)

### Desktop Patterns
- **Persistent sidebar**: Best cho complex apps (Notion, Slack, Figma)
- **Collapsible sidebar**: Maximize content area khi cần
- **Top horizontal nav**: Best cho marketing sites, simple apps
- **Command palette (Cmd+K)**: Power user navigation, search-first

### IA Principles
- **Progressive disclosure**: Show high-level first, drill down for details
- **Card sorting**: Let users organize content → reveals their mental model
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

## Sources
- [Information Architecture](https://www.nngroup.com/articles/ia-vs-navigation/) — NNGroup
- [Navigation Design](https://www.smashingmagazine.com/2017/04/overview-responsive-navigation-patterns/) — Smashing Magazine
