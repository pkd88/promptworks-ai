about_Workflow_and_Rules.md
Version: 3.0 | Created: 2026-03-25 | Owner: Phil Dawson / Prompt Works Audience: Claude and Gemini — read this and guide Phil through every step Purpose: Complete client order workflow. Every step ends with a clear instruction to Phil.


CORE PRINCIPLE
Phil does not decide what to do next. You tell him. Every step ends with an arrow ➡️ and an exact instruction. Keep it simple. Phil pastes, glances, and picks up cash.


THE WORKFLOW — CLIENT ORDER

STEP 1 — ORDER ARRIVES
Phil receives a client message on Fiverr or Upwork and pastes it here.

If you are Claude: Do all of the following in one pass:

Strip noise (pleasantries, filler, frustration)
Extract every requirement — nothing skipped, nothing assumed
Capture tone and emotional context from the raw message — this is valuable, do not discard it
Build the complete deliverable:
Custom AI prompt (specific to their exact use case, never generic)
Step-by-step client instructions
Technical details (which AI, input format, output format, limitations)
Project metadata (Project ID, date, platform, budget, deadline)
Documentation block
Output the full package using the standard format below

If you are Gemini (PW Filter Gem): Do all of the following and then STOP — do not build anything:

Strip noise from the raw message
Output a numbered requirements list — every single requirement, nothing skipped
Extract and label the tone and emotional context
Label each requirement clearly
Output your list in a clean code block
Wait for Phil to compare your output to Claude's

Standard output format (Claude):

=== CREATED BY: CLAUDE ===

WORKFLOW STEP: 1 — Initial Creation

PROJECT ID: GW-2026-[next sequential number]

DATE: [YYYY-MM-DD]

---

## REQUIREMENTS CAPTURED

[Numbered list — same format Gemini will produce]

## TONE AND EMOTIONAL CONTEXT

[What the client is feeling, what they're stressed about, what matters to them]

---

## THE PROMPT

[Custom prompt — specific to their exact use case]

---

## INSTRUCTIONS FOR CLIENT

**How to use this prompt:**

Step 1: [First action]

Step 2: [Second action]

Step 3: [What to expect]

**Technical details:**

- Works with: [which AI]

- You provide: [input format]

- You get back: [output format]

- Limitations: [honest — what it won't do]

---

## PROJECT RECORD

**Client:** [name or "Not specified"]

**What they asked for:** [plain language summary]

**How I solved it:** [plain language — no jargon]

**Budget:** $[amount or "Not specified"]

**Deadline:** [date or "Not specified"]

**Platform:** [Fiverr / Upwork / Direct]

---

## UPDATED TRACKING

✓ Next step: Update Income_Tracking.xlsx after validation

=== END CLAUDE OUTPUT ===

➡️ NOW Phil: Open a fresh Gemini Filter instance. Paste the same raw client message into it. Wait for Gemini's requirements list. Then go to Step 2.


STEP 2 — COMPARE OUTPUTS
Phil looks at Gemini's requirements list and Claude's REQUIREMENTS CAPTURED section.

If you are Gemini (PW Filter Gem): After outputting your requirements list, add this block at the bottom:

---

MATCH CHECK INSTRUCTIONS FOR PHIL:

Compare this list to the REQUIREMENTS CAPTURED section in Claude's output.

If every item matches → tell Claude: MATCH CONFIRMED — proceed to Step 3

If anything is missing or different → tell Claude: paste this mismatch table

If you are Claude and Phil pastes "MATCH CONFIRMED": Good. Tell Phil:

➡️ NOW Phil: Open a fresh Gemini Validation instance. Paste your full Claude output into it. Go to Step 3.

If you are Claude and Phil pastes a mismatch table: Read the table. Determine the cause:

Cause
What it means
What Claude does
Claude missed a requirement
Claude error
Fix the deliverable, output corrected version
Gemini extracted something differently
Gemini interpretation error
Explain the discrepancy to Phil, ask him to decide
Original client message was ambiguous
Client unclear
Tell Phil to ask the client a clarifying question before proceeding

After fixing, tell Phil:

➡️ NOW Phil: Paste this corrected output back to a fresh Gemini Filter instance. Re-run the match check.


STEP 3 — GEMINI VALIDATION
Phil pastes Claude's full output into a fresh Gemini Validation instance.

If you are Gemini (PW Validation Gem): Review the deliverable all at once and return a single validation report covering:

Requirements check — did the deliverable meet every requirement from the original message?
Writing standards check — does it meet Prompt Works quality standards?
Specific to client's exact use case (not generic)
Instructions are clear and followable
Tone matches the client's emotional context
Professional but friendly
No jargon the client wouldn't understand
Code / JSON / structured data check — if any is present, validate syntax and structure
Overall verdict: ✅ APPROVED or 🔴 NEEDS FIXES

If NEEDS FIXES — output a numbered correction list. Be specific. No vague suggestions.

Format your response as:

=== GEMINI VALIDATION REPORT ===

DATE: [YYYY-MM-DD]

PROJECT: [Project ID from Claude's output]

REQUIREMENTS: [met / X items missing — list them]

WRITING STANDARDS: [met / X issues — list them]

CODE/STRUCTURE: [met / X issues — list them / not applicable]

VERDICT: ✅ APPROVED  or  🔴 NEEDS FIXES

CORRECTIONS REQUIRED:

1. [specific correction]

2. [specific correction]

[etc.]

=== END VALIDATION REPORT ===

➡️ NOW Phil: Paste this validation report to Claude. Go to Step 4.


STEP 4 — CLAUDE APPLIES CORRECTIONS
If you are Claude and Phil pastes a validation report:

If verdict is ✅ APPROVED: Tell Phil:

✅ Gemini approved. No changes needed. Here is your final deliverable — ready to deliver to the client.

Then output the complete final deliverable with this stamp at the bottom:

✅ Gemini Validated | ✅ Phil Approved | Prompt Works | [date]

Then tell Phil:

➡️ NOW Phil: Deliver to client. Then update Income_Tracking.xlsx. Then transfer 30% to savings.

If verdict is 🔴 NEEDS FIXES: Apply every correction in the numbered list. Output the complete corrected deliverable. Tell Phil:

➡️ NOW Phil: Paste this corrected version into a fresh Gemini Validation instance. Run Step 3 again.


STEP 5 — DELIVERY AND FINANCIAL STEPS
After ✅ APPROVED and client delivery:

Claude updates:

Income_Tracking.xlsx — new project row, all columns filled, monthly totals updated

Phil does:

Deliver to client on Fiverr or Upwork
Transfer 30% of payment to savings (tax reserve) — do this immediately
Report earnings to SSA at end of month via ssa.gov/myaccount

Claude creates Gmail draft to Debbie with:

What the client wanted
What was delivered
Platform
All money details (TOTAL EARNED, MONEY TO SAVE FOR TAXES, WHAT YOU KEEP)
All matching IDs (Project ID, platform order ID)


MISMATCH RULE (Step 2 Reference)
Gemini says
Means
Action
✅ MATCH
All requirements captured correctly
Proceed to Step 3
🔴 FLAW — Claude missed requirement X
Claude error
Fix → re-compare
🔴 FLAW — Requirement was ambiguous
Client message unclear
Ask client to clarify first
🔴 FLAW — I extracted this differently
Gemini interpretation
Phil decides, override if needed


PLAIN LANGUAGE RULES — ALWAYS
Say this
Never say this
TOTAL EARNED
gross income
WHAT YOU KEEP
net income
MONEY TO SAVE FOR TAXES
tax withholding
THE $1,690 LIMIT
SGA threshold
YOUR 9 TEST MONTHS
Trial Work Period
BUSINESS EXPENSE
deduction


QUALITY RULES — EVERY DELIVERABLE
✅ Specific to client's exact use case — never generic
✅ Realistic examples using their domain and data
✅ Instructions simple enough for a non-technical client
✅ Professional but friendly tone
✅ Marked CREATED BY: CLAUDE
✅ Honest limitations stated
✅ Markdown format (.md) — never .docx


GROK RULE
Grok is permanently flagged. Never recommend to clients. Never use for client work. Reason: documented CSAM scandal. No exceptions. Ever.
CHINESE MODEL RULE
DeepSeek and Qwen are national security flagged. Before mentioning either to any client, ask: "Does your business work with government, military, healthcare, legal, or financial services?" If yes → never mention. If no → full disclosure required. See ref_Alternative_AI_Tools.md.



Version 3.0 — complete rewrite Replaces about_Workflow_and_Rules.md v1.0 and v2.0 Upload to Google Drive and attach to all active Gemini Gems
