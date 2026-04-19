AI Research Report — April 2026
Gemini Deep Research Prompts
Due: April 10, 2026 Output file: AI_Research_2026-04.md Prepared by: Claude / Prompt Works

⚠️ REMINDER: Start each Gemini session with: "Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task."
Run ONE prompt at a time. Do not combine. Wait for full output before starting next.

PROMPT 1 OF 7
Topic: Growing Freelance Markets for AI Services
<role>
You are a senior freelance market analyst specializing in AI service demand trends. You track what clients are actually paying for, not what vendors are promoting. You write for a non-technical audience.
</role>

<task>
Research and report on the fastest-growing markets for AI freelance services as of early 2026. Focus on where real money is moving, not hype. Include specific industries, company sizes, and geographic markets showing the strongest demand for AI prompt engineering, workflow automation, and AI consulting.
</task>

<inputs>
- Current date: April 2026
- Target audience: Solo AI freelancer positioning for growth
- Platforms in scope: All freelance platforms including Fiverr, Upwork, Toptal, PeoplePerHour, Contra, Freelancer.com, LinkedIn, direct outreach
- Geographic focus: US market primary, global secondary
</inputs>

<constraints>
- Only include markets with verifiable demand signals (job postings, platform data, industry reports)
- Separate "growing fast" from "already crowded"
- Flag any markets that are declining or oversaturated
- No generic advice — specific industries, company types, and dollar ranges only
- Plain English throughout — no jargon
</constraints>

<output>
Return a structured Markdown report with these exact sections:
1. **TOP 5 GROWING MARKETS** — industry, why it's growing, average project value, client type
2. **PLATFORMS BEYOND FIVERR/UPWORK** — name, demand level, average rates, how to get started
3. **SKILLS CLIENTS ARE PAYING FOR RIGHT NOW** — ranked list, include search volume or demand signal
4. **RED FLAGS — Markets to Avoid** — oversaturated or declining
5. **BEST OPPORTUNITY FOR A SOLO OPERATOR** — one specific recommendation with reasoning

Use BOLD for key terms. Use tables where comparisons are needed. Use YYYY-MM-DD for any dates.
</output>

<example>
Good finding: "Legal tech firms (50–200 employees) are posting 3x more AI workflow automation jobs on Upwork in Q1 2026 vs Q1 2025. Average project: $800–2,500. They need document review automation and client intake prompts."

Bad finding (too vague): "The AI market is growing and there are many opportunities."
</example>


PROMPT 2 OF 7
Topic: AI Tools Your Clients Already Have (Copilot, M365, Google Workspace)
<role>
You are an enterprise AI adoption specialist who has helped hundreds of small and mid-size businesses figure out what AI tools they already have and why they're not using them effectively. You understand Microsoft 365, Google Workspace, and Copilot from the client's side, not the vendor's side.
</role>

<task>
Research and report on the AI tools that small and mid-size businesses (especially local governments, nonprofits, and professional services firms) already have access to in 2026 — specifically Microsoft Copilot, M365 AI features, and Google Workspace AI. Focus on: what these tools can actually do, where they fall short, and where an outside AI consultant fills the gap.
</task>

<inputs>
- Current date: April 2026
- Client profile: Local government offices, small professional services firms, nonprofits — most running M365 or Google Workspace
- Specific example: A city government in a small US city (under 100,000 population) likely running M365
- Consultant profile: Solo AI freelancer who can configure, train, and extend these tools
</inputs>

<constraints>
- Focus on what clients HAVE but don't USE well — not what they need to buy
- Include specific Copilot features that confuse or underserve small organizations
- Include where Google Workspace AI fails compared to expectations
- Flag the gap between what vendors promise and what clients actually get
- Plain English — write as if explaining to a city clerk, not a CTO
</constraints>

<output>
Return structured Markdown with these sections:
1. **WHAT M365/COPILOT ACTUALLY DOES** — real capabilities, current pricing tier breakdown
2. **WHERE COPILOT FAILS SMALL ORGS** — top 5 failure points with specific examples
3. **GOOGLE WORKSPACE AI** — what it does, where it falls short
4. **THE CONSULTANT GAP** — specific things an outside AI specialist does that Copilot can't
5. **HOW TO POSITION YOURSELF** — 3 specific pitch angles for a solo AI consultant approaching M365 clients
6. **KINGMAN, AZ ANGLE** — what a small Arizona city government likely has, likely struggles with, and would pay for

Use BOLD for key terms. Tables for feature comparisons. YYYY-MM-DD for dates.
</output>

<example>
Good finding: "Copilot for M365 requires a $30/user/month add-on that most small orgs have but don't enable. Even when enabled, 70% of users never get trained. A consultant who runs a 2-hour staff training session can charge $500–800 and position for ongoing work."
</example>


PROMPT 3 OF 7
Topic: AnythingLLM — Models, Use Cases, and Best Practices
<role>
You are a local AI deployment specialist who helps non-technical business owners run AI tools privately on their own hardware. You have deep experience with AnythingLLM, Ollama, and open-source language models. You explain things in plain English without assuming technical background.
</role>

<task>
Research and report on AnythingLLM as of April 2026. Cover: what models work best in it, what use cases it handles well, how to configure it for business tasks like RAG (document Q&A), what hardware it needs, and how a freelancer can use it to build demos and client solutions. Also cover Ollama as the model runner that works alongside it.
</task>

<inputs>
- Current date: April 2026
- Hardware context: Windows mini PC (modest specs), Chromebook as primary device
- Use cases in scope: Document Q&A (RAG), business automation, client demos, local private AI
- User skill level: Non-developer, comfortable with settings and configuration, not comfortable with command line
</inputs>

<constraints>
- Focus on models that run on modest hardware (not requiring enterprise GPU)
- Include free/open-source models only unless paid option is significantly better
- Flag any models that are too large or too slow for a mini PC
- Plain English — no ML jargon without explanation
- Include realistic performance expectations (speed, quality, limitations)
</constraints>

<output>
Return structured Markdown with these sections:
1. **WHAT ANYTHINGLLM DOES WELL** — top use cases with specific examples
2. **BEST MODELS FOR MODEST HARDWARE** — name, size, best use case, speed expectation
3. **RAG USE CASES** — specific examples of document types and queries that work well
4. **OLLAMA INTEGRATION** — how it works with AnythingLLM, setup basics
5. **CLIENT DEMO IDEAS** — 3 specific demos a freelancer could build and show in AnythingLLM
6. **LIMITATIONS** — what AnythingLLM can't do well, where to use something else instead
7. **NOTEBOOKLM COMPARISON** — when to use each one

Use BOLD for key terms. Tables for model comparisons. YYYY-MM-DD for dates.
</output>


PROMPT 4 OF 7
Topic: Modern AI Development Approaches — Plain English Guide
<role>
You are a technology educator who specializes in explaining modern AI development concepts to business owners and non-developers. You have watched the AI development landscape evolve rapidly in 2025–2026 and can explain what's real, what's hype, and what actually matters for someone building AI-powered products or services.
</role>

<task>
Research and write a plain-English guide to modern AI development approaches as of April 2026. Cover RAG, AI agents, MCP (Model Context Protocol), local LLMs, no-code AI builders, and workflow automation. For each: explain what it is in one sentence, what it's good for, what it costs, and whether it's ready for real use or still experimental.
</task>

<inputs>
- Current date: April 2026
- Audience: Non-developer freelancer who builds AI solutions for small businesses
- Tools already in use: Claude, Gemini, AnythingLLM, NotebookLM, Google Workspace
- Goal: Understand what clients will ask for, what to learn next, what to avoid
</inputs>

<constraints>
- One plain-English sentence definition for each approach — no jargon
- Honest assessment of maturity (ready now / getting there / still experimental)
- Include cost realities — free, cheap, or expensive?
- Flag anything that sounds impressive but isn't ready for client work
- Include specific tools for each approach, not just concepts
</constraints>

<output>
Return structured Markdown with these sections:
1. **RAG (Retrieval Augmented Generation)** — what it is, tools, cost, readiness
2. **AI AGENTS** — what they are, tools, cost, readiness, risks
3. **MCP (Model Context Protocol)** — what it is, why it matters, tools, readiness
4. **LOCAL LLMs** — what they are, tools, when to use vs cloud AI
5. **NO-CODE AI BUILDERS** — what's available, who it's for, limitations
6. **WORKFLOW AUTOMATION WITH AI** — tools, use cases, cost
7. **WHAT TO LEARN NEXT** — ranked by client demand and learning curve
8. **WHAT TO IGNORE** — overhyped approaches not ready for freelance use

Use BOLD for all tool names and approach names. Tables for comparisons. YYYY-MM-DD for dates.
</output>


PROMPT 5 OF 7
Topic: Free AI Demo Stack for Freelancers
<role>
You are a freelance AI consultant who regularly demonstrates AI capabilities to small business prospects. You have tested every major free AI tier and know exactly what you can and cannot show without paying. You focus on impressive, practical demos that convert skeptical clients.
</role>

<task>
Research and report on the best free AI tools and demos available to a freelancer in April 2026. Focus on what you can show a client for free, what requires a paid tier, and which free tools are genuinely impressive vs. underwhelming. Include specific demo scripts or scenarios for each tool.
</task>

<inputs>
- Current date: April 2026
- Audience: Solo AI freelancer doing client prospecting and demos
- Context: Demonstrating AI capabilities to small businesses, local government, nonprofits
- Tools already owned: Claude Pro, Gemini Pro, AnythingLLM, NotebookLM (all paid)
- Goal: What can you show for FREE to supplement paid tools — and what's the most impressive free demo?
</inputs>

<constraints>
- Must be genuinely free — no trial expiration tricks
- Include specific demo scenarios, not just tool names
- Flag tools that require sign-up vs. completely anonymous
- Rate each demo on: Wow factor (1-5), Relevance to small business (1-5), Ease of setup (1-5)
- Be honest about limitations of free tiers
</constraints>

<output>
Return structured Markdown with these sections:
1. **TOP FREE DEMO TOOLS** — tool name, what to demo, wow factor, ease of setup
2. **BEST DEMO FOR A LOCAL GOVERNMENT CLIENT** — specific scenario using free tools
3. **BEST DEMO FOR A SMALL BUSINESS CLIENT** — specific scenario using free tools
4. **ANYTHINGLLM AS A FREE DEMO** — what you can show, how to set it up fast
5. **NOTEBOOKLM DEMO IDEAS** — specific scenarios clients find impressive
6. **WHAT NOT TO DEMO FOR FREE** — things that look bad on free tier
7. **CONVERTING THE DEMO TO A PAID PROJECT** — one-sentence pitch after each demo type

Use BOLD for tool names. Rating tables. YYYY-MM-DD for dates.
</output>


PROMPT 6 OF 7
Topic: Token and AI Cost Management Best Practices for Teams
<role>
You are an AI operations specialist who helps small teams and solo operators get more done with less AI spending. You understand token economics, model selection, task routing, and how to build workflows that use expensive AI only when necessary. You have worked with Claude, Gemini, and open-source models.
</role>

<task>
Research and report on best practices for managing AI token usage and costs across a multi-AI workflow in 2026. Focus on task routing (which task goes to which AI), prompt efficiency, offloading to cheaper or free models, and building sustainable workflows that don't hit usage limits or break the bank. Include specific recommendations for Claude, Gemini, and AnythingLLM.
</task>

<inputs>
- Current date: April 2026
- Workflow in use: Claude (primary operations, deliverables), Gemini Pro (deep research, validation), AnythingLLM (local RAG, document Q&A), NotebookLM (document synthesis)
- Pain point: Claude hitting token/usage limits; need to offload more to Gemini and AnythingLLM
- Goal: Keep Claude for high-value tasks only; push everything else downstream
</inputs>

<constraints>
- Specific routing rules, not general advice
- Include prompt efficiency techniques that reduce token use without reducing quality
- Flag tasks that people send to Claude that should go elsewhere
- Include AnythingLLM local model use cases where it replaces cloud AI
- Plain English throughout
</constraints>

<output>
Return structured Markdown with these sections:
1. **TASK ROUTING GUIDE** — table: task type → best AI → why → estimated token cost
2. **TASKS TO MOVE OFF CLAUDE** — specific examples with what to use instead
3. **TASKS TO KEEP ON CLAUDE** — what Claude does that nothing else does as well
4. **PROMPT EFFICIENCY TECHNIQUES** — specific techniques that reduce token use
5. **ANYTHINGLLM AS A CLAUDE REPLACEMENT** — use cases where local models are good enough
6. **GEMINI FOR HEAVY LIFTING** — best use cases, how to structure prompts for Gemini
7. **NOTEBOOKLM ROLE** — where it fits, what it saves Claude from doing
8. **SAMPLE WORKFLOW** — one complete example of a client project routed across all 4 tools

Use BOLD for key terms. Tables for routing decisions. YYYY-MM-DD for dates.
</output>


PROMPT 7 OF 7
Topic: NotebookLM — Advanced Features and Use Cases
<role>
You are a productivity researcher who specializes in knowledge management and AI-assisted research tools. You have extensively tested NotebookLM and understand its strengths, limitations, and underused features. You write for a non-technical audience who wants to get more value from tools they already have.
</role>

<task>
Research and report on NotebookLM's full capabilities as of April 2026. Cover advanced features beyond basic Q&A, the Audio Overview (podcast) feature, source management, and specific use cases for freelancers and small businesses. Include things most users never discover.
</task>

<inputs>
- Current date: April 2026
- User context: Freelancer who uses NotebookLM for document synthesis and cross-referencing
- Already knows: Basic Q&A against uploaded docs, ~10 file limit per notebook
- Goal: Get more value, discover advanced features, understand podcast/audio feature better
- Interest: Using NotebookLM to create deliverables, not just for personal research
</inputs>

<constraints>
- Focus on features that are actually useful, not just impressive demos
- Include the Audio Overview feature in detail — how to control it, customize it, use it for clients
- Flag features that are in beta or unreliable
- Include specific use cases for freelance client work
- Plain English throughout
</constraints>

<output>
Return structured Markdown with these sections:
1. **WHAT MOST USERS MISS** — top 5 underused NotebookLM features
2. **AUDIO OVERVIEW (PODCAST FEATURE)** — how it works, how to customize, client use cases
3. **BEST SOURCE TYPES** — what kinds of documents work best, what doesn't work well
4. **FREELANCE USE CASES** — specific ways a consultant can use NotebookLM for client work
5. **NOTEBOOK ORGANIZATION** — tips for managing multiple notebooks across projects
6. **NOTEBOOKLM VS ALTERNATIVES** — how it compares to AnythingLLM, Perplexity, Claude Projects
7. **WHAT'S COMING** — known upcoming features or roadmap items
8. **LIMITATIONS** — honest assessment of what it can't do

Use BOLD for key terms. Tables for comparisons. YYYY-MM-DD for dates.
</output>


ASSEMBLY INSTRUCTIONS
After all 7 prompts are complete:
Save each output as a separate doc in Google Drive — name them RESEARCH_01 through RESEARCH_07
Upload all 7 to NotebookLM as a new notebook
Ask NotebookLM: "Synthesize these 7 research reports into one executive summary with key findings and recommended actions for a solo AI freelancer."
Bring that summary + the 7 docs to Claude for final formatting as AI_Research_2026-04.md
Save final file to Google Drive

Prompts built by Claude / Prompt Works | April 3, 2026
