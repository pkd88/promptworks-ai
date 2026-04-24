**

# 

Version: 1.0 | Created: 2026-04-08 | Owner: Phil Dawson Purpose: Universal Markdown formatting standard for all RAG-ready documents produced by Prompt Works. Applies to: All Gems and workflows that create, convert, or stitch Markdown files — currently PW.3 (Clean-Room Data Technician), the Stitch Gem, and the Researcher Gem. Notebook placement: Shared PW context notebook. Attach to all Markdown-producing Gems.

  

---

## 1.0 The Lawbook

These are hard rules. Every Gem that produces Markdown must follow all of them every time. No exceptions.

### 1.1 Document Title

Every document must start with exactly one H1 title line. Use # once and never again in that document. Directly under the H1 title, write 2 to 3 short sentences that explain what the document is about, who it is for, and what problem it helps solve. These sentences are not optional.

### 1.2 Main Sections

Use ## for all main sections. Directly under every ## heading, write 1 to 2 sentences that clearly state what that section covers. These sentences must read like a short answer to the question "What is this section about?" Do not skip them. They are required for RAG retrieval accuracy.

  

Example of correct formatting:

  

## Monthly Tracking System

  

This section explains a simple way to track monthly income and compare it to the SSDI work limit. Use this section to find the rules for recording each payment.

### 1.3 Subsections

Use ### only when a true subsection is needed inside a ## section. If you use ###, also write 1 to 2 clear sentences directly under that heading. Do not go deeper than ### unless there is a strong specific reason.

### 1.4 No Table of Contents

Do not add a Table of Contents to any document. RAG systems use headings directly as retrieval anchors. A TOC adds noise without retrieval value and may create duplicate text in chunks.

### 1.5 Section Size

Keep each ## section between 300 and 500 tokens of content. If a section runs longer, split it with an additional ### subheading rather than letting it run as one long block.

### 1.6 Paragraphs

Keep paragraphs short and focused on a single idea. Put the most important fact or answer at the start of the paragraph, not the end. Use plain language.

### 1.7 Lists

Use numbered lists for steps that must happen in a specific order. Use bullet lists for unordered facts, options, or examples. Keep each list item short and clear. Do not nest lists more than two levels deep.

### 1.8 Code Blocks

Use fenced code blocks — triple backticks — for any multi-line code, commands, or full examples. Place the code block directly under the text that explains it. Do not split a code block across sections. Do not leave a code block without explanatory text nearby. Use inline code — single backticks — for function names, field names, and commands inside sentences.

### 1.9 Tables

Use Markdown tables when the data has clear columns and rows. Place every table inside a section that has a heading describing what the table shows. Do not mix unrelated topics in one table. If a table is very wide, split it or add explanatory text to keep chunks readable.

### 1.10 Horizontal Rules and Blockquotes

Use horizontal rules — --- — only to mark a strong break between major parts of a document. Prefer ## headings for structure instead. Use blockquotes — > — for warnings, important tips, or quoted material only. Do not use blockquotes for normal content.

### 1.11 Deprecated and Old Text

If old rules or outdated text must be kept in the document, move them into a clearly labeled section such as ## History and Changes or ## Old Versions. When something is no longer valid, use strikethrough ~~like this~~ AND add a plain word label such as "Deprecated" or "No longer valid." Do not leave outdated rules mixed into active sections without a clear label.

### 1.12 Citation Stripping

Delete all inline bracketed citations from source text — for example [1], [2], [cite: 3]. This is an authorized sanitization action. The meaning of the content must be preserved. Only the citation markers are removed.

### 1.13 URL Relocation

Remove all URLs from body text. Keep anchor text in place. Move all URLs to a ## References section at the bottom of the document as a numbered list. Never leave a raw URL inline in the body.

### 1.14 No YAML Front Matter

Do not add YAML front matter blocks to documents. Prompt Works uses the Bottom-Load Protocol for metadata, placed at the end of the document. YAML at the top contaminates the first RAG chunk.

### 1.15 Consistency

Use # once for the main title. Use ## for all main sections. Use ### for subsections when needed. Keep this structure the same across every document produced by this system.

  

---

## 2.0 Markdown Tag Reference for RAG

This section lists every major Markdown element and explains the correct way to use each one when building documents for RAG systems. The goal is not just correct syntax — it is clear structure that chunkers and retrievers can exploit.

### 2.1 Headings

# is used once for the document title only. ## marks all main sections. ### marks subsections. Avoid #### and deeper unless absolutely necessary.

  

Headings are the most important structural element for RAG. Most Markdown-aware chunkers split documents at heading boundaries. Each heading should describe a single concept, question, or task so that chunks aligned to those headings map cleanly to user queries.

  

Never use bold text as a fake heading. If it needs to be a section, use a real heading tag.

### 2.2 Paragraphs

Paragraphs are the body text inside each section. Keep related sentences together. Avoid mixing unrelated information in one paragraph. Put the most important point first. Short paragraphs retrieve better than long dense blocks.

### 2.3 Bold and Italic

Bold — **text** — and italic — *text* — are not recognized as structure by chunkers. They are ignored for splitting purposes. Use bold to highlight key terms or important parameter names. Use italic sparingly for definitions or titles. Do not rely on bold or italic as the only signal for important content — headings and lists carry that weight.

### 2.4 Bullet Lists

Use -  for unordered bullet lists. Use for sets of related facts, features, options, or examples where order does not matter. Keep items short. Avoid nesting more than two levels. A retriever that pulls a list chunk should get a complete, useful set — not a fragment.

### 2.5 Numbered Lists

Use 1. for ordered numbered lists. Use for steps, procedures, and sequences where order matters. Numbered lists inside a focused section retrieve cleanly as step-by-step instructions.

### 2.6 Code Blocks

Fenced code blocks use triple backticks at the start and end. Chunkers treat code blocks as atomic — they do not split inside them. Place each code block directly after the text that introduces it. One concept per code block. Label the language where possible — for example ```python or ```bash.

### 2.7 Inline Code

Single backticks mark identifiers, commands, field names, and file paths inside sentences — like this. Use freely wherever literal strings need to be distinguished from prose. Inline code is treated as plain text by chunkers — it does not affect splitting.

### 2.8 Tables

Markdown tables use the pipe character | to define columns and rows. Tables preserve tabular data unambiguously and are very valuable for RAG. Keep each table inside a single section under a heading that describes what the table shows. Do not let a table span across sections. Very wide tables may need to be split or accompanied by explanatory text.

### 2.9 Blockquotes

Use > to mark notes, warnings, cautionary tips, or quoted material. Keep blockquotes short and focused on one idea. Do not use blockquotes for layout or normal content. Complex nested blockquotes confuse chunkers.

### 2.10 Horizontal Rules

--- on its own line creates a horizontal rule. Use to mark a hard break between major parts of a document when a heading would be redundant. Use sparingly — overuse creates too many small disconnected chunks. Headings are always preferred over horizontal rules for structure.

### 2.11 Links

Format links as [descriptive text](url). Keep link text descriptive — for example "API rate limit policy" not "click here." Descriptive link text creates better retrieval context. Per the URL Relocation rule (1.13), all URLs must be moved to ## References — links in body text keep their anchor text in place and the URL is moved.

### 2.12 Images

Format as ![alt text](url). Most RAG systems index text only, not images. Alt text and nearby explanatory prose are what get indexed. Write descriptive alt text. Ensure the surrounding paragraph explains what the image shows. For multimodal RAG, the image syntax acts as a pointer — surrounding text still carries retrieval weight.

### 2.13 Strikethrough

Use ~~text~~ to mark deprecated or outdated content. Always pair strikethrough with a plain word label — "Deprecated," "Old rule," or "No longer valid." Never leave strikethrough text without explanation.

### 2.14 Footnotes

Some Markdown flavors support [^1] footnotes. Basic chunkers treat footnotes as plain text. For Prompt Works RAG documents, do not use footnotes. Integrate all important information into the main body text where it will chunk correctly.

### 2.15 Raw HTML

Avoid raw HTML in any document intended for RAG. HTML tags confuse parsers and produce inconsistent chunking. Stick to standard Markdown constructs. If a source document contains HTML, convert it to Markdown equivalents during sanitization.

  

---

## 3.0 Output Example

This section shows a complete, correctly formatted RAG-ready Markdown document. Use this as the reference for what correct output looks like. The topic is neutral and reusable.

  

---

  

# Widget API Guide

  

This guide explains how to authenticate, send requests, and handle errors when using the Widget API. It is written for developers who are integrating the API into their applications for the first time.

  

## Authentication

  

This section explains how to prove your identity to the Widget API before sending any requests. Every request must include a valid API key or it will be rejected.

  

### Getting an API Key

  

Follow these steps to create your first API key.

  

1. Sign in to your account at the Widget developer portal.

  

2. Go to the API Keys page in your account settings.

  

3. Click Create Key and copy the generated value immediately.

  

4. Store the key in a secure location. Do not share it or commit it to version control.

  

### Sending Authenticated Requests

  

Include your API key in the `X-Widget-Api-Key` header for every request you send. The header is required on all endpoints without exception.

  

```http

  

GET /v1/widgets HTTP/1.1

  

Host: api.widget.example

  

X-Widget-Api-Key: YOUR_API_KEY

  

If the key is missing or invalid, the API returns a 401 Unauthorized status code and stops processing the request.

## Creating Widgets

This section covers how to create a new widget using the API. Creating a widget requires a POST request with a JSON body.

### Request Format

Send a POST request to the /v1/widgets endpoint with the required fields in the request body.

  

POST /v1/widgets HTTP/1.1

  

Host: api.widget.example

  

Content-Type: application/json

  

X-Widget-Api-Key: YOUR_API_KEY

  

{

  

  "name": "Sample widget",

  

  "size": "medium"

  

}

  

The name field is required. The size field is optional. If you omit size, the API defaults to medium.

### Response Fields

A successful create request returns a JSON object. The table below describes each field in the response.

  

|Field|Type|Description|
|---|---|---|
|id|string|Unique identifier for the widget|
|name|string|The name you provided in the request|
|size|string|The size of the widget: small, medium, or large|
|created_at|string|ISO timestamp of when the widget was created|

## Error Handling

This section lists the error codes the Widget API returns and explains what each one means. Use this section to diagnose failed requests.

  

|Status|Meaning|Common Cause|
|---|---|---|
|400|Bad Request|Missing or invalid fields in the request body|
|401|Unauthorized|Missing or invalid API key|
|404|Not Found|The requested resource does not exist|
|500|Internal Error|Unexpected server-side problem|

  

For every error response, the body includes a message field with a plain-language description of the problem.

## References

1. Widget API developer portal — [https://developers.widget.example](https://developers.widget.example)
    
2. API rate limit policy — [https://developers.widget.example/rate-limits](https://developers.widget.example/rate-limits)
    

  

---

### END OF INSTRUCTIONS

- Functional Intent: Authenticate and use Widget API
    
- Authority Level: Level 3 (Standard)
    
- Linked Entities: Widget developer portal, rate limit policy
    

  

---

  

## 4.0 How Gems Use This Document

  

This section tells each Gem exactly what to do with this reference file.

  

All Gems that produce Markdown output must follow Part 1 (The Lawbook) without exception. The Lawbook rules override any conflicting instructions from a source document.

  

All Gems may reference Part 2 (Tag Reference) when making formatting decisions about specific Markdown elements.

  

All Gems must produce output that matches the structure shown in Part 3 (Output Example) — one H1 title with summary sentences underneath, `##` sections each with 1 to 2 opening sentences, correct use of lists and tables, no TOC, no YAML front matter, URLs relocated to References.

  

When a Gem's own instructions conflict with this document, this document wins on formatting decisions. The Gem's own instructions win on processing rules such as citation suppression, chunking protocol, and validation steps.

  

---

  

### END OF INSTRUCTIONS

  

- Functional Intent: Universal Markdown RAG formatting standard for all Prompt Works Gems

  

- Authority Level: Level 1 (Master) — applies across all Markdown-producing Gems

  

- Linked Entities: Gem 3 (Clean-Room Data Technician), Stitch Gem, Researcher Gem, shared PW context notebook

  
**