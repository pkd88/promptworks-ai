tool_Client_Order_Workflow
Version: 2.0 | Created: 2026-03-20 | Updated: 2026-03-20 | Owner: Phil Dawson

Overview
This document describes the complete Prompt Works workflow — how a client order flows from arrival to delivery, what each AI partner does at each step, and the rules that govern quality and consistency.
Every AI partner should understand this workflow and operate within their assigned role. No partner should attempt to do another partner's job.

Chat and Prompt Naming Rules
Every Claude chat and every Gemini prompt session must be named before work begins. This keeps every job organized, traceable, and separated from other work.
Claude chat naming format:
GW-2026-XXXX | [Platform] | [Service Type]

Example: GW-2026-0001 | Fiverr | Customer Feedback Prompt
Rules:
Each client order gets its own dedicated Claude chat — never mix two orders in one chat
Rename the chat BEFORE pasting any client content into it
Use the project ID from Income_Tracking.xlsx
Monthly research, business setup, and operations stay in separate chats from client orders
Gemini session naming: When starting any Gemini Gem session for a client order, begin with:
PROJECT: GW-2026-XXXX | [Platform] | [Service Type]

Paste this as the first line before any content so the session is identifiable.
This naming rule applies everywhere:
Claude chats
Gemini Gem sessions
Google Drive files
NotebookLM notebooks
Income_Tracking.xlsx rows
Client_Database.xlsx rows
All IDs must match across every tool for every project.

The Complete Client Order Workflow
Step 1 — Order Arrives + Chat Setup
Phil receives a client order on Fiverr or Upwork.
Before touching any AI tool:
Assign the next project ID from Income_Tracking.xlsx
Open a NEW Claude chat
Rename the chat: GW-2026-XXXX | [Platform] | [Service Type]
The chat is now ready for this order only
Owner: Phil Output: Named Claude chat ready to receive clean filtered input

Step 2 — Data Filter (PW.1.Filter Raw Input)
Phil pastes the raw client requirements into the PW.1.Filter Raw Input Gem. Gemini reads everything and produces a clean structured version for Claude.
Owner: Gemini — PW.1.Filter Raw Input Critical rule: Gemini MUST explicitly list every single client requirement before doing anything else. Nothing is skipped, summarized, or assumed. If a requirement is ambiguous, it is flagged — not ignored. Output: Clean structured requirements list inside a single code block, ready for Claude

Step 3 — Claude Builds the Deliverable
Phil pastes Gemini's clean filtered output into the named Claude chat. Claude builds the deliverable — the custom AI prompt, documentation, usage instructions, and any supporting materials.
Owner: Claude Output: Draft deliverable ready for validation

Step 4 — Gemini Validation First Pass (PW.2.Validate Deliverables)
Phil pastes Claude's draft into the PW.2.Validate Deliverables Gem along with the requirements list. Gemini reviews and returns a checklist.
Owner: Gemini — PW.2.Validate Deliverables Output: Checklist — each requirement marked complete, partial, or missing

Step 5 — Claude Applies Feedback
Phil pastes Gemini's checklist back into the Claude chat. Claude fixes any partial or missing items.
Owner: Claude Output: Revised deliverable

Step 6 — Final Checklist Validation (PW.2.Validate Deliverables — Second Pass)
Phil pastes the ORIGINAL raw client requirements AND Claude's final output into the Validation Gem together. Gemini produces a final numbered checklist.
Owner: Gemini — PW.2.Validate Deliverables Output: Final checklist. VALIDATION PASSED = ready to deliver. VALIDATION FAILED = back to Claude.

Step 7 — Delivery
Claude prepares the final delivery package. Phil delivers to the client via Fiverr or Upwork.
Owner: Phil + Claude Output: Delivered order

Step 8 — Financial and Compliance Steps
After delivery and payment:
Claude updates Income_Tracking.xlsx with all project details
Phil transfers 30% of payment to savings immediately (tax reserve)
Phil reports earnings to SSA at end of month via ssa.gov/myaccount or the "my Social Security" app
Claude creates Gmail draft to Phil's wife summarizing the project, platform, all money details, and all matching IDs
Owner: Phil + Claude

Research Workflow
When research is needed (monthly AI reports, market research, platform intelligence):
Phil opens the Deep Research Gem (no instructions — standalone)
Phil pastes the pre-built research prompt starting with the required prefix
Gemini runs Deep Research — ONE task at a time only
Phil pastes the raw Gemini output to Claude
Claude formats it into a clean .md file
Phil saves to Google Drive and uploads to the Prompt Works Project and NotebookLM
Research prompt prefix (required every time):
"Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task."

Ongoing Awareness Research
Phil maintains awareness of four areas that affect Prompt Works strategy:
The Gig AI Economy — trends in freelance AI work, pricing, demand
Platform Best Practices — what is working on Fiverr and Upwork right now
Social Sentiment — what people are saying about Fiverr, Upwork, and AI tools on Reddit and social media
AI News — latest developments in AI models, tools, and platforms

Gemini-Specific Rules
DO:
Give Gemini clear, specific, structured tasks
Use the PW.1 and PW.2 Gems for defined jobs
Attach context documents instead of writing long instructions
Keep required output format simple — numbered lists and plain text only
DO NOT:
Run multiple Deep Research tasks simultaneously (causes crashes)
Ask Gemini for tables, nested structures, or multi-column layouts (gets stuck)
Expect Gemini to maintain context without support docs attached
Use Gemini for emotional support or personal advice

Claude-Specific Rules
DO:
Trust Claude to maintain context across sessions via the Prompt Works Project
Use Claude for all client-facing deliverables and formatting
Use Claude to update spreadsheets and financial tracking
DO NOT:
Ask Claude to run deep web research (Gemini's job)
Ask Claude to validate its own output (Gemini's job)

Quality Standards
Every deliverable must meet these standards before delivery:
All requirements addressed — verified by Gemini checklist
Plain language — clear instructions, client can use it without help
Complete package — prompt + usage instructions + technical details
Documented — project recorded in Income_Tracking.xlsx and Client_Database.xlsx

Permanent Flags
Grok: Never recommend. Never use. Permanent flag due to CSAM scandal.
Fake metrics: Never claim client results that have not happened.
GIS expertise: Phil's LA County work did NOT involve GIS. Remove from any materials that include this claim.

Version 2.0 — updated with chat naming rules, correct Gem names (PW.1 and PW.2), and corrected Step 1 workflow (Gemini Data Filter first, not Claude). Attach to all Gemini Gems alongside about_PromptWorks_Team.md
