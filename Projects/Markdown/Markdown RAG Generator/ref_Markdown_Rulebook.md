# 📖 The Markdown Lawbook
> A complete guide to writing clean, correct Markdown — every rule, every element.

---

## Table of Contents
- [Headings](#headings)
- [Paragraphs](#paragraphs)
- [Line Breaks](#line-breaks)
- [Emphasis — Bold & Italic](#emphasis)
- [Blockquotes](#blockquotes)
- [Lists](#lists)
- [Code](#code)
- [Horizontal Rules](#horizontal-rules)
- [Links](#links)
- [Images](#images)
- [Tables](#tables)
- [Task Lists](#task-lists)
- [Footnotes](#footnotes)
- [Escaping Characters](#escaping-characters)
- [HTML in Markdown](#html-in-markdown)
- [Front Matter / Metadata](#front-matter)
- [The Cardinal Rules](#the-cardinal-rules)

---

## Headings

Use `#` symbols to create headings. More `#` = smaller heading.

```markdown
# H1 — Document Title (USE ONLY ONCE)
## H2 — Major Section
### H3 — Subsection
#### H4 — Sub-subsection
##### H5 — Rarely needed
###### H6 — Almost never used
```

**Laws:**
- ✅ Only **one H1** per document — it is the page title [web:36][web:42]
- ✅ Always put a **space** after the `#` symbol [web:31]
- ✅ Never skip levels — don't jump from H2 to H4 [web:43]
- ✅ Do NOT use headings just to make text bigger
- ✅ Leave a blank line before and after every heading

---

## Paragraphs

A paragraph is just plain text with a blank line between blocks.

```markdown
This is paragraph one.

This is paragraph two.
```

**Laws:**
- ✅ Separate paragraphs with **one blank line**
- ❌ Do NOT indent paragraphs with spaces or tabs

---

## Line Breaks

To force a line break inside a paragraph, end the line with **two spaces** or use `<br>`.

```markdown
Line one  
Line two

Line one<br>
Line two
```

**Laws:**
- ✅ Two trailing spaces creates a `<br>` line break [web:30]
- ✅ `<br>` is the cleaner, more readable option
- ❌ Do NOT rely on a single Enter key — it won't create a break

---

## Emphasis

```markdown
*italic* or _italic_

**bold** or __bold__

***bold and italic*** or ___bold and italic___

~~strikethrough~~
```

**Laws:**
- ✅ Use `*` for italic, `**` for bold — be **consistent** throughout the doc [web:32]
- ✅ Don't mix `*` and `_` styles in the same document
- ❌ Avoid `__double underscore__` bold — some parsers handle it differently
- ✅ Strikethrough uses `~~two tildes~~` on each side

---

## Blockquotes

Use `>` to indent and highlight a quote or note.

```markdown
> This is a blockquote.

> This is a multi-line blockquote.
> It spans two lines.

> Nested blockquote level one
>> Nested blockquote level two
```

**Laws:**
- ✅ Add a blank line before and after a blockquote
- ✅ Nested quotes use `>>` (double arrow)
- ✅ Great for tips, warnings, pulled quotes, or citations

---

## Lists

### Unordered Lists

```markdown
- Item one
- Item two
  - Sub-item (indent 2 spaces)
  - Sub-item
- Item three
```

### Ordered Lists

```markdown
1. First step
2. Second step
3. Third step
   1. Sub-step
   2. Sub-step
```

**Laws:**
- ✅ Use `-` for unordered lists — pick one style and stick to it [web:35]
- ✅ Use `1.` format for ordered lists
- ✅ Indent sub-items with **2 spaces**
- ❌ Don't mix `-`, `*`, and `+` in the same list
- ✅ Leave a blank line before and after a list block
- ✅ Use **ordered lists** for steps; use **unordered** for collections

---

## Code

### Inline Code

```markdown
Use `backticks` around inline code.
```

### Code Blocks (Fenced)

````markdown
```python
def hello():
    print("Hello, world!")
```
````

**Laws:**
- ✅ Always label fenced code blocks with the language (`python`, `bash`, `json`, etc.) [web:39]
- ✅ Use triple backticks ` ``` ` — not tildes, not indentation, unless necessary
- ❌ Never nest triple backticks inside triple backticks — use 4 backticks for the outer block
- ✅ Inline code uses single backticks on each side

---

## Horizontal Rules

Creates a dividing line between sections.

```markdown
***

***

___
```

**Laws:**
- ✅ Use `---` (three dashes) — it is the most readable[35]
- ✅ Always put a **blank line before and after** a horizontal rule
- ❌ Do not use `---` directly after text — it will be read as an H2 heading instead

---

## Links

```markdown
[Link Text](https://example.com)

[Link Text](https://example.com "Optional Tooltip")

[Reference Link][ref-id]

[ref-id]: https://example.com
```

**Laws:**
- ✅ Link text should describe the destination — not just "click here"
- ✅ Use reference-style links to keep text clean in long documents
- ✅ Always use full URLs with `https://`
- ❌ Don't leave bare URLs without angle brackets: use `<https://example.com>` if raw

---

## Images

```markdown


![Alt Text](image-url.jpg "Optional Tooltip")
```

**Laws:**
- ✅ **Always write descriptive alt text** — it's required for accessibility[33]
- ✅ Alt text describes what the image shows
- ✅ Images are like links — but with a `!` in front
- ❌ Do NOT leave alt text empty unless image is purely decorative

---

## Tables

```markdown
| Column A | Column B | Column C |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
```

### Alignment

```markdown
| Left     | Center   | Right    |
|:---------|:--------:|---------:|
| text     | text     | text     |
```

**Laws:**
- ✅ Always include the header row and the separator row (`|---|`)
- ✅ Use `:` in the separator row to set alignment
- ✅ Leave blank lines before and after a table
- ❌ Tables do NOT support multi-line cells in standard Markdown

---

## Task Lists

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task
```

**Laws:**
- ✅ Requires a space inside the brackets for unchecked: `[ ]`
- ✅ Requires an `x` for checked: `[x]`
- ✅ Supported in GitHub, Obsidian, and most modern renderers
- ❌ Not supported in all basic Markdown parsers

---

## Footnotes

```markdown
This is a sentence with a footnote.[3]

[3]This is the footnote text.
```

**Laws:**
- ✅ Footnote references go inline; definitions go at the bottom of the doc
- ✅ Use descriptive labels instead of numbers when possible: `[^source]`
- ❌ Not supported in all Markdown parsers — check your platform first

---

## Escaping Characters

Use a backslash `\` to show a special character as plain text.

```markdown
\# This is not a heading
\*This is not bold\*
\- This is not a list item
```

**Escapable characters:** `\ ` ` * _ { } [ ] ( ) # + - . ! |`

**Laws:**
- ✅ Use `\` before any character that has special Markdown meaning
- ✅ Essential when writing about Markdown itself

---

## HTML in Markdown

Most Markdown parsers allow raw HTML inline.

```markdown
<br>
<strong>Bold via HTML</strong>
<mark>Highlighted text</mark>
<details>
  <summary>Click to expand</summary>
  Hidden content here.
</details>
```

**Laws:**
- ✅ HTML is valid inside Markdown files
- ✅ Use `<br>` for clean line breaks
- ✅ `<details>` + `<summary>` creates collapsible sections — very useful
- ❌ Avoid HTML unless Markdown alone can't do the job

---

## Front Matter / Metadata

YAML front matter goes at the very top of the document.

```markdown
***
title: My Document Title
author: Phil Dawson
date: 2026-04-16
tags: [markdown, reference, lawbook]
description: A complete markdown reference guide.
***
```

**Laws:**
- ✅ Must be the **very first thing** in the file — nothing above it
- ✅ Surrounded by `---` on both ends
- ✅ Supported in Jekyll, Obsidian, Hugo, and many AI tools
- ❌ Not rendered visually in all editors — it stays as metadata

---

## The Cardinal Rules

These are the non-negotiable laws of clean Markdown:

| Rule | Law |
|------|-----|
| H1 Count | Only **one H1** per document |
| Heading Order | Never skip a heading level (H1 → H2 → H3) |
| Blank Lines | Add blank lines before/after headings, lists, tables, rules, blockquotes |
| Consistency | Pick one style per element and use it throughout |
| Alt Text | Always add alt text to images |
| Code Labels | Always label fenced code blocks with the language |
| List Style | One list marker style per document (`-` or `*`, not both) |
| Link Text | Never use "click here" — describe the destination |
| No Skip | Don't use headings for visual size — use them for structure |
| Front Matter | YAML front matter must be first, nothing above it |

---

*Last updated: 2026-04-16 | Phil's PromptWorks Reference Docs*