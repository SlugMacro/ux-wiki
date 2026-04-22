# UX/UI Design Wiki — Schema

## Purpose
Personal knowledge base về UX/UI Design. Biên soạn, liên kết, và duy trì kiến thức từ sách, articles, courses, và kinh nghiệm thực tế.

## Categories

### Foundations
- **Principles** — Design principles, heuristics, mental models
- **Psychology** — Cognitive biases, Gestalt, perception, behavior patterns
- **Accessibility** — WCAG, inclusive design, assistive tech

### Visual Design
- **Typography** — Type systems, pairing, hierarchy, readability
- **Color** — Color theory, palettes, contrast, systems
- **Layout** — Grid systems, spacing, responsive, composition
- **Iconography** — Icon design, icon systems, visual metaphors

### Interaction Design
- **Patterns** — Common UI patterns (navigation, forms, modals, cards...)
- **Micro-interactions** — Animation, transitions, feedback, delight
- **Navigation** — IA, wayfinding, menu patterns, breadcrumbs

### UX Process
- **Research** — User interviews, surveys, usability testing, analytics
- **Strategy** — Personas, journey maps, jobs-to-be-done, value proposition
- **Wireframing** — Low-fi, mid-fi, sketching, prototyping methods
- **Testing** — Usability testing, A/B testing, heuristic evaluation

### Design Systems
- **Tokens** — Design tokens, variables, theming
- **Components** — Component architecture, atomic design, variants
- **Documentation** — Writing guidelines, pattern libraries, governance

### Tools & Workflow
- **Figma** — Tips, plugins, workflows, auto-layout, variables
- **Prototyping** — Figma prototyping, Framer, ProtoPie
- **Handoff** — Dev handoff, specs, inspect tools, code generation

### Case Studies
- **Redesigns** — Notable redesigns, before/after analysis
- **Breakdowns** — UI teardowns of great products
- **Personal** — Lessons from own projects

## Page Structure

Every wiki page MUST follow this template:

```markdown
# {Title}

> One-line summary of this topic.

## Overview
2-3 paragraphs explaining the concept.

## Key Points
- Bullet points of essential knowledge

## Examples
Real-world examples, screenshots references, or code snippets.

## Related
- [[linked-page-1]]
- [[linked-page-2]]

## Sources
- [Source title](url) — brief note
```

## Rules

1. **Links**: Use `[[wiki-link]]` format to connect related pages
2. **Ingest**: When adding a new source, update ALL related existing pages
3. **No duplication**: If info exists on another page, link to it — don't repeat
4. **Practical focus**: Always include actionable takeaways, not just theory
5. **Examples**: Prefer real product examples (Airbnb, Stripe, Linear, Notion...)
6. **Log everything**: Every ingest/update gets a line in `log.md`
7. **Vietnamese + English**: Giải thích bằng tiếng Việt, giữ thuật ngữ tiếng Anh

## Lint Checks

Run periodically to keep wiki healthy:
- [ ] Orphan pages (no incoming links)
- [ ] Dead links (links to non-existent pages)
- [ ] Stale content (>6 months without update)
- [ ] Contradictions between pages
- [ ] Missing categories (gaps in coverage)
- [ ] Pages too long (>500 lines → split)
