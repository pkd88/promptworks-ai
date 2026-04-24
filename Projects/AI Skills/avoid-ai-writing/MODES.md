---
name: MODES
description: >
  Defines the two operating modes for the avoid-ai-writing skill.
  Detect-only vs detect+rewrite. When to use each. How to switch between them.
part-of: avoid-ai-writing
version: 1.0.0
---

# Modes — Detect vs Rewrite

This skill runs in one of two modes. Choose based on what the user needs.

---

## MODE 1 — Detect Only

**What it does:**
Reads the content and lists every AI pattern found. No changes to the text.
The writer sees what is flagged and decides what to fix themselves.

**When to use detect mode:**
- User wants to see the problems before deciding what to fix
- Some flagged patterns might be intentional — AI patterns are not always wrong
- Auditing content you should not alter (published work, someone else's writing)
- Quick scan without waiting for a full rewrite
- User is learning what their AI tells are

**Trigger phrases for detect mode:**
- "detect only"
- "flag only"
- "audit only"
- "just flag, don't rewrite"
- "scan this"
- "what AI patterns are in this"
- "show me the problems"
- "what would you flag"

**Output:**
See `OUTPUT_FORMAT.md` — Detect Mode section.

---

## MODE 2 — Rewrite (Default)

**What it does:**
Flags every AI pattern found AND rewrites the content to fix them.
Returns the cleaned version plus a summary of what changed.

**When to use rewrite mode:**
- Default when no mode is specified
- User wants a clean draft ready to use
- Content is headed toward publication or delivery
- User says "clean this up," "humanize this," "make this sound less like AI"

**Trigger phrases for rewrite mode:**
- "rewrite this"
- "clean this up"
- "humanize this"
- "remove AI-isms"
- "make this sound less like AI"
- "fix the AI patterns"
- Default — if no mode is specified, use rewrite mode

**Output:**
See `OUTPUT_FORMAT.md` — Rewrite Mode section.

---

## MODE 3 — Auto (Write Clean From the Start)

**What it does:**
Applies all hard ban rules and soft flag rules during initial writing,
before a draft even exists. The output should not need auditing.

**When to use auto mode:**
- User asks to write an article, email, post, report, or any document
- User says "write me a..." or "draft a..." or "create a..."
- Any initial writing task where a clean draft is the goal
- When ref_Chat-Behavior-No-AI-Voice.md is active in the system prompt

**This mode is always-on when:**
- The companion file `ref_Chat-Behavior-No-AI-Voice.md` is loaded
- The user has set up a Gem, Space, or system prompt with that file active

**How it works:**
Load `RULES_HARD.md` and `RULES_SOFT.md` silently before writing.
Apply the rules during drafting, not after.
Do not announce that you are doing this — just write clean.
If the content type is known, also load the relevant profile from `PROFILES.md`.

**Trigger phrases for auto mode:**
- "write me an article about..."
- "draft a blog post on..."
- "write an email to..."
- "create a report on..."
- Any writing task where you are generating content, not reviewing it

**Important:**
Auto mode does not replace detect or rewrite mode.
If the user asks to audit something after writing, switch to detect or rewrite mode.

---

## Mode Summary

| Mode | When | Triggered by | Output |
|---|---|---|---|
| Detect | Auditing only | "scan this," "flag only" | Issues list only |
| Rewrite | Auditing + fixing | "clean this up," default | Issues + clean draft + diff |
| Auto | Initial writing | "write me..." any draft request | Clean draft, no audit report |

---

## Switching Modes Mid-Conversation

If the user switches from writing to auditing, or auditing to rewriting,
switch modes immediately without asking for confirmation.

Examples:
- User got a rewrite → asks "can you just show me what you flagged without changing it" → switch to detect mode output
- User got a detect report → asks "ok fix all the P0 and P1 items" → switch to rewrite mode
- User asked for an article → then asks "audit that for AI tells" → switch to detect or rewrite mode

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: RULES_HARD.md*
