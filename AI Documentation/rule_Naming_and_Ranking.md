rule_Naming_and_Ranking
Version: 1.0 | Created: 2026-03-20 | Owner: Phil Dawson Purpose: Defines all file naming conventions, DAM prefixes, file hierarchy, and notebook placement rules for Prompt Works. Applies to: All files, docs, notebooks, gems, chats, and project IDs across all tools.


THE CORE RULE
Phil names everything. AI names nothing.

No AI partner — Claude, Gemini, NotebookLM, or PPX — ever assigns a name to a file, document, notebook, or any other asset. If a name is needed and Phil has not provided one, the AI asks Phil for it first. This rule exists because AI-generated names are unpredictable, inconsistent, and occasionally embarrassing. (See: NANO BANANA2.)


FILE PREFIX SYSTEM (DAM PREFIXES)
Every file in the Prompt Works system uses a prefix that identifies its type and function. The prefix determines where the file lives, how it is used, and whether it belongs in the shared context notebook.
PREFIX DEFINITIONS
Prefix
Full Name
What It Is
Example
about_
About Document
Describes a person, team, or system. Background and identity context.
about_PromptWorks_Team.md
context_
Context Document
Rules, settings, or operational parameters for a specific tool or gem.
context_Deep_Research_Rules.md
rule_
Rule Document
Non-negotiable standards that apply across tools or workflows.
rule_Naming_and_Ranking.md
ref_
Reference Document
A reference guide or knowledge base document. Looked up, not acted on.
ref_Prompt_Engineering_Guide.md
tool_
Tool Document
Contains prompts, scripts, or instructions that are actively executed.
tool_Gemini_Research_Prompts.md
index_
Index Document
A master list or table of contents for a system or folder.
index_Master_List.md
AI_Research_
Research Archive
Monthly or quarterly research reports. Date-stamped.
AI_Research_2026-03.md
GW-
Project Record
Client project deliverables and documentation. ID-stamped.
GW-2026-0001_deliverable.md


NOTEBOOK PLACEMENT RULES
Not every file belongs in the shared PW context notebook. Putting the wrong files in a shared notebook causes AI partners to act on documents they should only reference — or worse, execute tool prompts during the wrong task.
SHARED PW CONTEXT NOTEBOOK — PASSIVE FILES ONLY
These file types go in the shared notebook that is attached to all Gems:

✅ about_ — always in shared notebook ✅ context_ — always in shared notebook ✅ rule_ — always in shared notebook ✅ ref_ — always in shared notebook
DO NOT PUT IN SHARED NOTEBOOK
These file types are active — they contain prompts or instructions that get executed. Putting them in a shared notebook risks unintended execution.

❌ tool_ — call explicitly when needed, do not leave in shared notebook ❌ GW- — project files, live in Google Drive by project ID ❌ AI_Research_ — archive files, live in dedicated research notebook
GEM-SPECIFIC NOTEBOOKS
Some gems have their own dedicated notebook in addition to the shared PW context notebook. Gem-specific files (like a thumbnail style guide) live in the gem's own notebook, not the shared one.

Gem
Shared PW Notebook
Gem-Specific Notebook
PW.0.Deep Research
✅
Research archive notebook
PW.1.Filter Raw Input
✅
None
PW.2.Validation
✅
None
PW.3.Thumbnail Generator
✅
Thumbnail notebook (style guide + sample image)


GEM NAMING CONVENTION
All Prompt Works Gems follow this format:

PW.[NUMBER].[Function Name]

Current gems:

Gem Name
Function
PW.0.Deep Research
Research engine — runs monthly and quarterly research prompts
PW.1.Filter Raw Input
Data filter — cleans client orders for Claude
PW.2.Validation
Validation — checks Claude output against requirements
PW.3.Thumbnail Generator
Image generation — creates consistent branded thumbnails

Rules:

PW prefix always — never WP or any other variation
Number reflects workflow order where applicable
Function name is plain English, no abbreviations
Phil assigns all gem names — Gemini never names a gem


CLAUDE CHAT NAMING CONVENTION
Every Claude chat must be named before work begins. Format:

GW-2026-XXXX | [Platform] | [Service Type]

Examples:

GW-2026-0001 | Fiverr | Customer Feedback Prompt
GW-2026-0002 | Upwork | Email Automation Prompt
GW-2026-0003 | Direct | MS Access Database Cleanup

Rules:

One client order per chat — never mix two orders
Rename the chat BEFORE pasting any client content
Use the project ID from Income_Tracking.xlsx
Monthly research, business setup, and operations use descriptive names without GW- prefix
Examples of non-client chats: Research - March 2026, Business Setup - March 2026


PROJECT ID SYSTEM
All client projects are assigned a sequential ID at the start of the order workflow.

Format:

GW-2026-XXXX

Rules:

GW = Gig Work
2026 = year (updates each year)
XXXX = sequential four-digit number starting at 0001
Next available ID is always in Income_Tracking.xlsx
The same ID appears on every record related to that project — Claude chat, Income_Tracking.xlsx row, Client_Database.xlsx row, deliverable file, Gmail draft to wife

Current next ID: GW-2026-0001 (no completed projects yet as of 2026-03-20)


GEMINI SESSION NAMING
When starting any Gemini Gem session for a client order, begin with:

PROJECT: GW-2026-XXXX | [Platform] | [Service Type]

Paste this as the first line before any content so the session is identifiable.


FILE DATING CONVENTION
All dates in filenames and document headers use ISO format:

YYYY-MM-DD

Examples:

AI_Research_2026-03.md — monthly research archive
2026-03-20 — date references inside documents

Never use MM/DD/YYYY or any other format. ISO format sorts correctly and is unambiguous across regions.


SUMMARY — QUICK REFERENCE
What
Format
Example
File prefix
type_FileName.md
rule_Naming_and_Ranking.md
Client project ID
GW-YYYY-XXXX
GW-2026-0001
Claude chat
GW-2026-XXXX | Platform | Service
GW-2026-0001 | Fiverr | Feedback Prompt
Gem name
PW.N.Function
PW.3.Thumbnail Generator
Date format
YYYY-MM-DD
2026-03-20
Research archive
AI_Research_YYYY-MM.md
AI_Research_2026-03.md



This document belongs in the shared PW context notebook and the Prompt Works Claude Project. Phil names everything. AI names nothing.
