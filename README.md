# ISO 20022 Academy

A website for learning and exploring ISO 20022 payment messaging — message types, terminology, and structure. Built with plain HTML, CSS, and JavaScript, no frameworks or build step.

## Running it

Open `index.html` in a browser. That's it — no install, no server required.

## Pages

- **History** — how ISO 20022 came about and where it's headed
- **Explorer** — browse message families (CAMT, PACS, PAIN, and others), click any message for its purpose, direction, use cases, and an XML example (in progress)
- **Transformer** — message format conversion (in progress)
- **Glossary** — searchable definitions of payment terms (IBAN, BIC, settlement, etc.)
- **Learning Path** — structured course modules (in progress)

## File structure

```
index.html              page shell, header/nav, content + detail-panel containers
assets/css/style.css    all styling, theme variables
assets/js/data.js       message catalog and glossary content
assets/js/app.js        page routing and page templates
assets/js/ui.js         detail panel, explorer/glossary rendering, theme toggle
assets/js/preloader.js  one-time intro animation
```

This repo is still under development, please feel free to reach out to me for the updates on this if you like it !
