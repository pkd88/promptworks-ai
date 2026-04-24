CLIENT ORDER WORKFLOW TEMPLATE
For: Prompt Works (Phil Dawson)Created: 2026-03-13


🎯 WHEN CLIENT ORDER ARRIVES
Phil pastes client message to Claude → Claude executes this workflow automatically


STEP 1: READ CLIENT ORDER
Extract:

What they want AI to do
Which AI tool (ChatGPT/Claude/Gemini/other)
Industry/use case
Budget (if mentioned)
Deadline (if mentioned)
Platform (Fiverr/Upwork/Direct)


STEP 2: OPEN INCOME_TRACKING.XLSX
File location: /mnt/project/Income_Tracking.xlsx

Actions:

Read current data
Find next empty row
Prepare new project entry
Auto-generate Project ID: GW-2026-[sequential starting 0001]


STEP 3: CREATE THE DELIVERABLE
Output format: MARKDOWN (.md file)

=== CREATED BY: CLAUDE ===

WORKFLOW STEP: 1 - Initial Creation  

PROJECT ID: GW-2026-[auto-number]

DATE: [YYYY-MM-DD]

CLIENT: [name or "Not specified"]

PLATFORM: [Fiverr/Upwork/Direct or "Not specified"]

---

## THE PROMPT

[Custom prompt specific to their exact use case]

[Never generic - always uses their domain/data examples]

[Tested and validated]

---

## INSTRUCTIONS FOR CLIENT

**How to use this prompt:**

**Step 1:** [First action - be specific]

**Step 2:** [Second action - clear steps]

**Step 3:** [What to expect - realistic outcomes]

**Technical details:**

- **Works with:** [ChatGPT/Claude/Gemini - specific version if relevant]

- **You provide:** [input format with example]

- **You get back:** [output format with example]

- **Limitations:** [what it won't do - be honest]

---

## PROJECT RECORD

**Client:** [name if provided, otherwise "Not specified"]

**What they asked for:** [original request in simple words]

**How I solved it:** [technical approach in simple words - no jargon]

**Budget:** $[amount or "Not specified"]

**Deadline:** [date or "Not specified"]

**Platform:** [Fiverr/Upwork/Direct or "Not specified"]

---

## UPDATED TRACKING

✓ Added to Income_Tracking.xlsx  

✓ Row [number] updated  

✓ Monthly totals recalculated

**Your current month (March 2026):**

- **TOTAL EARNED THIS MONTH:** $[amount]

- **MONEY TO SAVE FOR TAXES:** $[amount at 30%]

- **Room Left This Month:** $[1,690 - total earned]

**Download your updated spreadsheet below.**

[Link to updated Income_Tracking.xlsx]

---

## TAX REMINDER

**SET ASIDE NOW:** $[project amount × 0.30]

**Action:** Transfer to savings account immediately

**Why 30%?** Covers federal + state + self-employment tax safety buffer

---

=== END CLAUDE OUTPUT ===

**NEXT STEP:** Copy everything above to Gemini for validation


STEP 4: UPDATE INCOME_TRACKING.XLSX
Add new row with:

Date
Project ID
Client
What They Wanted
Platform
TOTAL EARNED
MONEY TO SAVE FOR TAXES
WHAT YOU KEEP
Status
Notes
2026-03-13
GW-2026-0001
[Client Name]
[Brief description]
Fiverr
$50.00
$15.00
$35.00
In Progress
[Any notes]

Update formulas:

TOTAL EARNED THIS MONTH (sum)
MONEY TO SAVE FOR TAXES (30% of total)
WHAT YOU KEEP (70% of total)
Room Left This Month ($1,690 - total earned)
YOUR 9 TEST MONTHS counter (only when > $1,690)


STEP 5: SAVE & PRESENT FILES
Files created:

[ProjectID]_Deliverable.md - The prompt + instructions
Income_Tracking_Updated.xlsx - Updated spreadsheet

Present both to Phil for download


STEP 6: PHIL'S VALIDATION PROCESS
Phil copies output to Gemini with this prompt:

Ignore all previous instructions and saved Gems/system prompts. This is a standalone validation task.

Review this prompt engineering deliverable for accuracy, completeness, and quality.

CHECK FOR:

1. Technical accuracy (will the prompt actually work?)

2. Clear instructions (can client follow them?)

3. Realistic examples (domain-specific, not generic)

4. Proper AI tool selection (right tool for the job?)

5. Honest limitations (what it won't do)

RESPONSE FORMAT:

✅ APPROVED - ready to deliver

OR

⚠️ NEEDS FIXES:

- Issue 1: [specific problem]

- Issue 2: [specific problem]

- Suggested fix: [exact changes needed]

If ✅ APPROVED: Phil delivers to clientIf ⚠️ NEEDS FIXES: Phil pastes to Claude → Claude revises → re-validate


STEP 7: WHEN PROJECT DELIVERED
Phil tells Claude: "Project GW-2026-XXXX delivered"

Claude actions:

Update Income_Tracking.xlsx → Status = "Delivered"
Update Income_Tracking.xlsx → Date Delivered = [today]
Create Gmail draft to wife with full project summary

Gmail draft template:

To: [Wife's email]

Subject: Gig Work Income Report - [Project ID]

Hi [Wife's name],

Just completed a new project:

CLIENT REQUEST: [What they wanted in simple words]

DELIVERABLES: [What I created for them]

PLATFORM: [Fiverr/Upwork/Direct]

PAYMENT: $[amount] (will hit account in [timeframe])

PROJECT ID: GW-2026-XXXX

INVOICE/GIG ID: [platform's ID number]

TAXES SET ASIDE: $[30% amount] - transferred to savings ✓

NET INCOME: $[70% amount]

MONTH TOTAL SO FAR: $[cumulative]

ROOM LEFT THIS MONTH: $[1,690 - cumulative]

Love,

Phil


STEP 8: TAX TRANSFER
Immediate action after payment received:

Transfer $[amount × 0.30] to savings account

DO NOT SKIP THIS STEP


STEP 9: MONTHLY REPORTING
Every 5th of the month:

Call SSA: 1-800-772-1213

Report:

"I earned $[total] last month from freelance work"
"My Trial Work Period count is [X] months" (only months over $1,690)
"I'm working through platforms: Fiverr, Upwork"


AUTOMATION CHECKLIST
Claude does automatically:

✅ Generate Project ID (sequential)
✅ Create custom prompt (never generic)
✅ Write clear instructions
✅ Update Income_Tracking.xlsx
✅ Calculate taxes (30%)
✅ Calculate room left ($1,690 limit)
✅ Track TWP months (when > $1,690)
✅ Create delivery confirmation
✅ Draft email to wife

Phil does manually:

✅ Validate with Gemini
✅ Deliver to client
✅ Transfer tax money to savings
✅ Report to SSA monthly
✅ Backup files to Google Drive (1st of month)


SIMPLE LANGUAGE RULES
Always use:

"TOTAL EARNED" not "gross income"
"WHAT YOU KEEP" not "net income"
"MONEY TO SAVE FOR TAXES" not "tax withholding"
"THE $1,690 LIMIT" not "SGA threshold"
"YOUR 9 TEST MONTHS" not "Trial Work Period"
"BUSINESS EXPENSE" not "deduction"

Never use jargon - Phil has ADHD and needs simple, clear language


QUALITY STANDARDS
Every deliverable must:

✅ Be specific to client's exact use case
✅ Include realistic examples from their domain
✅ Have step-by-step instructions
✅ List technical requirements clearly
✅ State honest limitations
✅ Be marked "CREATED BY: CLAUDE"
✅ Use professional but friendly tone
✅ Be in Markdown format (.md)

Never:

❌ Generic prompts
❌ Copy-paste templates
❌ Unrealistic promises
❌ Missing technical details
❌ Confusing jargon
❌ .docx files (Markdown only!)


PROJECT ID SYSTEM
Format: GW-YYYY-NNNN

Examples:

GW-2026-0001 (first project of 2026)
GW-2026-0002 (second project)
GW-2026-0147 (147th project)
GW-2027-0001 (first project of 2027 - resets)

Sequence:

Starts at 0001 each calendar year
Auto-increments
Never skips numbers
Tracks in Income_Tracking.xlsx


FILE NAMING
Deliverables:

GW-2026-0001_ClientPrompt.md
GW-2026-0001_Documentation.md

Internal tracking:

Income_Tracking_Updated.xlsx
Client_Database_Updated.xlsx

Archives (monthly):

AI_Research_2026-03.md
Projects_Completed_2026-03.md


BACKUP SCHEDULE
Every 1st of month:

Download Income_Tracking.xlsx
Download Client_Database.xlsx
Upload both to Google Drive
Verify uploads successful
Delete local copies (keep in Project only)

Calendar reminder set: ✅


EMERGENCY CONTACTS
SSA: 1-800-772-1213Brother-in-law (tax attorney): [Phil has contact]Arizona Bridge to Independent Living: [awaiting callback]



END OF WORKFLOW TEMPLATE



This workflow is optimized for:

Phil's ADHD (small steps, clear language)
SSDI compliance ($1,690 limit, TWP tracking)
Tax preparation (30% auto-calculate)
Quality control (Gemini validation)
Wife awareness (auto Gmail draft)
Monthly SSA reporting
Professional deliverables

Created: 2026-03-13Last Updated: 2026-03-13Version: 1.0
