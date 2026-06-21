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

## Adding content

All message and glossary data lives in `assets/js/data.js`, in the `DATA` object. Add an entry there and it shows up automatically — no other files need to change.

```javascript
{
    code: 'CAMT.055',
    family: 'CAMT',
    title: 'CAMT.055',
    subtitle: 'Your Title Here',
    purpose: 'What this message does...',
    direction: 'Bank → Customer',
    category: 'Cash Management',
    useCases: ['Use Case 1', 'Use Case 2'],
    fields: ['Field1 (Description)', 'Field2'],
    example: '<Document>...</Document>'
}
```

Theme colors live in `assets/css/style.css` under `:root`.
