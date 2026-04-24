---
name: OUTPUT_FORMAT
description: >
  Defines how the avoid-ai-writing skill presents its results.
  Covers detect mode output, rewrite mode output, and auto mode behavior.
  Consistent format makes audits easy to read and act on.
part-of: avoid-ai-writing
version: 1.0.0
---

# Output Format — How Results Look

This file defines exactly how to present audit results.
Follow these formats consistently so every audit is easy to scan and act on.

---

## Detect Mode Output

Return results in two sections only.

---

### Section 1: Issues Found

Label it exactly: **Issues Found**

List every AI pattern identified. Group by severity tier.
Quote the offending text exactly as it appears in the original.
State the rule number it violates.

Format each item as:

[Severity] Rule reference — "quoted offending text"
Brief note on why it is a problem if not obvious.

Example:

**P0**
- H2 (Chatbot filler) — "I hope this helps!"
- H9 (Cutoff disclaimer) — "As of my last update, the situation may have changed."

**P1**
- H3 (Contrastive reframing) — "It's not just about writing well. It's about thinking clearly."
- H1 (Em dash) — "The fix was simple — and it worked."
- S1 (Tier 1 word) — "leverage" used 3 times
- S4 (Stacked transitions) — "Additionally... Moreover... Furthermore" in same paragraph

**P2**
- S5 (Sentence uniformity) — All sentences between 16 and 22 words throughout
- S6 (Paragraph uniformity) — Every paragraph is 4 sentences

---

### Section 2: Assessment

Label it exactly: **Assessment**

For each flagged item, note one of three things:

- **Fix this** — clear problem, no context makes it acceptable
- **Worth a look** — likely a problem, but might be intentional
- **Your call** — the pattern is present but could be working in context

Keep it short. One line per item is enough.
If the text is clean, say so directly: "No significant AI patterns found."

Do not rewrite anything in detect mode.
Do not suggest rewrites unless the user asks.

---

## Rewrite Mode Output

Return results in four sections.

---

### Section 1: Issues Found

Same format as detect mode Section 1.
List every issue before rewriting anything.

---

### Section 2: Rewritten Version

Label it exactly: **Rewritten Version**

Return the full rewritten content.
- Preserve the original structure, intent, and all specific facts and details
- Only change what the rules require
- Do not improve the argument, add new ideas, or restructure without cause
- Do not over-edit — if a section is clean, leave it alone
- Natural disfluency and rough edges that are clearly human: leave them

If the piece needed a full rewrite rather than a patch, say so briefly
before the rewrite: "This needed a full structural rewrite, not a patch.
The core argument is preserved. Structure rebuilt from the main point."

---

### Section 3: What Changed

Label it exactly: **What Changed**

A brief summary of the meaningful edits made.
Not every word — just the categories and key changes.

Format:

- Removed [X] em dashes — replaced with commas and periods
- Cut chatbot opener: "I hope this helps!"
- Replaced 4 Tier 1 words: leverage → use, robust → solid, seamless → smooth, pivotal → key
- Broke up 3 uniform paragraphs — varied length
- Removed contrastive reframe in paragraph 2
- [If nothing needed changing]: "No changes made. Text was already clean."

Keep this section short. Bullets only. No explanation unless the change was unusual.

---

### Section 4: Second-Pass Audit

Label it exactly: **Second-Pass Audit**

Re-read the rewritten version from Section 2.
Look for anything that survived the first pass:
- Recycled transitions that slipped through
- Lingering inflation or hype phrasing
- Copula avoidance that was missed
- New patterns introduced by the rewrite itself (rewrites can introduce AI tells)
- Anything that still does not sound like a specific person wrote it

If issues remain: fix them, show the corrected text inline, note what changed.
If the rewrite is clean: say so directly. "Second pass clean. No further changes."

Do not invent problems. If it is clean, say it is clean.

---

## Auto Mode Output

In auto mode the skill runs silently during initial writing.
There is no audit report. There is no issues list.
The output is simply the written content — clean from the start.

The only exception: if the user asks "what rules did you apply" or
"what did you avoid," give a brief summary of the profiles and rules used.

Format for that summary:

Profile used: [profile name]
Hard rules applied: [list the H rules that were relevant]
Soft rules applied: [list any S rules that shaped choices]
Patterns avoided: [brief list of the main things steered around]

---

## Quick Scan Output (Short Version)

When the user asks for a fast scan of a short piece (under 200 words),
use this condensed format instead of the full four-section output.

**Quick Scan Results**

P0: [list any P0 issues, or "none"]
P1: [list the top P1 issues, or "none"]
P2: [brief note on P2 patterns, or "none"]

Clean? [yes / mostly / needs work]

Then ask: "Want a full rewrite, or just the P0 and P1 fixes?"

---

## Tone of Audit Output

The audit itself should not sound like AI.
Apply RULES_HARD.md to the audit output just as you would to any writing.

Specifically:
- No chatbot filler in the audit: "Great news — your text is mostly clean!"
- No hype about the rewrite: "Here is a dramatically improved version!"
- No fake enthusiasm about finding problems
- Direct, specific, calm
- If the text is bad, say it is bad
- If it is good, say it is good
- No padding to soften the verdict

The audit is a professional edit. Treat it like one.

---

## File Reference Quick Guide

When citing rule violations in output, use these short references:

| Reference | Meaning |
|---|---|
| H1 through H10 | Hard rules from RULES_HARD.md |
| S1 through S12 | Soft rules from RULES_SOFT.md |
| L1 through L10 | Leave-alone rules from RULES_LEAVE_ALONE.md |
| C1 through C5 | ChatGPT-specific tells from MODEL_TELLS.md |
| CL1 through CL5 | Claude-specific tells from MODEL_TELLS.md |
| G1 through G3 | Grok-specific tells from MODEL_TELLS.md |
| P1 through P3 | PPX-specific tells from MODEL_TELLS.md |
| GM1 through GM2 | Gemini-specific tells from MODEL_TELLS.md |

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: EXAMPLES.md — the final file*
