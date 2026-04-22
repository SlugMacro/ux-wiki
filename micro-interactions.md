# Micro-interactions

> Những chi tiết nhỏ tạo nên trải nghiệm lớn — animation, feedback, delight.

## Overview

Micro-interactions là các animation/feedback nhỏ xảy ra khi user tương tác với UI: button hover, toggle switch, loading state, pull-to-refresh. Chúng làm interface feel "alive" và communicative. Rule: **functional first, delightful second**.

## Key Points

### 4 Parts of a Micro-interaction (Dan Saffer)
1. **Trigger** — Gì khởi tạo (user click, system event)
2. **Rules** — Gì xảy ra (logic behind the interaction)
3. **Feedback** — User thấy/nghe/cảm nhận gì
4. **Loops & Modes** — Gì xảy ra nếu lặp lại hoặc trong conditions khác

### Animation Principles cho UI
- **Duration**: 150-300ms cho most transitions. <100ms feels instant, >500ms feels slow
- **Easing**: ease-out cho entrances, ease-in cho exits, ease-in-out cho moves
- **Stagger**: Danh sách items animate lần lượt (20-50ms delay between items)
- **Transform only**: Animate `transform` và `opacity` — browser tối ưu nhất

### Common Micro-interactions
| Interaction | Purpose |
|------------|---------|
| Button press (scale down) | Confirm tap received |
| Skeleton → content | Reduce perceived load time |
| Toggle switch | Immediate state feedback |
| Pull to refresh | Trigger + progress feedback |
| Swipe to delete | Direct manipulation |
| Page transitions | Spatial orientation |
| Toast slide-in | Non-intrusive notification |
| Hover state | Indicate interactivity |

### When NOT to animate
- User đang typing hoặc editing (distracting)
- Repeated actions (toast mỗi lần save = annoying)
- Khi user đã tắt `prefers-reduced-motion`
- Performance-sensitive contexts (low-end devices)

### prefers-reduced-motion
```css
@media (prefers-reduced-motion: reduce) {
  * { animation-duration: 0.01ms !important; }
}
```
Always respect this media query — some users have vestibular disorders.

## Examples

- **Stripe**: Gradient animation trên hero, subtle nhưng memorable
- **Linear**: Transitions cực smooth giữa views, spatial consistency
- **Telegram**: Message send animation + checkmarks = satisfying feedback loop

## Related
- [[common-ui-patterns]]
- [[design-principles]]
- [[accessibility-basics]]
- [[ai-ux-patterns]] — Streaming animations, AI loading states, confidence visual cues, agent progress indicators

## Sources
- [Microinteractions](https://microinteractions.com/) — Dan Saffer
- [Motion Design Principles](https://m3.material.io/styles/motion/overview) — Material Design 3
- [Animation Handbook](https://www.designbetter.co/animation-handbook) — InVision
