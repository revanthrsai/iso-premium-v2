# ISO 20022 Academy

A course, not a reference. Learn the language of modern payments — from how money
actually moves to reading and validating real ISO 20022 messages — through long-form
lessons that always start with a human problem, never a tag. Built with plain HTML,
CSS, and JavaScript: no frameworks, no build step.

## Running it

Open `index.html` in a browser. That's it — no install, no server required.

## Sections

- **The History** — five cinematic chapters on how the world's money messaging evolved:
  from paper and telegrams, through SWIFT MT, to the ISO 20022 migration. Routed at
  `#/history/<chapter-slug>`.
- **The Library** — 30 long-form lessons in five levels (100 Fundamentals → 500 Case
  Studies), each following the nine-beat Lesson Spine from `PHILOSOPHY.md`. Includes
  knowledge checks, a persisted "mark as learned" toggle, and beat-4 flow diagrams.
  Lessons live as Markdown in `content/`, routed at `#/library`.
- **The Playground** — five integrated tools that share one message hand-off: XML Viewer,
  Transformer (MT ⇄ MX), Validator, Comparator, and a Sample Message Library. Routed at
  `#/playground/<tool>`.
- **The Glossary** — 87 searchable, category-filtered payment terms with cross-links into
  the Library and Playground. Routed at `#/glossary`.

## File structure

```
index.html               page shell: header/nav, content container, script includes
DESIGN_TOKENS.css        single-source design tokens (dark + light themes)
TEMPLATE.html            standalone page-shell reference (header / content / footer)
content/*.md             the 30 Library lessons (frontmatter + Markdown + tokens)
assets/css/style.css     all styling, on top of the tokens
assets/js/app.js         routing (hash), page templates, History chapters
assets/js/toc.js         Library table of contents (levels, order, metadata)
assets/js/markdown.js    lesson engine: frontmatter, Markdown, {{embed}}/{{check}}/{{flow}} tokens
assets/js/flow-diagram.js beat-4 business-terms flow diagram component
assets/js/data.js        glossary terms + Progress store (localStorage)
assets/js/ui.js          glossary rendering, detail panel, theme toggle
assets/js/xml-viewer.js  Playground: XML tree viewer
assets/js/transformer.js Playground: MT ⇄ MX transformer
assets/js/validator.js   Playground: message validator
assets/js/comparator.js  Playground: message comparator
assets/js/samples.js     Playground: sample message library
assets/js/motion.js      motion design system (reduced-motion gated)
assets/js/preloader.js   one-time intro animation
```

## Documentation

- `PHILOSOPHY.md` — the product's teaching philosophy and the nine-beat Lesson Spine
- `NAVIGATION.md` — information architecture and the `#/…` route scheme
- `COMPONENTS.md` — component inventory and usage
- `ACADEMY_BLUEPRINT_PLAN.md` — the phased roadmap and session log
- `REFINEMENT.md` — Phase 7 quality & trust pass (sessions 7.1–7.7)

This repo is still under development — feel free to reach out for updates if you like it!
