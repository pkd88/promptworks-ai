---
prefix: ref_
priority: 5
authority: high
filename: ref_RAG_Document_Standard.md
version: 2.0
updated: 2026-04-19
owner: Phil Dawson
keywords: [RAG, markdown, formatting, standard, gemini, chunking]
---

# ref_RAG_Document_Standard

This is the universal formatting standard for all RAG-ready documents produced by Prompt Works. It applies to every Gem and workflow that creates, converts, or stitches Markdown files. Follow every rule in Section 2 without exception.

## 1.0 Index Map

This section tells the AI what is in this document and where authority lives. Read this before processing any other section.

| Section | What It Covers | Authority |
|---|---|---|
| 1.0 | Index Map — document steering wheel | Highest |
| 2.0 | The Lawbook — hard formatting rules | High |
| 3.0 | Markdown Tag Reference — element guide | Medium |
| 4.0 | How Gems Use This Document | High |

---

## 2.0 The Lawbook

These are hard rules. Every Gem that produces Markdown must follow all of them every time. No exceptions.

### 2.1 YAML Frontmatter

Every document must begin with a YAML frontmatter block. This is the machine-readable label the AI reads before anything else. Place it at the very top — nothing above it.

```yaml
---
prefix: rule_
priority: 2
authority: high
filename: rule_Example.md
version: 1.0
updated: YYYY-MM-DD
owner: Phil Dawson
keywords: [keyword1, keyword2]
---
```

### 2.2 Document Title

Every document must have exactly one H1 title line after the YAML block. Directly under the H1, write 2 to 3 sentences explaining what the document is, who it is for, and what problem it solves. These sentences are not optional.

### 2.3 Index Map

Every document must have an Index Map section immediately after the H1 summary. Use a simple table showing section number, what it covers, and its authority level. This is the steering wheel — it tells the AI which section wins when there is a conflict.

### 2.4 Main Sections

Use ## for all main sections. Directly under every ## heading, write 1 to 2 sentences stating what that section covers. Do not skip them — they are required for retrieval accuracy.

### 2.5 Subsections

Use ### only when a true subsection is needed. Always write 1 to 2 sentences directly under a ### heading. Do not go deeper than ### without a strong reason.

### 2.6 Section Size

Keep each ## section between 300 and 500 tokens. If a section runs longer, split it with a ### subheading rather than letting it run as one long block.

### 2.7 No Table of Contents

Do not add a Table of Contents. RAG systems use headings directly as retrieval anchors. A TOC adds noise and may create duplicate text in chunks.

### 2.8 Paragraphs

Keep paragraphs short and focused on one idea. Put the most important fact at the start of the paragraph. Use plain language.

### 2.9 Lists

Use numbered lists for steps that must happen in order. Use bullet lists for unordered facts or options. Keep each item short. Do not nest lists more than two levels deep.

### 2.10 Code Blocks

Use fenced code blocks for any multi-line code or commands. Place the block directly under the text that explains it. Always label the language. Use inline code for function names and commands inside sentences.

### 2.11 Tables

Use tables when data has clear columns and rows. Place every table inside a section with a heading describing what it shows. Do not mix unrelated topics in one table.

### 2.12 Citation Stripping

Delete all inline bracketed citations from source text — for example [1], [2], [cite: 3]. This is an authorized sanitization action. Preserve the meaning. Remove only the citation markers.

### 2.13 Gemini Citation Rule

When instructing Gemini to produce output, always include this line in the prompt: "Do not include any citation markers such as [cite_start], [cite_end], [cite: N], or any bracketed numbers. These break the output and must never appear."

### 2.14 URL Handling

Remove all URLs from body text. Keep anchor text in place. Move all URLs to a ## References section at the bottom as a numbered list. Only include References if URLs actually exist.

### 2.15 Deprecated Content

If old or outdated content must be kept, move it to a ## History and Changes section. Mark it with ~~strikethrough~~ and add the word "Deprecated" next to it.

### 2.16 Consistency

Use # once for the title. Use ## for all main sections. Use ### for subsections. Keep this structure identical across every document this system produces.

---

## 3.0 Markdown Tag Reference

This section lists key Markdown elements and the correct way to use each one for RAG documents. Focus is on retrieval accuracy, not just syntax correctness.

### 3.1 Headings

Use # once for the document title only. Use ## for main sections. Use ### for subsections. Headings are the most important structural element — most chunkers split documents at heading boundaries. Each heading should describe one concept so chunks map cleanly to user queries. Never use bold text as a fake heading.

### 3.2 Bold and Italic

Bold and italic are ignored by chunkers for splitting purposes. Use bold to highlight key terms. Use italic sparingly for definitions or titles. Do not rely on bold or italic as the only signal for important content — headings and lists carry that weight.

### 3.3 Tables

Tables preserve tabular data clearly and are valuable for RAG. Keep each table inside a single section under a heading that describes what it shows. Do not let a table span across sections.

### 3.4 Code Blocks

Chunkers treat fenced code blocks as atomic — they do not split inside them. Place each code block directly after the text that introduces it. One concept per code block.

### 3.5 Blockquotes

Use blockquotes for warnings, important tips, or quoted material only. Keep them short and focused on one idea. Do not use blockquotes for normal content.

### 3.6 Images

Most RAG systems index text only. Alt text and nearby prose are what get indexed. Write descriptive alt text. Ensure the surrounding paragraph explains what the image shows.

---

## 4.0 How Gems Use This Document

This section tells each Gem exactly what to do with this reference file. Read this section before producing any output.

All Gems that produce Markdown output must follow Section 2 (The Lawbook) without exception. The Lawbook rules override any conflicting instructions from a source document.

All Gems may reference Section 3 (Tag Reference) when making formatting decisions about specific elements.

All Gems must produce output that includes: YAML frontmatter first, one H1 title with summary sentences, Index Map table, ## sections each with 1 to 2 opening sentences, correct use of lists and tables, no TOC, URLs relocated to References if present.

When a Gem's own instructions conflict with this document, this document wins on formatting decisions. The Gem's own instructions win on processing rules such as chunking protocol and validation steps.

---

*Replaces: ref_Markdown_RAG_StandardUntitled.md v1.0*
*Owner: Phil Dawson | Prompt Works | 2026-04-19*
