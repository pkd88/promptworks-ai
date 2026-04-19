ref_Alternative_AI_Tools.md
Version: 1.0 | Created: 2026-03-22 | Owner: Phil Dawson / Prompt Works Purpose: Reference guide for alternative and budget AI tools — for Phil's testing and client advisory use Updated: Manually when pricing or policies change


QUICK REFERENCE — TOOL ROSTER
Tool
Origin
Cost
Best For
Data Risk
DeepSeek V3.2
China 🇨🇳
Free / Very cheap API
Bulk testing, brainstorming
HIGH — China servers
MiniMax M2.7
China 🇨🇳
$0.30/M input, $1.20/M output
Research awareness only
HIGH — China servers
ChatGPT
USA 🇺🇸
Free / $20/mo Plus
Client deliverables, general use
Low
Claude
USA 🇺🇸
Free / $20/mo Pro
Primary work tool
Low
Gemini
USA 🇺🇸
Free / paid tiers
Research, validation
Low
Perplexity / Comet
USA 🇺🇸
Free / paid
OUR research only — NO client use
Medium
Microsoft Copilot
USA 🇺🇸
Free / M365
Office integration
Low
Meta AI
USA 🇺🇸
Free
Basic tasks
Medium


DEEPSEEK — DETAILED ENTRY
What It Is
DeepSeek is a Chinese open-source AI company producing large language models that rival US models at a fraction of the cost. Current flagship: DeepSeek V3.2.
Pricing (as of March 2026)
Free web/app access: Yes — sign up at deepseek.com, no credit card required
Free API credits: 5 million tokens upon registration (no credit card)
API pricing: $0.028/M tokens (cache hit) | $0.28/M tokens (cache miss) | $0.42/M output tokens
Comparison: Up to 95% cheaper than GPT-5
Sign up: platform.deepseek.com
What DeepSeek Is Good At
Bulk prompt testing (run 100 variations for pennies)
Math and logic reasoning
Coding tasks
Brainstorming with non-sensitive content
General summarization
What DeepSeek Is NOT Good At (compared to Claude/GPT)
Content writing and tone nuance
Following complex formatting instructions
Consistency on long tasks


⚠️ DEEPSEEK DATA WARNING — READ EVERY TIME
The Privacy Policy Says (verbatim):
"Your Personal Data may be processed and stored in our servers in the People's Republic of China."
What They Collect:
Everything you type — all prompts, inputs, chat history
IP address, device ID, approximate location
Your inputs may be used to train their models (unless you opt out)
How to Opt Out of Training:
Settings → Data → Turn OFF "Improve the model for everyone"
Also Do This After Every Test Session:
Settings → Data → Delete all chats
Governing Law:
All disputes go to a court in Hangzhou, China under Chinese law.


DEEPSEEK — PROMPT WORKS USAGE RULES
Rule
Detail
✅ Allowed
Testing YOUR prompts with dummy data
✅ Allowed
Brainstorming, non-sensitive research
✅ Allowed
Bulk variation testing
❌ Never
Real client data of any kind
❌ Never
Customer PII, financials, legal docs
❌ Never
Healthcare, government, defense content
❌ Never
Prompt Works business strategy or methodology
The Dummy Data Rule
Always use realistic-looking FAKE data when testing on DeepSeek. Claude will build dummy datasets on request — same structure as real client data, zero risk.


CLIENT ADVISORY — DEEPSEEK DISCLOSURE
When recommending DeepSeek to clients as a budget option, always include this statement:

"DeepSeek is a powerful, low-cost AI option. However, their privacy policy states that data is stored on servers in China. I recommend it only for non-sensitive work — not for content containing customer data, financial information, legal documents, or anything confidential to your business."

This disclosure protects Prompt Works from liability. Say it every time, no exceptions.


MINIMAX M2.7 🇨🇳 — RESEARCH AWARENESS ENTRY
What It Is
MiniMax is a Chinese AI company. M2.7 is their flagship text model released March 18, 2026. The headline feature: it participated in its own evolution — running 100+ autonomous cycles where it analyzed its own failures, rewrote its own code, and re-evaluated itself, achieving a reported 30% performance improvement with no human involvement.
Why It's Notable
Self-improving AI loop — first major public example of a model deeply involved in its own training
Benchmarks approach Claude Opus 4.6 and GPT-5 on coding and agent tasks
3x faster than comparable US models, fraction of the cost
Also produces video (Hailuo), speech, and music — full multimodal suite
API pricing: $0.30/M input tokens, $1.20/M output tokens (very cheap)
Context window: 204,800 tokens
MiniMax Prompt Works Rules
Rule
Detail
✅ Allowed
Research awareness — know it exists
✅ Allowed
Include in monthly AI research reports
❌ Never
Recommend to clients
❌ Never
Use for any client work
❌ Never
Send real data of any kind
⚠️ DATA WARNING — Same as DeepSeek
MiniMax is a Chinese company. All data is subject to Chinese law and Chinese government access. Treat with the same caution as DeepSeek. Not for client work. Not for Prompt Works business data. Research awareness only.


PERPLEXITY — USAGE NOTE
Commercial use ban: January 23, 2026

Perplexity banned commercial use of their platform for paid tiers as of January 23, 2026.

✅ Phil can use PPX for his OWN research
❌ Never build client deliverables using PPX output
❌ Never recommend PPX to clients for business use


COMET BROWSER — PERPLEXITY'S AI BROWSER
What It Is
Comet is Perplexity's AI-powered browser built on Chromium. Phil uses it on his phone for personal browsing and Reddit. Desktop launched July 2025, Android November 2025, iOS March 18, 2026.
What It Does
AI assistant built into the browser sidebar — answers questions about the page you're reading
Summarizes articles, compares prices, synthesizes info across multiple tabs
Voice mode built in
Perplexity Deep Research integrated
Syncs research threads between phone and desktop
⚠️ IMPORTANT: Same Rules as Perplexity
Comet IS Perplexity. Same commercial use ban applies.

✅ Phil can use Comet for personal browsing and OWN research
❌ Never use Comet output for client deliverables
❌ Never recommend Comet to clients for business use
Data Note
Perplexity collects browsing and search history from Comet to build ad profiles. No opt-out available in the app. Keep client-related browsing out of Comet entirely.


TAMPERMONKEY — BROWSER SCRIPT DELIVERY
What It Is
A browser extension that runs JavaScript scripts on web pages. Used to auto-inject prompts into AI interfaces with one click.
Cross-Platform Compatibility
Platform
Tool
Status
Chrome (any OS)
Tampermonkey
✅ Best option
Firefox (any OS)
Tampermonkey or Greasemonkey
✅ Works great
Edge
Tampermonkey
✅ Works
Android (Kiwi Browser)
Tampermonkey
✅ Works well
Safari (Mac)
Userscripts app
⚠️ Limited
iPhone/iPad
None
❌ Apple blocks it
Business Opportunity
Delivering a prompt AS a Tampermonkey script is a premium upsell:

Client gets one-click prompt injection
No copy/paste required
Works on their specific workflow page
Price point: $150-300 per script
Future Fiverr gig: "I will deliver your AI prompt as a ready-to-install browser automation script"


FUTURE TOOLS TO RESEARCH
Tool
Why Watch It
Qwen (Alibaba)
Another Chinese model — similar data concerns as DeepSeek
Mistral
French open-source — EU data law compliance, interesting alternative
Llama (Meta)
Open source, can run locally — zero data risk
Local models (Ollama)
Run AI on your own machine — total privacy, great for sensitive client work


DOCUMENT MAINTENANCE
Update pricing quarterly — AI tool costs change fast
Verify DeepSeek commercial use terms before recommending to any client
Add new tools as they emerge from monthly research reports
Flag any tool with Chinese ownership with 🇨🇳 and the data warning



Version 1.1 — added MiniMax M2.7 and Comet browser entries Updated: 2026-03-26 Next review: 2026-06-01 This document belongs in the Prompt Works Claude Project and Google Drive
