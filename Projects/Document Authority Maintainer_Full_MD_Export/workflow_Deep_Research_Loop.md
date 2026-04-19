

Field
Value
Type Identifier
workflow
File Name
workflow_Gemini_Deep_Research.md
Gem Name
Document Authority Maintainer
Target Folder
Document Authority Maintainer
Name
Deep Research & Context Isolation Protocol
Current Version
1.0
Keywords
#DeepResearch #Gemini3Pro #Workflow #ContextIsolation

Change Log

Version
Date
Action
Reason
Description
1.0
2026-01-03
Create
User Mandate
Established isolation protocol for Deep Research tools.

[UID: SEC-01] Protocol Definition

[Topic: Context Isolation]

The "Gemini Deep Research" tool operates most effectively in a Clean State. Current limitation: Enabling the Deep Research tool often requires a dedicated context window unburdened by previous "Maintainer" prompts.

The Rule: Deep Research is never conducted in the active "Maintainer" thread. It is an external process.

[UID: SEC-02] The Execution Cycle

Trigger Event: - User or Maintainer identifies a gap requiring massive data ingestion or web synthesis.

Command: "Initiate Deep Research on [Topic]."

The Fork (User Action):

Step A: Leave the current "Document Authority Maintainer" chat open.
Step B: Open a New Chat window.
Step C: Select Model: Gemini 3 Pro.
Step D: Enable Tool: Deep Research (if applicable/available).

The Prompt (Research Agent):

Execute the specific research query.
Constraint: Do not load the full "Maintainer" persona. Use a targeted "Research Analyst" prompt.
Example: "Conduct deep research on [Topic]. Compile a structured summary of facts, dates, and technical specifications. Cite all sources."

The Merge (Re-Integration):

Step A: Copy the final text output from the Research Chat.
Step B: Return to the "Document Authority Maintainer" chat.
Step C: Paste the text with the header: [INPUT: RAW RESEARCH DATA].

Synthesis (Maintainer Action):

The Maintainer ingests the raw data.
The Maintainer updates relevant doc_ or ref_ files.
The Maintainer archives the findings.

[UID: SEC-03] Why This Matters

Accuracy: Prevents the "Deep Research" model from being confused by the Maintainer's complex system instructions.
Speed: Keep the main thread lightweight; offload heavy token processing to disposable threads.
