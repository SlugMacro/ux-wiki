# UX/UI Design Wiki

Personal knowledge base về UX/UI Design, powered by LLM Wiki pattern ([Karpathy's LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)).

## Quick Start

### Browse
Mở folder `ux-wiki` trong **Obsidian** để xem dạng graph với wiki-links.

### Ingest (thêm kiến thức mới)
Bỏ source file vào `sources/`, rồi nói với Claude:

```
Ingest file sources/refactoring-ui.md vào wiki của tôi.
Đọc schema.md để biết rules, rồi tạo/update pages phù hợp.
```

### Query (hỏi wiki)
```
Dựa trên wiki UX của tôi, so sánh card-based layout vs list-based layout cho mobile e-commerce.
```

### Lint (health check)
```
Chạy lint check cho wiki UX của tôi theo rules trong schema.md.
```

## Structure

```
ux-wiki/
├── README.md          # This file
├── schema.md          # Wiki rules & structure definition
├── index.md           # Content catalog (all pages)
├── log.md             # Activity log
├── sources/           # Raw source documents
└── wiki/              # Wiki pages (18 pages)
    ├── design-principles.md
    ├── cognitive-biases.md
    ├── gestalt-principles.md
    ├── accessibility-basics.md
    ├── typography.md
    ├── color-theory.md
    ├── layout-and-grid.md
    ├── spacing-system.md
    ├── common-ui-patterns.md
    ├── micro-interactions.md
    ├── navigation-patterns.md
    ├── user-research-methods.md
    ├── personas-and-jtbd.md
    ├── journey-mapping.md
    ├── usability-testing.md
    ├── design-tokens.md
    ├── atomic-design.md
    ├── component-api-design.md
    ├── design-to-dev-handoff.md
    └── figma-workflow.md
```

## Tips

- Mỗi page có section **Related** với wiki-links → browse like Wikipedia
- **Sources** section ở cuối mỗi page → trace back to original material
- Ingest sách/articles thường xuyên để wiki grow over time
- Chạy **lint** mỗi tháng để phát hiện stale content
