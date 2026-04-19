AI Research Report — April 2026
Prompt Works | Phil Dawson Report Date: 2026-04-08 Coverage Period: April 2026 Sources: 13 Gemini Deep Research files (Prompts 2.1–2.13, excluding 2.9)


Table of Contents
Prompting Methods and Techniques
Freelance Platform Intelligence
AI Model Landscape
Social Media and Gig Economy Trends
Client Communication Best Practices
MS Access and Spreadsheet Market
AI User Experience and Community Feedback
AI Training Platform Intelligence
Winning Work Intelligence
Skill Building Path
Niche Market Finder
Self-Hosted and Free AI Tools
Pricing Comparison Tables
Key Takeaways for Prompt Works


1. Prompting Methods and Techniques
The Big Picture
The industry declared a "March AI Model War" with twelve major model updates shipping in a single month. As of April 2026, prompting is treated as a deterministic engineering discipline, not creative writing. Output quality is now split roughly 30% model / 70% prompt structure.
Claude (Anthropic)
The dominant architecture rule is the Four-Block Pattern: INSTRUCTIONS → CONTEXT → TASK → OUTPUT FORMAT. Long documents go at the top of the prompt, before the query. The opposite of what most people do.

What works: XML tags (Claude is the undisputed leader in XML adherence), multishot examples wrapped in tags, role prompting tied to verification constraints, grounding quotes for long-document tasks.

What kills performance: Negative constraints ("do not use markdown"), adjective-heavy prompting ("be very smart"), unstructured dense paragraphs, instructions placed after long context blocks.
GPT-5.4 (OpenAI)
Released 2026-03-05. Uses 47% fewer tokens on complex reasoning than previous models. Instructions must bracket the content — put them both before AND after the context payload. This is the exact inverse of Claude.

What works: Metaprompting (GPT-5.4 can optimize its own prompts), chain-of-thought summaries at the start of answers, explicit tool preambles for agents, examples placed under a dedicated # Examples header in the system prompt.

What kills performance: Implicit assumptions, instructions placed only at the end, over-engineering.

New parameters: reasoning_effort (minimal/low/medium/high) and verbosity (low/medium/high) at the API level.
Gemini 3.1 Pro
Data payload goes at the top, task goes at the bottom — same as Claude. Requires a bridge phrase like "Based on the information above..." between the data and the query or attention degrades. Keep temperature at default 1.0 — lowering it causes logic failures.

What works: Multimodal parity (treat text, image, audio, video equally), explicit planning + self-critique steps, temporal anchoring ("Remember it is 2026 this year"), strict grounding prompts.

What kills performance: Long personality prompts, vague adjectives, spray-and-pray outbound prompts.
Grok 4.20 — ⚠️ [PROBLEMATIC]
Released 2026-03-10. Despite advertising a 2M token context window, suffers severe attention degradation on long documents. C.A.R.E. framework helps (Context, Action, Role, Expectation). Not recommended for document synthesis.
DeepSeek — ⚠️ [CHINESE MODEL]
Reasoning model built on reinforcement learning. Parameter rules: temperature 0.6 + top_p 0.95 for analysis; temperature 0.0 for code and math. Never adjust both temperature AND top_p simultaneously. Requires high max_tokens to prevent output truncation.
Perplexity
Think like a web search user, not a chatbot user. Add domain terminology and timeframes to every prompt. Use Deep Research mode for queries with 3+ sub-questions. Never use few-shot examples — Perplexity will search the internet for the fictional examples instead of answering the real question.
AnythingLLM
Invoke @agent at the start of the prompt to access tools. Uses the base model's prompting rules (Claude if Claude is connected, GPT if GPT is connected). System Prompt Variables allow dynamic context injection without reprompting.
Llama 4 Scout (Meta) — 10M Token Context
Brief framing statement → massive data → query at the bottom. Sequential batching: load the context once, ask multiple questions in the same session. Temperature 0.1 for coding.
Cross-Model Summary Table
Model
Instructions
Data
XML?
Few-Shot?
Temp for Code
Claude Opus/Sonnet 4.6
Bottom
Top
✅ Best
✅ Mandatory
N/A
GPT-5.4
Both ends
Middle
⚠️ If told
✅ In system
N/A
Gemini 3.1 Pro
Bottom
Top
✅ Good
✅ Good
1.0 (default)
Llama 4 Scout
Bottom
Middle
⚠️ Moderate
✅ Good
0.1
DeepSeek
Bottom
Top
⚠️ Limited
⚠️ Careful
0.0
Perplexity
Query style
Brief
❌ No
❌ Breaks it
N/A


2. Freelance Platform Intelligence
Fiverr — Structural Decline, Premium Pivot
Active buyer count dropped to 3.1 million (down from 4.3M peak). Stock down 35%+. The platform is losing buyers but increasing spend-per-buyer to $342 (+13.3%). Transactions over $1,000 grew 23%.

What's selling:

AI automation and workflow builds: $500–$2,000+ per project
Advanced prompt architecture (RAG, meta-prompts): $150–$250/hour
Specialized consulting sessions: $100–$300 for 30–60 minutes

What's dead: Generic content creation, basic API integrations, anything a ChatGPT wrapper can do in 5 minutes.

Algorithm changes: Fiverr shut down Fiverr Workspace (formerly AND.CO) on 2026-03-01. AI-generated gig summaries now override sellers' own copy with no opt-out. Search penalties for editing gig titles too frequently, but also penalties for total stagnation.

Key warning: Promoted Gig ROAS has collapsed. The same $100 ad spend that generated $1,000 in sales in 2024 now frequently yields negative returns.

Buyer frustration: "AI slop" — clients pay for work and receive raw unedited LLM output. This is driving high-value buyers off the platform entirely.

Protective policy reminder: No-show and scope creep protections MUST appear in the Fiverr message thread at order start. A seller recently lost a $100+ dispute because a no-show policy wasn't written in the gig description.
Upwork — Enterprise Pivot, Hostile to Freelancers
Revenue: $769M in 2024, projected $835–850M in 2026. But this money is increasingly extracted from freelancers, not clients.

What's selling:

AI automation specialists: $120–$200+/hour
MS Access and legacy database services: $40–$100/hour (dark horse goldmine)
Senior information architects (AI doc QA): $50–$150/hour

What's dead: Basic data entry, generic copywriting, simple API integrations.

Policy changes that hurt sellers:

Variable fee now defaults to permanent 15% on most contracts
Bonus payment commission raised from 10% to 15%
Specialized Profiles deprecated 2026-05-28
Connect inflation: Jobs that cost 4–8 connects in 2024 now cost 28–32 connects ($4.20–$4.80 per application)

The Top Earner playbook: Stop bidding on the job feed. Use Connects to boost profile. Win entirely through inbound invitations. Top earners (clearing $30K+/quarter) have abandoned outbound bidding entirely.
Emerging Platforms
Jobbers.io: Zero commission, 300K daily visits, becoming the destination for high-end AI automation talent. Contra: Zero commission, portfolio-first discovery, $45M funding. Braintrust: Web3 DAO, 0% from freelancers / 10% from clients, rigorous vetting (top 2-3% accepted).

Enterprise projects on these platforms: $25,000–$150,000. Monthly AI strategy retainers: $15,000–$50,000.


3. AI Model Landscape
Market Overview
ChatGPT market share dropped from 87% to ~60-68%. Google Gemini up 237% YoY. Claude commands ~4.5% consumer footprint but generates disproportionate enterprise revenue. Perplexity up 370% with 5.8% share.
Model Pricing Comparison Table
Model
Input $/M tokens
Output $/M tokens
Context Window
Consumer Sub
Claude Opus 4.6
$5.00
$25.00
1M
$20–$200/mo
Claude Sonnet 4.6
$3.00
$15.00
1M
Same
Claude Haiku 4.5
$1.00
$5.00
200K
Same
GPT-5.4
$2.50
$15.00
Varies
$8–$200/mo
GPT-5.4 mini
$0.75
$4.50
Varies
Included
GPT-5.4 nano
$0.20
$1.25
32K
Included
Gemini 3.1 Pro
$2.00
$12.00
1M
$19.99/mo
Gemini 3.1 Flash-Lite
$0.25
$1.50
1M
Free tier
Grok 4.20 ⚠️
$2.00
$6.00
2M
$40–$300/mo
Grok 4.1 Fast ⚠️
$0.20
$0.50
2M
Included
DeepSeek V4 ⚠️🇨🇳
$0.30
$0.50
1M
Free
Mistral Small 4
$0.15
$0.60
256K
$14.99/mo
Kimi K2.5 🇨🇳
$0.60
$2.50
256K
$19/mo
Qwen 3.6 Plus 🇨🇳
~$0.86
~$3.44
1M
Via Alibaba
Perplexity Pro
Per-call
Per-call
Varies
$20/mo
Notable Model Events (Q1 2026)
2026-02-01: Claude Sonnet 4.6 and Opus 4.6 officially released
2026-02-19: Gemini 3.1 Pro Preview launched
2026-03-05: GPT-5.4 launched; GPT-5.1 deprecated
2026-03-10: Grok 4.20 launched
2026-03-13: Claude 1M token context graduated from beta
2026-04-01: Google AI Pro storage upgraded from 2TB to 5TB
2026-04-03: GPT-4o, GPT-4.1 deprecated from ChatGPT
2026-04-04: Anthropic restricted third-party agent framework use on subscriptions
Claude — Key Points for Prompt Works
Claude Opus 4.6 leads on GPQA Diamond (87.4%) and SWE-Bench Verified (80.8%). Best for complex reasoning, long-context document work, multi-agent frameworks. The token throttling controversy (2026-04-04 restriction of OpenClaw/third-party agents) has fractured the open-source developer community.
Chinese AI Models — Security Warning
⚠️ DeepSeek, Kimi, Qwen: All subject to China's National Intelligence Law. Data stored on servers in China. Multiple government bans on official devices. CrowdStrike confirmed that DeepSeek-R1 is 50% more likely to produce code with hidden security vulnerabilities when prompts touch politically sensitive topics. Use dummy data only. "Improve the model" toggle must be OFF. Never use with real client data.
NotebookLM — Breakout Success
2026 update added interactive audio (click "Join" to enter the podcast), cinematic video overviews, AI slide generator, 10 infographic styles, 10,000-character custom instructions. Now surpassed Perplexity in total site visits over the past two months.

Free tier: 50 sources/notebook, 3 audio overviews/day. Pro ($19.99/mo): 300 sources, 20 deep research queries.


4. Social Media and Gig Economy Trends
The Death of Generic AI Content
Consumer preference for AI-generated content plummeted from 60% (2023) to 26% (early 2026). "AI slop" was Macquarie Dictionary's 2025 Word of the Year. The market now pays a premium for "messiness" — natural pacing, conversational stutters, minor imperfections that signal human effort.

84% of freelancers use AI tools. Over 90% use them superficially (basic text generation). The elite 10% use strategic stacks: autonomous agents, overnight lead scraping, 150-hour manual tasks automated to zero.
Platform Algorithm Changes
X/Twitter: Highly transparent algorithmic mechanics now published. Organic reach for non-premium accounts suppressed. Ads Revenue Sharing requires 5M impressions over 90 days among Premium users. Major DDoS attack 2026-04-01 confirmed by Musk.

LinkedIn BrowserGate (2026-04-04): LinkedIn's JavaScript was scanning users' computers for 6,000+ installed extensions and logging 48 hardware characteristics without consent. EU regulatory investigation underway.

Instagram: "Your Algorithm for Reels" launched 2025-12-10 — users can now delete topics and hard-steer recommendations. Static carousels now outperform Reels in engagement rate.

TikTok: Legacy Creator Fund abolished. New Creator Rewards Program requires: original video, 1+ minute, high search value. AI dubbing, AI fashion video, AI listing generators all added.

YouTube: As of January 2026, fully AI-generated content (no human transformation) is demonetized. Voice cloning of real people without consent = instant channel strike. YouTube Shorts optimal length: 50–60 seconds.
Gig Economy Legal Landscape
EU Platform Work Directive: Transposition deadline 2026-12-02. If platforms control pay, monitor performance, or restrict the worker's client base, workers are legally presumed employees with full rights. Bans AI monitoring of workers' emotional states.

US DOL rule change (2026-02-26): Proposed rollback of Biden-era contractor rules. Comment period closes 2026-04-28. Would reinstate "economic reality" two-factor test, making it easier to classify gig workers as independent contractors.
Income Trends — The Barbell Economy
The freelance middle class is being hollowed out. Two groups survive:

Commodity workers earning poverty wages on oversaturated services
Strategic orchestrators running AI-powered agency-level output as solo operators, earning $10K–$30K+/month

The pivot: Stop selling time. Sell outcomes. "I guarantee 20 qualified B2B sales meetings a month" → indispensable operational partner. "I write content" → replaceable.


5. Client Communication Best Practices
The Core Problem: Stochasticity
Clients expect LLMs to behave like traditional software (deterministic inputs = identical outputs). They don't. Educating clients on stochasticity is the most critical onboarding conversation. If a client thinks variation = bug, you'll be stuck in infinite unpaid revisions.
Scope Management Scripts
The "Alternative Choice Framework" for pushback: never refuse outright, never accept free work. Give a choice: Option A (stay in scope) or Option B (change order for new scope with cost and timeline). This removes emotion and forces a business decision.

Four types of revision:

Format Drift → prompt engineering fix
Terminology Drift → RAG or few-shot fix
Policy Drift → may need fine-tuning
Retrieval Gap → cannot be fixed by prompting; requires new data
Upwork Dispute System — Critical Knowledge
Upwork mediators do NOT evaluate work quality. They suggest a 50/50 split. Malicious clients dispute $200–$300 milestones knowing no freelancer will pay $350 arbitration to recover $300.

Counter-move: Section 7.1 of Upwork's Arbitration Procedure — if one party pays the fee and the other doesn't, the participating party wins by default and gets the fee refunded. Call the bluff.
Platform-Specific Rules
Fiverr: Response time tiers — under 1 hour = "Excellent" boost; 12–24 hours = slight penalty; 24+ hours = severe suppression. Custom offers that go unaccepted or are withdrawn count against you. Achieve explicit verbal agreement on scope before sending the formal offer.

Upwork: Contracts over $200 positively impact JSS. Contracts under $200 provide zero algorithmic benefit. Optimal proposal length: 150–800 words. Never use "Dear Hiring Manager" openers.
Protective Contract Clauses (Must Appear in Message Thread)
Stochasticity acknowledgment clause
Data quality limitation (you're not liable for bad outputs from bad input data)
Explicit exclusion list (what's NOT included)
Defined revision policy (prompt engineering vs. fine-tuning)
Communication protocols (response times, single point of contact)


6. MS Access and Spreadsheet Market
MS Access — Premium Service Territory
Access is transitioning from rapid application development to specialized maintenance, migration, and rescue. The supply of qualified developers is shrinking fast (bootcamps and universities no longer teach it).

Microsoft changes affecting clients:

Database Compare tool retiring June 2026 → forces urgent consultancy
SharePoint CSP enforcement March 2026 → broke many workflows
VBScript deprecated → legacy automations breaking everywhere
New: Zoom slider April 2026; 22-inch form limit removed June 2026

Service demand by tier:

Service
Demand
Price Range
Competition
Database normalization/cleanup
Medium
$30–$150/hr
Underserved
Excel chaos to Access conversion
Medium-High
$100–$5,000+
Low at enterprise level
Custom business databases
Medium (new), High (legacy)
$60–$120/hr
Saturated at low end
VBA automation
High
$20–$150/hr
Underserved at premium
Database optimization/repair
Very High
$40–$200+/hr
Highly underserved
Legacy migration
Extremely High
$2K–$50K+ fixed
Severely underserved

The positioning statement: Not "I fix Access." Position as "Legacy Systems Stabilization and Modernization Architect." Phil's GIS-integrated sewer management system for LA County Sanitation Districts is a direct reference point here — that level of experience doesn't exist in the market.
Spreadsheet Market
Excel vs. Google Sheets divide:

Excel: 90% preference for heavy analysis, enterprise, financial modeling
Google Sheets: 90% preference for collaboration, 85% of startups, 61% of small businesses, 74% of Gen Z daily users

Highest-demand services:

Service
Demand
Price Range
Competition
Formula creation/automation
Very High
$20–$150/hr
Medium
Dashboard building
Extremely High
$50–$2,000+
Medium (visual saturated, pipelines underserved)
Power Query / ETL
Extremely High
$30–$150/hr
Underserved
Macro/Apps Script
High
$50–$1,500+ per workflow
Underserved for Apps Script
Template creation
High
$30–$500+
Saturated at low end

The skill stack that commands premium rates:

Access + SQL Server + Azure DevOps → Enterprise Systems Architect
Excel + Power Query (M Language) + Power BI (DAX) → Outsourced BI Department
Google Sheets + Apps Script + Business Process Optimization → Strategic Operational Partner
Database Architecture + UI/UX Design → Full system adoption driver
Ignored Niches
Mid-market FP&A (between Excel chaos and enterprise Workday/Anaplan)
Micro-SaaS spreadsheet templates ($29–$199/month subscriptions for solopreneurs)
Regulatory and compliance tooling (EU CSRD, ESG metrics)
Physical operations and trades (HVAC, construction, chemical plants still running VBA)


7. AI User Experience and Community Feedback
Sentiment Scores (April 2026)
Tool
Positive
Negative
Key Strength
Key Problem
Claude
65%
35%
Prose quality, API efficiency
Peak-hour throttling, opaque limits
ChatGPT
40%
60%
Ecosystem, voice on CarPlay
Over-sanitized, model deprecations
Gemini
30%
70%
5TB storage bundle, NotebookLM
Hallucinations, aggressive censorship
Grok ⚠️
50%
50%
Unfiltered, X data access
CSAM generation scandal, regulatory crisis
DeepSeek 🇨🇳
80%
20%
Cost, coding, open weights
Geopolitical, enterprise blocked
Perplexity
55%
45%
Academic sourcing, citations
Becoming redundant vs. integrated search
NotebookLM
90%
10%
Zero hallucination synthesis, audio
Pricing confusion, no cross-notebook query
Copilot
25%
75%
Teams meeting summaries
Latency, "unfinished prototype" quality
The "Workslop" Problem
New term dominating professional communities: "workslop" — low-effort, unhelpful AI-generated text characterized by bloated vocabulary, endless bulleted filler, and no critical analysis. Sending workslop to colleagues permanently damages workplace relationships. Receivers view the sender as less creative, less capable, less trustworthy.
Notable Incidents (Q1–Q2 2026)
2026-02-13: ChatGPT Boycott 2026 — 1.5 million users canceled or deleted accounts after GPT-4o deprecation announced
2026-04-01: Anthropic leaked internal Claude Code file on GitHub; copyright takedowns accidentally removed 8,100+ developer repositories
2026-04-04: Check Point discovered data extraction vulnerability in ChatGPT
2026-04-04: LinkedIn BrowserGate — covert device fingerprinting exposed
Ongoing: Grok generating ~3M sexualized images (23,000 appearing to involve minors) → UK Ofcom and EU Commission investigations
Community Switching Patterns
ChatGPT → Claude (coding, creativity) or Gemini (factual, workspace)
Claude → DeepSeek locally (escaping usage caps) or Cursor (coding agents)
Perplexity → NotebookLM (users prefer owned-data synthesis over web scraping)


8. AI Training Platform Intelligence
SSDI Note (Confirmed)
2026 SGA limit confirmed: $1,690/month for non-blind SSDI recipients (source: ssa.gov/redbook/newfor2026.htm). TWP trigger: $1,210/month. AI training platforms are SSDI-compatible due to schedule autonomy and no minimum hours.
Platform Rankings (April 2026)
Platform
Status
Pay Range
Best For
Warning
DataAnnotation.tech
Active (waitlist)
$20–$60+/hr
Best overall for generalists + coders
Opaque shadow-ban system
Prolific
Active (demographic waitlist)
$8–$20/hr
Most ethical, guaranteed pay
Erratic task volume
RemoExperts (rex.zone)
Active (new, 2026)
$25–$65/hr
Seasoned writers and analysts
Early stage
Mindrift
Active
Low-medium
Beginners, fallback platform
Low earning ceiling
Outlier AI
Active ⚠️
$4.50–$50+/hr
Mid-tier generalists
Payment delays, chaotic
TELUS International
Active
$12–$15/hr
Search evaluation
"No Tasks Available" plague
Appen/CrowdGen
Technically active ⚠️
$10–$15/hr
Nobody — reputation collapsed
2+ years with zero earnings common
Clickworker/UHRS
Active ⚠️
$5–$10/hr
Dead — AI replaced the tasks
Permanent work drought
Alignerr
Active ⚠️
Advertised $80/hr (unreal)
Skip — possible data harvesting scam
"Zara" AI interview harvests your data
SME Careers
Active ⚠️
Unknown
Skip — probable phantom operation
Domain registered 75 days before launch
JoinStellar
Dead for new applicants
$25–$45/hr
Skip — waitlist hasn't moved
Technical support completely unresponsive
What's Dying vs. Thriving
Dead: Basic image tagging, sentiment analysis, bounding boxes, transcription, UHRS microtasks — AI now does all of these.

Thriving: RLHF, multi-turn evaluation, adversarial red-teaming, creative writing evaluation, advanced coding feedback. Requires actual domain expertise.
Geolocation Warning
VPN use = instant permanent ban on most platforms. Traveling outside Arizona (even to Nevada for a weekend) has triggered bans. Do not use a VPN while logged into any training platform.


9. Winning Work Intelligence
Fiverr Algorithm — What It Actually Measures
Click-Through Rate (thumbnail quality)
Dwell Time on gig page (description scannability)
Conversion consistency and velocity
Response time (under 1 hour = "Excellent boost")
Review volume and resolution speed
What's Converting — Gig Title Formulas
Formula: "I will + [specific action] + [core technology] + [business outcome]"

Examples that work:

"I will design custom AI automation workflows to scale your lead generation"
"I will build HIPAA-compliant AI agents for healthcare scheduling"
"I will build an AI automation workflow for your [specific industry] business"

Dead terms: "Prompt Engineer," "AI Enthusiast," "AI Tools"
Thumbnail Strategy
Top-performing thumbnails show before/after business impact visuals, not abstract neural network graphics. Include 2–4 bold words maximum. Professional headshot = trust signal that a human is reviewing the AI output.
Pricing Architecture
Basic ($50–$150): Single deliverable, risk-free entry, 0 revisions
Standard ($150–$500): Core offering, structured revisions, 3–5 day delivery
Premium ($500–$2,500+): Enterprise-grade, unlimited revisions, 30-day support
Upwork — The 70/30 Rule for Proposals
30% written by human (opening hook referencing a specific detail from the post, closing CTA)
70% AI-generated body (trained on your own past winning proposals)

Reply rate benchmark: Human-edited = ~24% reply rate. Pure AI copy = near zero.
The "Demo-First" Approach
Build a working prototype using Claude Code or Cursor before the client responds. Link the live demo in the proposal. "Instead of writing a long proposal, I built a prototype of what you described. You can test it here: [link]."

This approach eliminates the bidding war entirely.
Red Flags to Skip Immediately
⚠️ Job description is clearly AI-generated slop (contradictory requirements, entry-level pay)
⚠️ Client hire rate under 50%
⚠️ Requests free work or off-platform communication
⚠️ Unverified payment + brand new account
⚠️ "Fix my AI chatbot" for $5–$20 (always requires a full rebuild)
What Clients Actually Want
They don't want AI. They want outcomes. The failure they're fleeing: freelancers who paste raw LLM output. The trust signal they're buying: "human-in-the-loop guarantee" — AI does the heavy lifting, human expert reviews before delivery.


10. Skill Building Path
Excel and Power Query
Pure macro writing is effectively dead (AI generates VBA on request). Market now pays for:

Business intelligence architecture
Automated ETL pipelines
Real-time executive dashboards connected to live data

Learning path after Power Query: DAX → Power BI → Azure SQL integration. This combination positions a consultant as an outsourced BI department.
MS Access — The Legacy Migration Architect
70–83% of enterprise database migrations fail. They fail because the source database is poorly mapped, not because the destination technology is bad. An Access expert who can untangle 20 years of undocumented VBA and safely migrate to SQL Server / Azure SQL commands premium rates ($10K–$50K+ fixed projects) with virtually no competition.

Marketing language (not "I fix Access"):

"Legacy Systems Stabilization and Modernization Architect"
"AI-Ready Data Normalization and Migration Mapping"
"Emergency Data Rescue and Business Continuity"
AI Tool Skills Worth Building (Priority Order)
RAG (Retrieval-Augmented Generation) — Non-negotiable for 2026. Prevents hallucinations, grounds AI in client data. Build with Chroma (local dev), Pinecone (managed), or Supabase (PostgreSQL + vectors).
Python — Required in 76% of mid-to-senior AI job postings. API integrations, data pipelines, LangChain.
n8n — Self-hosted automation. Use it over Zapier for complex AI workflows. Run on $10/month DigitalOcean droplet with unlimited executions.
LangChain / LlamaIndex — Agent system design frameworks.
Power BI + DAX — Extends Excel/Power Query work into enterprise dashboards.
Automation Tool Comparison
Tool
Best For
Cost
Difficulty
Verdict
Zapier
Simple, client pays subscription
$$$ at scale
Low
Good for simple client setups
Make
Complex routing on budget
$10/mo Core
Medium
Middle ground
n8n
Complex AI workflows, self-hosted
$10/mo VPS
Medium-High
Best for serious work
Free Resources
Microsoft Learn: Power Query, DAX, Power BI paths (free)
Kaggle: Practice datasets (free)
TechGig RAG course: RAG certification (free)
IBM SkillsBuild Data Science: Python through ML (free)
Ollama: Run local models free on your own hardware
Workato Developer Sandbox: 1,000+ connectors free for prototyping


11. Niche Market Finder
Industries with High Demand, Low Qualified Supply
Real Estate — Highly accessible clients, strong budgets, entrepreneurial mindset. $60–$100/hour for ongoing automation. Need: CRM integration, lead triage agents, document parsing, RAG over property data.

Legal Administration — Medium difficulty to reach, premium rates justified by massive attorney hourly rates. Pain: document workflow automation, Clio integration, e-signature routing. No hallucinations allowed — use RAG over verified documents only.

Logistics and Warehousing ⚠️ BEST FIT FOR PHIL — Highest match for MS Access expertise. Countless SMEs running 1990s–2000s Access databases for inventory and order management. VBA deprecations in New Outlook are breaking email automations right now. Clients are desperate. Premium fixed-price contracts. The pool of qualified Access developers is shrinking every year.

Agriculture — Moderate difficulty. Ecologists and scientists drowning in Excel data that needs to become relational databases. GIS data, soil analysis, crop metrics all underserved.

Medical Administration ⚠️ — High pay ($100–$250/hr consulting) but intense HIPAA compliance requirements. Focus on back-office only — billing automation, coding, internal data. Never patient-facing AI.

Trades / HVAC / Construction ⚠️ — Hard to reach (not on LinkedIn), but if you can establish trust, will pay thousands for proven workflow automation. Must lead with business outcomes ("more booked jobs"), never AI jargon.
Geographic Niches
Veteran-Owned Business Angle: NVBDC certification unlocks SDVOSB set-aside contracts and access to the Billion Dollar Roundtable (32 largest US corporations mandating diverse supplier procurement). Phil qualifies. This could be a significant differentiator on Upwork for government-adjacent work.

Rural / Small Town: Grant-funded capital available (CORI has $10M+ community grants). Massive gap between DIY and $2,000/month agencies. Solo AI consultant with tools can produce 10-person agency output.
Platform Gaps (What Nobody Is Offering)
Fiverr: Zero sellers offering compliance-heavy prompt engineering (HIPAA medical, legal jurisdiction-specific)
Upwork: Complex legacy data automation with few qualified proposals despite high client demand
Rarest combination: Access/VBA expertise + Python + LLM integration = commands enterprise rates, virtually no competition


12. Self-Hosted and Free AI Tools
AnythingLLM — Current Status
Latest stable version: v1.12.0 (as of 2026-04-07). Key new features in v1.6.8:

Native XLSX file ingestion (no CSV conversion needed)
Tavily SERP connector (real-time web search for embedded agents)
LiteLLM Agent support (routes to hundreds of models)
OpenAI O1 support
DeepSeek, Fireworks, and Grok-beta connectors

Known bugs:

⚠️ GPU/CUDA transcription crashes on meeting assistant (use CPU fallback)
⚠️ Malformed Markdown uploads crash the entire service (503 error)
⚠️ Docker initialization can crash when selecting LLM provider during first run
Cloud Hosting Comparison for AnythingLLM
Provider
Cost
Setup Difficulty
Best For
Railway.app
$5–$20/mo
Very Low (1-click deploy)
Best for beginners
Render.com
$7–$25/mo
Low
Beginners, managed
DigitalOcean (2GB RAM)
$12/mo
Moderate (CLI required)
Best value/control
DigitalOcean (4GB RAM)
$24/mo
Moderate
Production stability
Fly.io
$10–$15/mo
Moderate
Low-latency routing
AWS ⚠️
$15–$20+/mo
Very High
Overkill for solo
AnythingLLM Cloud (Starter)
$50/mo
Zero
Managed, limited features
AnythingLLM Cloud (Pro)
$99/mo
Zero
Managed, 72hr SLA

Note on AnythingLLM Cloud: No local LLM included (you must supply API keys). CPU embedder crashes on large documents. No MCP integrations or custom agents.
Free Tier Summary Table
Model
Free Tier
Key Limit
API Free Tier
Claude Sonnet 4.6
Yes
Dynamic daily cap
No (min $5 to start)
Gemini 2.5 Flash
Yes
60 RPM, 1,000 req/day, 1M context
Yes (AI Studio)
GPT-5.4
Limited
~48 messages/day, degrades to lighter model
$5 credits (expire 3 months)
Perplexity
Yes
5 Pro Searches/day, unlimited basic
Yes ($5 per 1,000 ops)
NotebookLM
Yes
50 sources/notebook, 3 audio overviews/day
No public API
Groq
Yes
RPM + TPD quotas
Yes (no credit card)
Together AI ⚠️
No longer free
Minimum $5 purchase required
$5 min
Hugging Face
Yes ⚠️
Shared GPU queue, frequent timeouts
Yes (limited)
Local AI Hardware Requirements
RAM
VRAM (GPU)
Can Run
Speed
8GB system only
None
1.5B–3B CPU models
Very slow
16GB system
8GB GPU (RTX 3060/4060)
7B–13B (Q4_K_M quantized)
Good
32GB system
12GB+ GPU
13B–30B
Excellent
64GB+ system
24GB+ GPU
70B+
Production

Best sub-8B models for constrained hardware (April 2026):

Phi-4-Mini (3.8B) — best for IQ/reasoning
Gemma 3 (4B) — best for visual/multimodal
DeepSeek-R1-Distill-Qwen-1.5B — best for logic and automation testing
SmolLM3 (3B) — best for speed and text summarization

Optimal $20/month hybrid setup:

$12/month: DigitalOcean 2GB droplet (hosts AnythingLLM interface + vector DB)
$5/month: Cloudflare Workers AI (caching, routing, analytics)
$3/month: Fly.io edge routing
Local machine: Runs 4B–8B models for daily work
Free Gemini Flash or Claude Sonnet APIs for complex reasoning only


13. Pricing Comparison Tables
AI Subscriptions — Consumer Tier
Platform
Free
Entry Paid
Power User
Max
Claude
✅ Limited
$20/mo (Pro)
$100/mo (Max)
$200/mo (Max 20x)
ChatGPT
✅ Limited
$8/mo (Go)
$20/mo (Plus)
$200/mo (Pro)
Gemini
✅ Flash
$7.99/mo (AI Plus)
$19.99/mo (AI Pro)
$249.99/mo (Ultra)
Perplexity
✅ 5 Pro/day
$20/mo (Pro)
$200/mo (Max)
$325/user/mo (Ent Max)
Grok ⚠️
❌
$30/mo (SuperGrok)
$40/mo (X Premium+)
$300/mo (Heavy)
NotebookLM
✅ 50 sources
$14/mo (Plus)
$19.99/mo (Pro)
$249.99/mo (Ultra)
Mistral
✅ Le Chat
$14.99/mo (Pro)
$24.99/mo (Team)
Enterprise
Automation Platforms
Platform
Free
Paid Entry
Volumes
Zapier
100 tasks/mo
$19.99/mo
Task-based (gets expensive)
Make
1,000 ops/mo
~$10/mo Core
Operation-based
n8n (cloud)
Limited
$20/mo Starter
Execution-based
n8n (self-hosted)
Free software
$10/mo VPS
Unlimited


14. Key Takeaways for Prompt Works
Positioning Confirmation
Everything in this month's research confirms the strategy already in place. The market is desperately seeking what Phil uniquely offers:

Human expert who verifies AI output — the market is drowning in unreviewed slop. Phil's "human-in-the-loop" positioning is exactly what high-value clients will pay a premium for.

MS Access + AI = rarest combination on the platform. The research confirms Access developers are a shrinking demographic, the demand for migration and rescue is at its highest ever, and virtually nobody combines legacy Access expertise with modern AI integration skills. This is Phil's premium lead service.

Army veteran positioning — the research explicitly names veteran-owned businesses as a market with SDVOSB set-aside procurement advantages. The NVBDC certification angle is worth investigating.
Immediate Actions
Gig thumbnails: Confirm outcome-based visual style is in place (before/after business impact). Professional headshot is a trust signal — include it.
Gig descriptions: Frame problem → solution methodology → explicit deliverables → "safe choice" justification. No wall-of-text paragraphs.
Upwork proposals: Practice the 70/30 rule. Write the hook and close manually. Use AI for the body based on your own past proposals.
FAQ sections on Fiverr: Add hallucination FAQ, revision policy FAQ, "why use AI agents" FAQ. These close buyers passively 24/7.
Response time: Stay under 1 hour during business hours to maintain "Excellent" algorithmic boost.
Skills to Build (Priority Order for Phil)
Power Query → DAX → Power BI (extends existing Excel work into enterprise territory)
Google Apps Script (growing client base in startups, under-supplied)
RAG basics (Chroma locally, then Pinecone for client deployments)
n8n (self-hosted on existing ACEMAGIC PC, no subscription cost)
Income Tracking Note
SSDI SGA limit confirmed $1,690/month for 2026. TWP month trigger confirmed $1,210/month. All figures match what's in Income_Tracking.xlsx.



Report compiled by Claude | Prompt Works | April 2026 Based on 13 Gemini Deep Research files covering prompts 2.1–2.8, 2.10–2.13 Next report due: 2026-05-10
