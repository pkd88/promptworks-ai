AI Task Capture Protocol v1.0
Purpose: Standardize how AI assistants (Claude, Gemini, Haiku) flag tasks during conversations for Phil's Master To-Do List.

Last Updated: 2026-03-29


Core Principles
Flag, Don't Execute — AI cannot write to Phil's Excel. AI flags tasks; Phil copies.
Full Context Always — Never just task name. Include why, what, dependencies.
Chat Source Tracking — Always include which conversation this came from.
Type Classification — Distinguish between regular tasks, parking lot items, recurring prep.


When to Capture Tasks
Explicit Requests
User: "Add to my list: test DAM multi-file"

→ Capture immediately
Implicit Mentions
User: "I should really update those test scenarios"

→ Flag: "📝 Captured for your to-do list"
Parking Lot Items
User: "Explain that later, I need to focus now"

→ Flag: "🅿️ PARKING LOT: [topic]"
End-of-Session
User: "What should I add from this conversation?"

→ Summarize all flagged items


Capture Format
Standard Task Format
📝 TODO: [Task Name]

Priority: [P1/P2/P3] (suggested)

Context: [Full explanation - why, what, dependencies]

Status: Not Started

Source: [AI name]

Source Chat: "[Exact chat name]"

Project: [PromptWorks/ShareWithMe/DAM/LA Kings/Personal]

Type: Task

Date: [YYYY-MM-DD]

[Ready to copy to Excel]


Parking Lot Format
🅿️ PARKING LOT: [Topic to explain later]

Task: [Understand/Review/Explain X]

Context: [What was being discussed when this was parked]

Source: [AI name]

Source Chat: "[Exact chat name]"

Priority: P3 (default for parking lot)

Type: Parking Lot

Date: [YYYY-MM-DD]

[Phil: Review this chat later for full explanation]


Recurring Prep Format
🔁 RECURRING: [Prep task name]

Task: [Task name]

Context: [What needs doing]

Recurrence: [Weekly/Monthly/etc.]

Reminder: [How far in advance]

Due Date: [Next occurrence]

Type: Prep Item

Priority: [P1/P2/P3]

[Set up recurring in Excel]


Urgent Flag Format
⚠️ URGENT (P1): [Task name]

Context: [Why urgent, what's blocking]

Due Date: [If known]

Dependencies: [What's blocked by this]

[Add to Excel immediately]


Examples
Example 1: Standard Task
User: "I need to test that DAM multi-file thing"

AI Response:

"📝 TODO: Test DAM v2.2 multi-file upload

Priority: P1 (suggested - you're actively working on DAM)

Context: Verify waiting room logic works in Gemini Pro. Upload 3+ files, 

ensure menu only appears after 'ready' command. Check if Option 4 

(Master Merge) highlights correctly for multiple files.

Status: Not Started

Source: Claude

Source Chat: 'DAM Multi-File Upload Fix'

Project: DAM

Type: Task

Date: 2026-03-29

Ready to copy to Excel?"


Example 2: Parking Lot
User: "Wait, how does that storage thing work? Explain later, 

I need to finish this first."

AI Response:

"🅿️ PARKING LOT: Understand persistent storage API

Task: Get full explanation of window.storage for Claude Artifacts

Context: Mentioned during Tourism AI menu discussion. Phil wanted to 

know if similar functionality exists in Gemini. Couldn't dive deep 

during active conversation.

Source: Claude

Source Chat: 'Tourism AI Business Model'

Priority: P3

Type: Parking Lot

Date: 2026-03-29

[Review this chat later when you have time]"


Example 3: End-of-Session Summary
User: "What should I add to my list from today?"

AI Response:

"From today's conversation, here are 6 tasks to add to Excel:

---

⚠️ P1 TASKS (Urgent):

1. Test DAM v2.2 multi-file upload

   Context: Verify waiting room logic, test with 3+ files

   Project: DAM

   Source Chat: 'DAM Multi-File Upload Fix'

2. Build Tourism AI demo

   Context: Kingman, AZ proof of concept with Featured Listings

   Project: PromptWorks

   Source Chat: 'Tourism AI Business Model'

---

📋 P2 TASKS (Important):

3. Merge persona libraries

   Context: Combine Gemini's 17 + Claude's 29, resolve duplicates

   Project: ShareWithMe

   Source Chat: 'Persona Library Build'

4. Document prefix system examples

   Context: Add use-case scenarios to ref_Prefix_System_v3.md

   Project: Personal

   Source Chat: 'Prefix System Reconciliation'

---

🔵 P3 TASKS (Someday):

5. Research Vin Scully quotes

   Context: Use Deep Research for persona card refinement

   Project: LA Kings

   Source Chat: 'Persona Library Build'

---

🅿️ PARKING LOT:

6. Understand persistent storage API

   Context: window.storage explanation parked during Tourism AI talk

   Type: Parking Lot

   Source Chat: 'Tourism AI Business Model'

---

Copy these to Excel when ready. All have Source = Claude, 

Date = 2026-03-29."


Priority Guidelines
P1 (High Priority / Urgent)
Blocking other work
Client deliverables with deadlines
System fixes preventing use
Time-sensitive opportunities

Examples:

Complete PromptWorks order (deadline approaching)
Fix bug preventing DAM usage
Test before demo to client


P2 (Medium Priority / Important)
Enhances existing systems
Improves workflow
Part of larger ongoing project
Can be scheduled but shouldn't be ignored

Examples:

Merge persona libraries
Document prefix system
Update ShareWithMe test scenarios


P3 (Low Priority / Someday)
Nice to have
Research/learning
Experimental ideas
No urgency or blocking

Examples:

Research new personas
Explore new AI features
Read documentation for future features


Context Writing Guidelines
Good Context (Full):

Context: Create Kingman, AZ tourism guide as proof of concept for 

PromptWorks product. Include Featured Listings tier to demonstrate 

monetization model. Use as sales tool for pitching other cities. 

Show potential clients what's possible with menu-driven AI. 

Depends on: finalizing menu structure system (currently in progress).

Bad Context (Insufficient):

Context: Build tourism demo



Good Context includes:

Why this matters (goal, motivation)
What specifically needs doing
How it fits into larger project
Dependencies (what's needed first)
Use case (when/where this will be used)


Chat Source Tracking
Always include exact chat name:

Source Chat: "Tourism AI Business Model"

Source Chat: "DAM Multi-File Upload Fix"

Source Chat: "Persona Library Build"

Why this matters:

Phil can return to exact conversation
Full context available if needed
Track which conversations were most productive
Don't lose important discussions


Special Cases
Multiple Tasks from One Statement
User: "I need to test DAM, merge the personas, and build that demo"

AI: "That's 3 separate tasks. Let me break them down:

📝 TODO 1: Test DAM v2.2 multi-file upload

[Full capture]

📝 TODO 2: Merge persona libraries  

[Full capture]

📝 TODO 3: Build Tourism AI demo

[Full capture]

Copy all 3 to Excel?"


Task Evolution During Conversation
[Early in conversation]

User: "I should document the menu system"

[Later in conversation - understanding deepens]

User: "Actually, it's not just menus - it's a whole router system"

AI: "Want me to update that todo?

Original: Document menu system

Updated: Document specialist router system (JSON-based)

Context: [expanded with new understanding]

Update Excel with revised version?"


Discovering Task is Already Done
User: "I need to fix the DAM apology loop"

AI: "Actually, we already fixed that in v2.2 - added clarified 

error handling per mode. That's in the document we built today.

Should I mark anything as done in your list, or were you 

thinking of something different?"


Integration with Excel
Phil's Workflow
During chat: AI flags tasks with 📝/🅿️/🔁/⚠️
End of session: Request summary if needed
Copy to Excel: Paste into appropriate columns
Add chat name: Fill in Source Chat column
Set reminders: Add Reminder Date if needed
AI's Role
Flag tasks during conversation
Provide full context
Classify by type/priority
Make copy-paste easy
Don't overwhelm with flags (quality over quantity)


Quality Checklist
Before flagging a task, verify:

✅ Is this actually actionable? (not just discussion)
✅ Is the context complete? (includes why/what/dependencies)
✅ Is priority appropriate? (P1/P2/P3 makes sense)
✅ Is type correct? (Task/Parking Lot/Recurring/Prep)
✅ Is source chat included?
✅ Is this a new task? (not already in Phil's list)


END OF PROTOCOL
Version: 1.0Last Updated: 2026-03-29Maintainer: Phil Dawson / ClaudeFile: ref_AI_Task_Capture_Protocol.md
