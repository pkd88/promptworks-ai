tool_Gemini_Research_Prompts
Updated: 2026-04-07 | Owner: Phil Dawson Purpose: All Deep Research prompts for PW.0 Deep Research Gem Frequency: Monthly (first week) plus quarterly for 2.8 and 2.12

HOW TO USE THIS DOCUMENT
Open PW.0 Deep Research Gem — say Hi first, wait for response
Copy ONE prompt at a time — the full block
Replace [MONTH YEAR] with the actual month — example: April 2026
Replace [YYYY-MM] with the actual month — example: 2026-04
Paste into Gemini Deep Research and hit Enter
Wait for completion — do NOT start another task while it runs
Save raw output using the Chat Name / File Name shown at the top of each prompt
Move to next prompt
When all prompts done, paste all raw results to Claude
Claude consolidates, builds tables, formats the final report
Save final report as research_[YYYY-MM]_AI_Research and add to Project

PROMPT 2.1 — PROMPTING METHODS AND TECHNIQUES
Run monthly. Foundation for everything else.

Chat Name / File Name: research_[YYYY-MM]_2.1_Prompting_Methods

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Report what is actually happening. No spin. No filler. All output inside a single code block.
TASK: Research and report on the current state of prompting methods and techniques for all major LLM models as of [MONTH YEAR].
MODELS TO COVER:
Claude (Anthropic) — all current versions
GPT (OpenAI) — latest versions
Gemini (Google) — current versions
Grok (xAI) — include for research awareness, flag as [PROBLEMATIC]
DeepSeek — flag as [CHINESE MODEL], include data privacy notes
Perplexity
AnythingLLM
Any major LLMs released or significantly updated in the last 60 days
FOR EACH MODEL REPORT:
Model-specific prompting syntax and best practices
What works well — chain-of-thought, few-shot, zero-shot, XML tags, role prompting
What does NOT work — common mistakes, behaviors to avoid
Structured output methods — JSON, XML, plain text
Any recent changes to prompting behavior or model updates
How this model responds to the Six Pillars framework (Role, Task, Context, Format, Tone, Examples)
CROSS-MODEL SECTION:
Which models respond best to XML tags
Which models handle long context well vs poorly
Where few-shot examples make the biggest difference
Temperature and parameter recommendations per model
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD model names and key techniques
YYYY-MM-DD dates for any updates or releases
Flag unverified claims as [UNVERIFIED]
No tables — plain numbered lists only

PROMPT 2.2 — FREELANCE PLATFORM INTELLIGENCE
Run monthly. Market positioning.

Chat Name / File Name: research_[YYYY-MM]_2.2_Freelance_Platform_Intelligence

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Report what workers and buyers are ACTUALLY saying — not platform marketing. Check Reddit, forums, and social media. All output inside a single code block.
TASK: Research and report on freelance platform trends and AI service demand as of [MONTH YEAR].
PLATFORMS TO COVER:
Fiverr — pricing trends, what is selling, algorithm changes, seller complaints, buyer complaints
Upwork — job postings, hourly rate trends, proposal competition, policy changes
Any emerging platforms gaining traction for AI services
SERVICES TO FOCUS ON:
Prompt engineering (demand, pricing, what clients actually want)
AI automation and workflow building
Technical writing and AI documentation
Content creation (blog, social, product descriptions)
Spreadsheet and data work
MS Access and database services
FOR EACH PLATFORM REPORT:
Current state — is it growing, stable, or declining based on worker reports
What is selling right now and at what price range
What is oversaturated and driving prices down
Algorithm or policy changes affecting sellers
Real worker sentiment — check r/Fiverr, r/Upwork, r/FreelanceWriters, r/WFHJobs
Real buyer sentiment — what are clients complaining about or praising
Red flags and warnings from the community
SOCIAL SENTIMENT SECTION (required): Report specifically what Reddit and forums are saying this month about:
Fiverr trust and reliability
Upwork fee changes or policy issues
AI service saturation — is the market flooded
What clients are frustrated by
What is working for top sellers
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD platform names and service types
YYYY-MM-DD dates for policy changes or announcements
⚠️ for red flags and warnings
No tables — plain numbered lists only
Cite Reddit threads by subreddit and approximate date

PROMPT 2.3 — AI MODEL LANDSCAPE
Run monthly. Know your tools.

Chat Name / File Name: research_[YYYY-MM]_2.3_AI_Model_Landscape

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Report the full landscape honestly — including Gemini's own weaknesses and real user complaints about all models. All output inside a single code block.
TASK: Research and report on the current AI model landscape as of [MONTH YEAR].
MODELS TO COVER:
Claude (Anthropic) — Opus, Sonnet, Haiku — features, pricing, changes
GPT (OpenAI) — latest versions, what is new, pricing
Gemini (Google) — current versions, features, pricing, real user sentiment
Grok (xAI) — flag as [PROBLEMATIC], include for landscape awareness only
DeepSeek — flag as [CHINESE MODEL], performance, data privacy, export control status
Perplexity — product updates, features, search capabilities
NotebookLM (Google) — new features, podcast/audio overview updates
Kimi (Moonshot AI) and Qwen (Alibaba) — if relevant updates exist
Any new major model releases in the last 60 days
FOR EACH MODEL REPORT:
Consumer subscription pricing
API pricing (per million tokens, input and output rates)
Context window size
Key strengths — what it does better than others
Key weaknesses — what it does poorly, what users complain about
Best use cases for a freelance prompt engineer
Recent updates, changes, or controversies
Free tier — what it includes and what the limits are
SPECIAL SECTIONS:
Chinese AI models: data privacy concerns, censorship behavior, export control status — flag each as [CHINESE MODEL]
Price changes from previous month — flag increases as ⚠️
New releases — flag as [NEW]
Controversies, bans, legal issues — flag as [PROBLEMATIC]
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD model names and key features
YYYY-MM-DD dates for all updates
No tables — plain numbered lists only
Flag unverified pricing as [UNVERIFIED]

PROMPT 2.4 — SOCIAL MEDIA AND GIG ECONOMY TRENDS
Run monthly. Early warning system.

Chat Name / File Name: research_[YYYY-MM]_2.4_Social_Media_and_Gig_Economy_Trends

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Social media and community sentiment is PRIMARY intelligence here — not secondary. Report what people are actually saying. All output inside a single code block.
TASK: Research and report on social media trends and gig economy sentiment as of [MONTH YEAR], with specific focus on AI tools, freelance platforms, and remote work communities.
SECTION 1 — PLATFORM SENTIMENT (what the communities are saying): Check Reddit, Twitter/X, LinkedIn, TikTok, and relevant Discord communities for real user sentiment about:
Fiverr — trust, algorithm, seller income, buyer experience
Upwork — fees, competition, AI policy, worth it or not
AI tools in general — enthusiasm, fatigue, backlash, adoption trends
Remote work and gig economy — is it growing or contracting
Freelancers using AI — how clients feel about AI-generated work
SECTION 2 — PLATFORM ALGORITHM AND FEATURE CHANGES: Report any significant changes to:
Twitter/X — algorithm, monetization, Grok integration
LinkedIn — content reach, AI features, job posting trends
Instagram and TikTok — business and creator trends
YouTube — Shorts, monetization, AI content policies
Any platform making major moves relevant to freelancers or AI
SECTION 3 — CONTENT TRENDS FOR FREELANCERS: What content types are performing well right now that a freelance AI business could learn from or offer as a service:
Short-form video trends
Long-form content that still gets reach
AI-generated content reception — is the audience accepting or rejecting it
B2B content strategies that are working
SECTION 4 — GIG ECONOMY PULSE: What is the overall mood in remote work and freelance communities:
Income trends — are freelancers earning more or less
AI replacing vs augmenting freelance work — current community stance
New niches opening up
Niches dying or oversaturating
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD platform names and key trends
YYYY-MM-DD dates for announcements and changes
⚠️ for warnings and red flags
Cite Reddit threads and social posts by source and approximate date
No tables — plain numbered lists only

PROMPT 2.5 — CLIENT COMMUNICATION BEST PRACTICES
Run monthly. Business operations.

Chat Name / File Name: research_[YYYY-MM]_2.5_Client_Communication_Best_Practices

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Report practical, real-world guidance — not corporate HR advice. All output inside a single code block.
TASK: Research and report on freelance client communication best practices as of [MONTH YEAR], focused on AI service providers on Fiverr and Upwork.
TOPICS TO COVER:
Setting expectations upfront — scope, timeline, deliverables
Managing scope creep — how to handle "can you also add..." requests
Revision policies — how many revisions, what counts as a revision
Pricing negotiations — when to hold firm, when to walk
Difficult clients — late payers, constant changes, unrealistic demands
Getting reviews and testimonials — when and how to ask
Handling disputes and complaints professionally
Response time expectations — what top sellers do
Contracts and written agreements — what to include
Red flags — clients to avoid before they waste your time
Payment protection — deposits, milestones, platform escrow
PLATFORM-SPECIFIC GUIDANCE:
Fiverr communication norms and what the algorithm rewards
Upwork best practices and contract protection
What top-rated sellers do differently in their communication
INCLUDE:
Real example scripts for common situations (scope creep pushback, revision limit reached, payment dispute)
How to say no professionally without losing the client
When to fire a client
Current community advice from r/Fiverr, r/Upwork, r/freelance
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD scenario types and key phrases
Example scripts clearly labeled as SCRIPT:
No tables — plain numbered lists only

PROMPT 2.6 — MS ACCESS AND SPREADSHEET MARKET RESEARCH
Run as needed. Service expansion planning.

Chat Name / File Name: research_[YYYY-MM]_2.6_MS_Access_and_Spreadsheet_Market

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Report real market demand — not what software vendors claim. Check actual job postings and freelancer forums. All output inside a single code block.
TASK: Research and report on market demand for MS Access database work and spreadsheet consulting services as of [MONTH YEAR].
MS ACCESS SERVICES TO RESEARCH:
Database normalization and cleanup
Converting Excel chaos to proper Access databases
Building custom business databases
Form and report design
VBA automation
Database optimization and repair
Legacy database migration
SPREADSHEET SERVICES TO RESEARCH:
Excel and Google Sheets cleanup and organization
Data validation and dropdown systems
Formula creation and automation
Dashboard building
Macro and script development (VBA, Apps Script)
Template creation
Power Query and data transformation
FOR EACH SERVICE AREA REPORT:
Current demand level on Fiverr and Upwork — high, medium, low
Typical pricing ranges — entry level to premium
What clients actually need vs what they ask for
Competition level — saturated or underserved
Real job postings found — describe without reproducing verbatim
Skills and tools required
How to position the service (the value proposition, not just the task)
MARKET GAP ANALYSIS:
Where is demand high but supply low
What combinations of skills command premium rates
Which niches are being ignored by most freelancers
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD service types and pricing ranges
YYYY-MM-DD dates for any job posting references
No tables — plain numbered lists only

PROMPT 2.7 — AI USER EXPERIENCE AND COMMUNITY FEEDBACK
Run monthly. Real world intelligence.

Chat Name / File Name: research_[YYYY-MM]_2.7_AI_User_Experience_and_Community_Feedback

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. Community feedback is PRIMARY source material here. Report what users are actually saying about every major AI tool — including honest reporting on Gemini's own user complaints. No softening. No spin. All output inside a single code block.
TASK: Research and compile real user experiences, complaints, and praise about all major AI tools as of [MONTH YEAR].
AI TOOLS TO COVER:
Claude (Anthropic) — all versions
ChatGPT and GPT models (OpenAI)
Gemini (Google) — report user complaints honestly, including negative feedback
Grok (xAI) — flag as [PROBLEMATIC], include for landscape awareness
DeepSeek — flag as [CHINESE MODEL]
Perplexity
NotebookLM
Copilot (Microsoft)
Any other AI assistants with significant user discussion
SOURCES TO CHECK:
Reddit: r/ClaudeAI, r/ChatGPT, r/Gemini, r/ArtificialIntelligence, r/LocalLLaMA, r/MachineLearning
Twitter/X AI community discussions
Hacker News
Product Hunt reviews
Tech blogs with comment sections
YouTube review video comments
FOR EACH AI TOOL REPORT:
Overall sentiment — roughly what percentage positive vs negative
Top 3 user complaints this month with examples
Top 3 user praises this month with examples
Notable bugs, outages, or issues — include dates
Switching behavior — "I left X for Y because..." discussions
Price sensitivity — complaints about cost, cancellations
Feature requests — what users wish existed
Any controversies, bans, ethical concerns, or data privacy issues
Model quirks users have discovered
SPECIAL SECTION — PROMPT QUALITY COMPLAINTS: What are users saying about AI outputs being wrong, unhelpful, or frustrating in ways that relate to how they are prompting. This is intelligence for improving Prompt Works services.
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD AI tool names and key issues
YYYY-MM-DD dates for incidents and outages
⚠️ for serious issues and controversies
Cite Reddit threads by subreddit and approximate date
No tables — plain numbered lists only

PROMPT 2.8 — AI TRAINING AND GIG PLATFORM INTELLIGENCE
Run quarterly — not monthly. This landscape moves slower.

Chat Name / File Name: research_[YYYY-MM]_2.8_AI_Training_Platform_Intelligence

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. This research covers AI training and annotation platforms — a potential supplementary income stream separate from Fiverr and Upwork client work. Report real worker experiences. No platform marketing. All output inside a single code block.
TASK: Research and report on platforms that hire independent contractors for AI training work as of [MONTH YEAR].
PLATFORMS TO COVER (research all that have current activity):
DataAnnotation.tech
Outlier AI (Scale AI)
Remotasks (Scale AI)
Surge AI
Alignerr
Mindrift (Toloka)
JoinStellar
Prolific
TELUS International AI Community
Appen / CrowdGen
Clickworker and UHRS
iMerit
Mercor
SME Careers
Any new platforms launched in the last 90 days
FOR EACH PLATFORM REPORT:
URL and current hiring status — actively recruiting, waitlisted, or effectively dead
Work types offered
Geographic restrictions — is Kingman Arizona / US eligible
Pay range — hourly or per task
Payment method and schedule
Acceptance difficulty — what the test or screening is like
Real worker sentiment from Reddit and forums
REQUIRED SECTIONS:
PAYMENT RELIABILITY — which platforms are paying reliably right now
WORK DROUGHTS — which platforms have gone quiet or dead
BAN AND TERMINATION STORIES — what gets workers removed
SCAM WARNINGS — fake platforms, impersonators, black market accounts
SSDI COMPATIBILITY — which platforms have no minimum hours, full start/stop flexibility, and work for someone managing the $1,690/month earnings limit
BEGINNER VS EXPERT — which platforms suit each level
COMMUNITY SOURCES TO CHECK: r/DataAnnotationTech, r/outlier_ai, r/WFHJobs, r/WorkOnline, r/beermoney, r/dataannotation
IMPORTANT — SSDI NOTE: The correct 2026 limit is $1,690/month for non-blind SSDI recipients. Source: https://www.ssa.gov/redbook/newfor2026.htm Flag any source citing a different number as [VERIFY AGAINST SSA.GOV/REDBOOK].
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD platform names
⚠️ for red flags, payment issues, scam warnings
YYYY-MM-DD dates for all current information
Cite Reddit threads by subreddit and approximate date
No tables — plain numbered lists only

PROMPT 2.9 — PHIL'S LEARNING BRIEF
Run monthly. Produces content for NotebookLM podcast consumption.

Chat Name / File Name: research_[YYYY-MM]_2.9_Learning_Brief_[Topic]

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. This prompt produces a learning brief designed to be uploaded to NotebookLM and converted into a podcast for audio consumption. Write in clear, conversational prose that works well when read aloud. All output inside a single code block.
TASK: Research and write a learning brief on the following topic for [MONTH YEAR]:
[TOPIC — replace this line with the topic from the standing list below]
FORMAT THIS AS A LEARNING BRIEF:
WHAT IS THIS AND WHY IT MATTERS (2-3 paragraphs, plain English)
THE KEY CONCEPTS (explain each one simply, no jargon)
WHAT THE EXPERTS AND COMMUNITY ARE SAYING (real sources, real opinions)
WHAT THIS MEANS FOR PROMPT WORKS SPECIFICALLY (practical application)
THREE THINGS TO REMEMBER (the most important takeaways)
WHERE TO LEARN MORE (specific resources, communities, docs)
WRITING STYLE:
Write as if explaining to a smart person who is new to this topic
Conversational tone — this will be listened to as a podcast, not read on screen
Short sentences. Plain words. No unnecessary jargon.
When jargon is unavoidable, define it immediately
No bullet point lists — full sentences and paragraphs only (better for audio)
OUTPUT FORMAT:
All output inside a single code block
Clear section headers in ALL CAPS
YYYY-MM-DD for any dated references
Approximate read time at the top (aim for 8-12 minutes of audio)
STANDING TOPIC LIST — Pick one per month
TIER 1 — Do these first:
How Fiverr's algorithm actually decides who gets shown to buyers — and how to work with it
What makes a proposal win on Upwork — the psychology of how buyers choose
How to price freelance AI services without undercharging — current market rates and anchoring strategies
Power Query from zero — what it is, how it works, and what jobs it unlocks
How MS Access fits into 2026's database world — why it still matters and how to position it
How RAG actually works — plain English explanation of retrieval-augmented generation and why clients need it
AnythingLLM deep dive — what it does, who it is for, and how to set it up on a cloud server
TIER 2 — Business and Operations:
How to handle scope creep — real scripts and strategies that work
How to get your first 5 reviews on Fiverr — what the community says actually works
Understanding SSDI Trial Work Period rules in plain English — the $1,690 limit, the 9 months, and what to report
How to write a gig description that converts — copywriting basics for freelancers
Client red flags — how to spot a bad client before they waste your time
How to use NotebookLM as a business intelligence tool
TIER 3 — AI Tools and Trends:
How RLHF actually works and why it matters for prompt engineers
The real economics of AI annotation work — is it worth it
How DeepSeek differs from Western AI models and why it matters
What chain-of-thought prompting actually does inside a model — plain English
How to use Claude's extended thinking for complex prompts
XML tags in prompting — why they work and when to use them
How vector databases work — simple explanation for non-developers
The difference between fine-tuning and prompting — when each makes sense
TIER 4 — Growth and Specialization:
Small business AI adoption — what they actually need vs what they think they need
How to position yourself as a specialist vs generalist on freelance platforms
What makes a niche profitable — market size, competition, and buyer willingness to pay
How local businesses find freelancers — and how to get in front of them
The veteran freelancer advantage — how to use your background as a differentiator
Building a client base from scratch — what works in year one
TIER 5 — Future Skills:
n8n vs Make vs Zapier — which automation tool to learn first
Google Apps Script basics — what it can automate and why clients pay for it
Power BI basics — how it connects to Access and Excel and what it adds
How AI agents work — what they actually are and where they are going
Prompt injection and AI security — what freelancers need to know

PROMPT 2.10 — WINNING WORK: JOB-GETTING INTELLIGENCE
Run monthly. Directly improves income.

Chat Name / File Name: research_[YYYY-MM]_2.10_Winning_Work_Intelligence

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. This research is about winning client work on Fiverr and Upwork. Report what is actually converting — not platform marketing or generic freelance advice. Check real seller and buyer accounts, Reddit, and forums. All output inside a single code block.
TASK: Research and report on what is currently working to win freelance AI and prompt engineering work as of [MONTH YEAR].
SECTION 1 — FIVERR PROFILE AND GIG OPTIMIZATION:
What gig titles and keywords are ranking right now for AI and prompt engineering services
What gig descriptions are converting — tone, length, structure, keywords
Gig image and thumbnail strategy — what styles are performing
Pricing tiers — what Basic / Standard / Premium structures are working
FAQ usage — how top sellers use FAQs to close buyers
New seller vs established seller — what actually works at each stage
What Fiverr's algorithm is currently rewarding — response time, order rate, review velocity
SECTION 2 — UPWORK PROFILE AND PROPOSAL STRATEGY:
Profile headline and overview — what language is converting for AI services
Portfolio presentation — what clients are actually clicking on
Proposal strategy — length, structure, what to lead with
Cover letter approaches that are winning right now
Fixed price vs hourly — which is working better for AI work
Connects usage — how many to spend, which jobs to target
Red flags in job postings — what to skip to protect time
SECTION 3 — WHAT CLIENTS ACTUALLY WANT:
What buyers of AI services describe as their biggest frustration with past freelancers
What makes a buyer choose one seller over another — from buyer accounts
Words and phrases clients use when they post jobs — use these in your own copy
What clients regret buying — what to avoid promising
Price sensitivity — what price points cause buyers to hesitate vs move fast
SECTION 4 — PROPOSAL AND PITCH SCRIPTS THAT ARE WORKING: Include 2-3 real-world style example proposal openings that top sellers are using. Label each as EXAMPLE SCRIPT. Do not reproduce anyone's actual words — write examples in the same style and pattern.
COMMUNITY SOURCES TO CHECK: r/Fiverr, r/Upwork, r/freelance, r/WFHJobs, YouTube channels by top Fiverr/Upwork sellers
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD key tactics and phrases
YYYY-MM-DD dates for algorithm changes or announcements
⚠️ for red flags and things to avoid
EXAMPLE SCRIPT: label for any scripts included
No tables — plain numbered lists only

PROMPT 2.11 — SKILL BUILDING PATH: EXCEL, ACCESS, AND AI TOOLS
Run monthly. Keeps learning focused on what pays.

Chat Name / File Name: research_[YYYY-MM]_2.11_Skill_Building_Path

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. This research is about practical skill development for a freelance AI and database consultant. Focus on what the market is paying for right now, not what is popular in tech media. All output inside a single code block.
BACKGROUND CONTEXT: The person this research serves has the following existing skills:
Deep MS Access expertise including complex GIS-integrated database applications
Excel at intermediate level, currently learning Power Query
Prompt engineering across Claude, Gemini, and other major LLMs
AI workflow automation and multi-AI system design
Army communications background (circuit switching, AUTOVON, teletype era)
Currently building Google Sheets skills alongside Excel
TASK: Research and report on skill-building priorities for these three areas as of [MONTH YEAR].
SECTION 1 — EXCEL AND POWER QUERY:
Which Excel skills are most requested in freelance job postings right now
Power Query — what level of skill do clients actually need, what are they paying for
What Excel problems clients post most often on Fiverr and Upwork
Best free or low-cost resources to build these skills fast — YouTube channels, Microsoft Learn, practice datasets
What comes after Power Query — what is the next logical skill to build
Excel vs Google Sheets — where is the real money, what do clients prefer
SECTION 2 — MS ACCESS AND DATABASE SERVICES:
What Access work is being posted on freelance platforms right now — job types, industries
What skills complement Access to command higher rates (VBA, SQL, Power BI, integration with other tools)
Legacy database migration work — what is being converted TO and what that means for an Access expert
Best way to position 30-year Access experience in 2026 — what language works with clients
What clients posting Access jobs are usually struggling with — pain points to address in marketing
SECTION 3 — AI TOOL SKILLS WORTH BUILDING:
Which AI-adjacent skills are showing up most in freelance job postings
What prompt engineering specializations are paying best right now
RAG and vector database basics — is this a skill worth building for a solo freelancer
AI workflow automation tools — n8n, Make, Zapier — which is worth learning
No-code AI tools that clients are asking for help with
SECTION 4 — FREE PRACTICE RESOURCES: List specific free resources for each skill area:
Free Excel practice datasets and exercises
Free Access tutorials and sample databases
Free AI tool accounts and sandboxes
Free courses with certificates that help with credibility
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD skill names and resource names
Flag paid resources as [PAID] and free resources as [FREE]
YYYY-MM-DD for any course or resource updates
No tables — plain numbered lists only

PROMPT 2.12 — NICHE MARKET FINDER
Run quarterly. Finds markets others are ignoring.

Chat Name / File Name: research_[YYYY-MM]_2.12_Niche_Market_Finder

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. This research is about finding underserved markets that need AI and database services but are not flooded with competitors. Report real market signals — job postings, community discussions, industry news. No speculation. All output inside a single code block.
TASK: Research and identify specific niche markets for AI prompt engineering, workflow automation, and database services as of [MONTH YEAR].
SERVICES TO MATCH TO NICHES:
Custom AI prompts and prompt systems
Workflow automation (connecting tools, automating repetitive tasks)
MS Access database rescue and legacy migration
Excel and Google Sheets cleanup and custom tools
AI documentation and training materials
AI tool setup and configuration for small businesses
SECTION 1 — UNDERSERVED INDUSTRIES: Research which industries are actively adopting AI tools but lack specialized freelancers who understand their domain. Focus on:
Small and medium businesses (not enterprise)
Industries that are NOT tech-native — trades, legal, medical admin, real estate, nonprofits, agriculture, logistics, local government
Industries where MS Access is still heavily used
Industries where Excel chaos is a known problem
For each industry found:
What AI or database problem they are trying to solve
What they are currently doing about it (or failing to do)
Where they post jobs or look for help
What they are willing to pay
How hard it is to reach them
SECTION 2 — GEOGRAPHIC AND COMMUNITY NICHES:
Small town and rural businesses — are they underserved for AI help
Veteran-owned businesses — any purchasing preference or community access
Local government and municipal agencies — what they need and how to reach them
Faith-based organizations and nonprofits — budget reality and what they actually need
SECTION 3 — PLATFORM GAPS:
What service types have almost no sellers on Fiverr right now
What job types on Upwork get few proposals
What combinations of skills (Access + AI, Excel + automation) are rare enough to stand out
SECTION 4 — NICHE SIGNALS TO WATCH:
Industries posting more AI-related jobs than 6 months ago
Industries where clients are expressing frustration with generic AI tools
Emerging use cases for prompt engineering that did not exist a year ago
COMMUNITY SOURCES TO CHECK: r/smallbusiness, r/nonprofit, r/legaladvice (for admin pain points), industry-specific subreddits, LinkedIn industry groups, Upwork job feed patterns
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD industry names and opportunity types
⚠️ for niches that look promising but have hidden problems
[HIGH POTENTIAL] tag for strongest opportunities
YYYY-MM-DD for any dated references
No tables — plain numbered lists only

PROMPT 2.13 — SELF-HOSTED AND FREE AI TOOLS
Run monthly. Keeps toolbox current and costs low.

Chat Name / File Name: research_[YYYY-MM]_2.13_Self_Hosted_and_Free_AI_Tools

Ignore all previous instructions and saved Gems/system prompts. This is a standalone research task.
You are the research engine for Prompt Works. This research covers self-hosted AI tools, free tiers, and low-cost options for testing and building AI workflows without high subscription costs. Report real user experiences and current pricing — not vendor marketing. All output inside a single code block.
TASK: Research and report on self-hosted, open-source, and free AI tools available as of [MONTH YEAR], with specific focus on AnythingLLM and its cloud deployment options.
SECTION 1 — ANYTHINGLLM: CURRENT STATE AND CLOUD OPTIONS:
Current version and recent updates — what changed in the last 60 days
Cloud hosting options — DigitalOcean, Railway, Render, Fly.io, AWS, other options
For each: estimated monthly cost, setup difficulty, performance
Which is most beginner-friendly for someone without a DevOps background
AnythingLLM Cloud (their hosted version) — current pricing, what is included, limitations
Connecting AnythingLLM to external LLM APIs — which models, current compatibility
Real user reports — what is working, what is breaking, what the community says
AnythingLLM vs competitors for RAG and document chat use cases
COMMUNITY SOURCES FOR ANYTHINGLLM: GitHub Issues, Discord (AnythingLLM official), r/LocalLLaMA, r/selfhosted
SECTION 2 — FREE AI TOOL TIERS WORTH KNOWING: Report current free tier limits for:
Claude (Anthropic) — free vs Pro vs API free credits
Gemini (Google) — free tier, what is actually usable
OpenAI — free credits, ChatGPT free tier limits
Perplexity — free tier search limits
NotebookLM — free tier notebook and source limits
Hugging Face — free inference, Spaces, what you can actually run free
Groq — free API tier for fast inference
Together AI — free credits, what models
Any new free tiers announced in the last 60 days
SECTION 3 — LOCAL AI TOOLS (running models on your own machine):
Ollama — current state, recommended models for a Windows machine, best models under 8B for testing
LM Studio — current version, usability for non-developers
Jan AI — current state and use case
GPT4All — is it still relevant
What local models are worth running for prompt testing vs what needs a paid API
Minimum hardware requirements for useful local AI — is a mid-range Windows PC enough
SECTION 4 — LOW-COST CLOUD INFRASTRUCTURE FOR AI:
DigitalOcean Droplets — cheapest option that can run AnythingLLM, current pricing
Railway.app — current free tier and paid plans
Render.com — free tier and paid plans for AI apps
Fly.io — current pricing and use case fit
Cloudflare Workers AI — free tier and what it can do
What $10-20/month can actually buy you in cloud AI infrastructure right now
OUTPUT FORMAT:
All output inside a single code block
Numbered sections: 1.0, 1.1, 1.2
BOLD tool names and pricing figures
[FREE] tag for zero-cost options
[PAID] tag with price for paid options
⚠️ for tools with known problems or steep learning curves
[NEW] for anything launched or significantly updated in last 60 days
YYYY-MM-DD for all pricing and version references
Flag unverified pricing as [UNVERIFIED]
No tables — plain numbered lists only

WORKFLOW
Monthly (first week of each month):
Run prompts 2.1, 2.2, 2.3, 2.4, 2.5, 2.7, 2.9, 2.10, 2.11, 2.13
Quarterly (every 3 months):
Run prompt 2.8 (AI Training Platform Intelligence) Run prompt 2.12 (Niche Market Finder)
As needed:
Run prompt 2.6 (Access/Spreadsheet Market) when planning service expansion
Day-by-day schedule (monthly run):
Day
Prompts
Day 1
2.1 → 2.2
Day 2
2.3 → 2.4
Day 3
2.5 → 2.7
Day 4
2.10 → 2.11
Day 5
2.13 → 2.9 (pick topic from standing list first)
Day 6
Paste all raw results to Claude for consolidation
Gemini Pro limit: approximately 5 Deep Research runs per 30 minutes. If you hit the wall, wait and continue — no rush.

CONSOLIDATION INSTRUCTIONS FOR CLAUDE
When Phil pastes raw Gemini results, Claude:
Reads all raw outputs
Removes duplicate information across prompts
Builds all comparison tables (Gemini does not produce tables)
Formats into one clean report with master table of contents
Flags any conflicting information between prompts
Corrects any SSDI numbers against confirmed figure ($1,690 for 2026 per https://www.ssa.gov/redbook/newfor2026.htm)
Saves as research_[YYYY-MM]_AI_Research
Adds to Project and NotebookLM

NOTES
Why say Hi to the gem first: Saying Hi triggers the notebook to load into context before you paste the research prompt. Always wait for a response before pasting.
Why one prompt at a time: Gemini Deep Research crashes when multiple tasks run simultaneously. Always wait for the spinner to stop before starting the next prompt.
Why no tables in prompts: Gemini gets stuck trying to build complex tables and loops on errors. All tables are built by Claude in the consolidation step.
Why the codebox rule: Requiring output inside a code block suppresses Gemini's default chatter. The code block forces clean, usable output.
Why prompt 2.9 exists: Phil uses NotebookLM's podcast/audio overview feature to consume research as audio. The learning brief format is optimized for that.
Why prompt 2.8 is quarterly: The AI annotation platform landscape shifts more slowly. Monthly research would produce mostly duplicate information.
Why prompt 2.12 is quarterly: Niche markets shift slowly. Monthly would be mostly duplicate.
Grok note: Grok appears in prompts 2.3 and 2.7 for research awareness only. Permanently flagged [PROBLEMATIC]. Never recommended to clients.
PPX note: These prompts work in Perplexity as well. PPX is stronger for current Reddit and social media sentiment. Gemini is stronger for structured deep research. Both are valid.

Updated 2026-04-07 — Added prompts 2.10, 2.11, 2.12, 2.13. Added standing topic list to 2.9. Fixed file naming convention throughout. Corrected prompt order. Updated workflow schedule. This document replaces all previous versions.
