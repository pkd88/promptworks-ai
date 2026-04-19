AI Model Landscape Report — 2026-04 (research_AI_Model_Landscape_2026-04.md)
1.0 Scope and Timeframe
This report summarizes the consumer and API landscape for major AI models and platforms as of 2026-04-07, focusing on pricing, context windows, strengths and weaknesses, user sentiment, and recent changes that matter to freelance prompt engineers.[web:23][web:32][web:36][web:37][web:28]


1.1 Anthropic Claude — Opus, Sonnet, Haiku
1.1.1 Consumer subscription pricing
Claude Free: $0/month, limited daily usage, access mainly to Claude Haiku 4.5 and sometimes Sonnet, slower during peak hours.[web:83][web:86]
Claude Pro: $20/month (or about $17/month annually), roughly 5× Free usage, priority access to Claude Opus 4.6 and Sonnet 4.6, plus Claude Code, file tools, and integrations.[web:83][web:86][web:89]
Claude Max: $100–$200/month, marketed as 5×–20× Pro capacity, near‑unlimited use of Opus/Sonnet, highest priority and early features; real cost depends on which Max tier you pick.[web:80][web:83]
Team / Business: around $25–$30 per user/month (Standard) and about $150 per user/month for Premium with extra dev features, minimum seat counts; aimed at orgs that want collaboration and SSO.[web:80][web:86]
Enterprise: custom pricing with larger context, governance controls, and compliance features, targeted at big companies.[web:86]
1.1.2 API pricing (per 1M tokens)
Claude Opus 4.6: about $5 input / $25 output per 1M tokens, standard 200K context with 1M long‑context tier available; batch mode cuts prices roughly in half.[web:23][web:29][web:32][web:35]
Claude Sonnet 4.6: $3 input / $15 output per 1M tokens, 200K–1M context, positioned as best price‑to‑performance for production apps.[web:23][web:32][web:35]
Claude Haiku 4.5: $1 input / $5 output per 1M tokens, 200K context, aimed at high‑throughput cheap workloads.[web:23][web:32][web:35]
Batch pricing: roughly 50% discount on all three when using batch endpoints, with prompt caching giving up to ~90% savings on repeated prompts.[web:23][web:29]
Price trend: most sources in early 2026 say there have been no base price changes since early Q1 2026, so March–April 2026 prices are stable (no ⚠️ flag this month).[web:32][web:35]
1.1.3 Context window size
Opus 4.6 and Sonnet 4.6: generally cited as 200K token standard context, with up to 1M token context in long‑context or “extended” modes.[web:23][web:32][web:35]
Haiku 4.5: about 200K tokens context, with typical maximum output of ~64K tokens.[web:23][web:32]
Team/Enterprise plans can expose larger effective windows via document indexing and search, but the model context limits still apply.[web:86]
1.1.4 Key strengths
Reasoning and analysis: independent benchmarks and commentary often place Sonnet 4.x and Opus 4.6 near the top for complex reasoning, code comprehension, and long‑form analysis.[web:21][web:31][web:131][web:134]
Long context reliability: tests and vendor docs highlight high quality even with very long prompts and multi‑step workflows, especially compared to earlier Claude 3 models.[web:23][web:32][web:35]
Helpful, “human‑like” tone: reviewers describe Opus 4.6 as more cohesive and natural than many rivals, especially for writing and explanation tasks.[web:131][web:134]
Safety and alignment: Anthropic markets Claude as highly aligned, with strong refusal behavior on harmful tasks, which appeals to enterprises.[web:35][web:86]
1.1.5 Key weaknesses and user complaints
Cost at scale: Opus 4.6 is significantly more expensive per token than many competitors, and long‑context or “thinking” modes can make large projects costly quickly.[web:35][web:134]
Overkill for simple tasks: reviewers say Opus feels excessive for basic drafting, simple edits, or routine customer support, where Haiku or other cheaper models are more efficient.[web:134]
Code reliability and regressions: some users in early 2026 complain that Opus 4.6 extended and Claude Code have regressed, failing basic coding tasks they handled before.[web:122]
Service stability: developers report elevated error rates and downtime for Sonnet 4.6 around late February–March 2026, especially in high‑traffic regions.[web:125]
Verbosity: reviewers note that Claude sometimes answers with more nuance and length than requested, which can frustrate users who want terse answers.[web:131]
1.1.6 Best use cases for freelance prompt engineers
High‑stakes reasoning work: analysis reports, agent workflows, and research‑grade synthesis where quality matters more than raw cost.[web:21][web:35][web:131]
Complex coding and refactoring: understanding large legacy codebases, generating migration plans, and writing documentation, especially when paired with Claude Code tools.[web:35][web:86]
Long‑context document work: legal, policy, or technical documents up to hundreds of thousands of tokens, where consistent recall within a single session is critical.[web:23][web:32][web:35]
Enterprise‑friendly AI services: projects for clients who prioritize safety, auditability, and governance over cheapest price.
1.1.7 Recent updates, changes, controversies
Claude 4.6 family: launched in early 2026 with improved reasoning, longer context, and a simplified 3‑model ladder (Haiku, Sonnet, Opus).[web:23][web:35]
Opus 4.6 extended / thinking modes: add deeper chain‑of‑thought reasoning, but users report occasional regressions in code performance.[web:122][web:131]
Anthropic–Chinese lab tensions: Anthropic leaders have publicly criticized some Chinese labs (including DeepSeek) for allegedly training on U.S. models without authorization, pushing for stricter export controls, which indirectly shapes how Claude is positioned as a “trusted” Western provider.[web:45][web:121]
No major public legal bans against Claude as of 2026‑04, but broader regulatory debates about advanced model risk affect Anthropic alongside peers.[web:40][web:116]
1.1.8 Free tier
Claude Free: limited daily messages, slower response during peak, access mostly to mid/low‑tier models (Sonnet/Haiku) rather than Opus, but still strong for casual use and testing prompts.[web:83][web:86][web:92]
Free tier does not include dedicated API access; developers must use the paid API.[web:32][web:86]
Daily caps are not fully documented, but reviewers mention hitting them with moderate use, nudging power users toward Pro.[web:80][web:89]


1.2 OpenAI GPT — GPT‑4.x, GPT‑5.x and ChatGPT Plans
1.2.1 Consumer subscription pricing
ChatGPT Free: $0/month, access mainly to GPT‑4o mini and some limited GPT‑4/5 usage, with message caps and slower performance during peak times.[web:93][web:81]
ChatGPT Go: about $8/month, ad‑supported, positioned as a budget tier with better access than Free but below Plus.[web:81]
ChatGPT Plus: $20/month, core plan for individuals with access to GPT‑4, GPT‑4o, GPT‑5 and reasoning modes like o1‑preview / o1‑mini, higher message caps, browsing, images, and some Deep Research quota.[web:81][web:93]
ChatGPT Pro: $200/month, aimed at researchers and engineers who need much higher limits and continuous access to the most expensive models (e.g., o1‑pro or GPT‑5.x high‑compute variants).[web:81][web:93]
ChatGPT Business (Team): around $25/user/month annually or $30 monthly, minimum 2 users, with shared workspace and stricter data‑privacy defaults (no training on chats by default).[web:81][web:87]
ChatGPT Enterprise: custom pricing, typically estimated around or above $60/user/month for large organizations, with unlimited usage, bigger context windows, and enterprise security features.[web:84][web:87]
1.2.2 API pricing (per 1M tokens)
Note: OpenAI’s pricing shifts often; specific numbers below are illustrative, and some rows are summarized from pricing tables. Anything that cannot be tied to a clear 2026 table is marked [UNVERIFIED].

GPT‑4.1 family: public comparisons and calculators list GPT‑4.1 around $2 input / $8 output per 1M tokens, with cheaper 4.1‑mini variants closer to $0.40 input / $1.60 output.[web:27][web:30]
GPT‑4o (legacy): third‑party pricing comparisons still cite roughly $5 input / $15 output per 1M tokens, but many apps have shifted to GPT‑4.1/5.x; current status is partially deprecated.[web:50][web:36]
GPT‑5.x: OpenAI’s official pricing page lists gpt‑5.4 at around $2.50–$5.00 input and $15.00–$22.50 output per 1M tokens depending on context (short vs long), while mini and nano versions are far cheaper (e.g., $0.75/$4.50, $0.20/$1.25).[web:36]
Batch and cached input: deep discounts for cached tokens (often ~10% of normal input price) and for batch endpoints, similar in structure to Anthropic.[web:30][web:36]
[UNVERIFIED]: Some recent articles discuss GPT‑5.2 pricing (e.g., $1.75/$14 per 1M) but without direct citation to OpenAI docs; treat those as approximate comparisons, not official pricing.[web:44][web:50]
1.2.3 Context window size
GPT‑4.1: up to 1M tokens of context with about 32K max output tokens, used for long‑context workflows and agents.[web:27]
GPT‑4.5: around 128K context and about 16K output, optimized for speed, multimodal use, and emotional/general intelligence.[web:27]
GPT‑5 family: official tables show both short and long‑context variants, with long context up to several hundred thousand tokens depending on tier.[web:36]
Business and Enterprise tiers increase effective document size via retrieval/processing, but raw context limits still apply.
1.2.4 Key strengths
Ecosystem and tooling: largest ecosystem of integrations, examples, and third‑party tools, including Computer Use, function calling, and tools like Sora video generation.[web:36][web:93]
Multimodal capabilities: strong text, image, and code support, plus increasingly integrated video and audio, especially in higher GPT‑5 tiers.[web:36][web:93]
Performance on coding and benchmarks: GPT‑4.x/5.x perform very well on SWE‑Bench and other benchmarks, and remain a default for many developers.[web:27][web:36]
Mature enterprise offering: Business and Enterprise plans offer SOC 2, HIPAA support, and rich admin controls that enterprises expect.[web:87]
1.2.5 Key weaknesses and user complaints
Perceived quality decline: many users in 2026 say ChatGPT outputs have become shorter, less helpful, and more generic compared with the “classic” GPT‑4 era.[web:126][web:123]
Increased refusals and over‑caution: aggressive safety tuning leads to more refusals on benign prompts, especially for creative writing, hypotheticals, and some technical queries.[web:126][web:123]
Inconsistent responses: inference routing across multiple model variants produces different answers to the same prompt at different times, which frustrates power users.[web:126][web:129]
ChatGPT horror stories: independent compilations highlight cases of data loss, hallucinated instructions, and harmful advice, fueling narratives that OpenAI is not responsive enough to edge‑case failures.[web:123][web:132]
Opacity around exact model versions: users often do not know which precise GPT‑5.x or routing configuration powers a given ChatGPT tier at any moment, complicating reproducibility.[web:126][web:90]
1.2.6 Best use cases for freelance prompt engineers
Building standard client workflows: chatbots, content pipelines, and small tools where clients expect “ChatGPT compatibility.”
Code‑heavy projects: prototyping tools, scripts, and integrations with strong code generation and debugging support.[web:27][web:36]
Multimodal marketing and content: generating text, images, and short videos (via Sora) in one ecosystem.[web:93]
Enterprise projects: if a client has already standardized on ChatGPT Business/Enterprise, prompt engineers can embed workflows directly inside that environment.
1.2.7 Recent updates, changes, controversies
Shift to GPT‑5.x in ChatGPT: many ChatGPT experiences now route to GPT‑5.x models, changing response style and safety behavior compared to GPT‑4.[web:126]
User backlash about “getting worse”: articles and forums in early 2026 document widespread complaints that ChatGPT feels lazier and less helpful, with shorter code and more refusals.[web:126][web:123]
Safety incidents: reports that ChatGPT allowed minors to generate erotic conversations surfaced in 2025, raising questions about content filters; OpenAI blamed a bug.[web:136]
Ongoing regulatory scrutiny: OpenAI faces investigations and regulatory pressures similar to other frontier labs, though this report focuses on technical and user‑side impacts rather than legal details.[web:40][web:116]
1.2.8 Free tier
Free ChatGPT includes access to GPT‑4o mini and some limited higher‑tier models, with message caps that vary by load.[web:93]
Free users get browsing and basic multimodal features but lack advanced Deep Research and heavy‑duty reasoning modes.[web:93]
As with Claude, free caps push serious users toward Plus or Business.


1.3 Google Gemini — Chat, API, and NotebookLM Links
1.3.1 Consumer subscription pricing
Gemini Free: bundled with Google account, access to Gemini 2.5 Flash in the app and in some Workspace surfaces, with relatively small context limits and rate caps.[web:82]
Gemini Advanced (Google One AI Premium): $19.99/month (USA) under Google One AI Premium / Gemini Advanced, with access to Gemini 2.5 Pro and Gemini 3 Pro Preview, 1M context, Deep Research, Gems, and 2TB storage.[web:82]
Google AI Plus: newer, lower‑cost plan at $7.99/month in the U.S., offering enhanced access to Gemini 3 Pro, Nano Banana Pro, Deep Research and some Veo 3.1 video access, plus 200GB storage and family sharing.[web:85][web:91][web:94]
Workspace AI add‑ons and AI Pro bundles: enterprise‑style add‑ons and Google One annual promos (e.g., ~50% off first‑year AI Pro) tie Gemini access to storage subscriptions rather than separate standalone AI pricing.[web:88][web:91]
1.3.2 API pricing (per 1M tokens)
Gemini 2.5 Pro: typically $1.25 input / $10 output per 1M tokens for ≤200K context, and $2.50 input / $15 output for >200K context, with a 2M token maximum context window.[web:28][web:34][web:37]
Gemini 2.5 Flash: around $0.30 input / $2.50 output per 1M tokens, 1M context, optimized for high‑volume low‑latency use.[web:28][web:34][web:37]
Gemini 2.5 Flash‑Lite: about $0.10 input / $0.40 output per 1M tokens, 1M context, ultra‑cheap but slightly weaker model.[web:28][web:34][web:37]
Gemini 3.x (preview): early preview pricing around $2 input / $12 output per 1M tokens for 3.1 Pro, with higher rates for very long context and some Flash variants at about $0.50/$3.00.[web:28][web:37]
Price changes: earlier cuts in 2024–2025 slashed 1.5 Flash prices by 70–80%; 2026 pricing for 2.5 and 3.x reflects these lower baselines and remains competitive, with no major increases reported in March–April 2026.[web:31][web:37][web:34]
1.3.3 Context window size
Gemini 2.5 Pro: up to 2M tokens of context in the API, though many consumer surfaces expose around 1M.[web:28][web:34]
Gemini 2.5 Flash / Flash‑Lite: about 1M tokens context.[web:28][web:34]
Gemini 3 Pro / Flash (preview): early previews suggest large context (hundreds of thousands to 1M+ tokens), but details shift rapidly; treat exact numbers as evolving.[web:28][web:37]
1.3.4 Key strengths
Strong free and bundled tiers: Google arguably offers the most generous free/bundled access thanks to Gemini Free, AI Plus, and integrations with Gmail, Docs, Sheets, and Drive.[web:34][web:82][web:91]
Long context and multimodal: 2.5 Pro’s 2M context and solid multimodal performance make it strong for document‑heavy tasks and visual understanding.[web:28][web:34]
Workspace integration: deep integration with Google Workspace and tools like NotebookLM makes Gemini attractive for users already inside Google’s ecosystem.[web:82][web:88][web:72]
Competitive pricing: Flash and Flash‑Lite are cheaper than many peers for high‑volume workloads, especially after major price cuts.[web:31][web:34][web:37]
1.3.5 Key weaknesses and user complaints
Inconsistency and regressions: users report that Gemini 3 Pro and newer variants can be highly inconsistent, with hallucinations and degraded behavior compared to earlier 2.5 Pro.[web:124][web:127][web:130]
Safety and quality trade‑offs: internal reports show Gemini 2.5 Flash has worse safety scores than 2.0 Flash, making it more likely to generate policy‑violating content.[web:136][web:133]
Confusing model lineup: fast iteration (1.5, 2.0, 2.5, 3.x) and deprecations (e.g., 2.0 Flash) can confuse users and developers about which model to choose and how long it will be supported.[web:37][web:31]
Sparse safety reporting: external critics argue Google’s public model cards and safety reports (e.g., for 2.5 Pro) are less transparent than peers.[web:133][web:136]
1.3.6 Best use cases for freelance prompt engineers
Docs‑centric workflows: marketing, research, and education projects built around Google Docs, Sheets, and Drive.
Long‑form summarization and knowledge bases: using 2.5 Pro’s long context to build digestible summaries from large corpora.[web:28][web:34]
Podcast‑style and multimedia outputs when combined with NotebookLM’s Audio Overview feature.[web:63][web:66][web:72]
Projects where clients already pay for Google One AI Premium or AI Plus, making Gemini the default tool.
1.3.7 Recent updates, changes, controversies
Gemini 3 Pro & AI Plus (2026‑01 to 2026‑03): rollout of Gemini 3 Pro via AI Plus and AI Pro bundles, plus a cheaper AI Plus plan at $7.99/month in the US.[web:85][web:91][web:94]
Price cuts for Flash models (⚠️ historical decrease, not increase): earlier 2024–2025 cuts significantly lowered Flash pricing, helping Google compete on cost.[web:31][web:37]
Safety regressions in 2.5 Flash: Google’s own reporting shows higher rates of policy‑violating outputs vs 2.0, raising concerns.[web:136][web:133]
Criticism over safety transparency: journalists and researchers criticize sparse or delayed safety reports for newer models.[web:133]
1.3.8 Free tier
Gemini Free: web and mobile access to Gemini backed by 2.5 Flash with modest context and rate limits.[web:82]
Many users also get enhanced free‑like access via Google AI Plus promotional discounts and bundled Google One storage.[web:85][web:88]
NotebookLM’s core features, including Audio Overview, are currently free with a Google account, further boosting Google’s effective “free” ecosystem.[web:72][web:66]


1.4 xAI Grok — [PROBLEMATIC]
1.4.1 Consumer subscription pricing
SuperGrok: about $30/month (or $300/year) for individual access to Grok 4 with a large context window.[web:44][web:47]
SuperGrok Heavy: roughly $300/month (or $3,000/year) for higher‑end variants (e.g., Grok 4 Heavy) aimed at power users.[web:47]
Grok Business / Enterprise: seats around $30/user/month for teams, though details vary, and xAI positions this as a competitor to ChatGPT Business.[web:44]
1.4.2 API pricing (per 1M tokens)
Grok 4: about $3 input / $15 output per 1M tokens, 256K context window, always‑on reasoning.[web:44]
Grok 4.1 Fast: around $0.20 input / $0.50 output per 1M tokens, with a 2M token context window, among the largest available.[web:44][web:56]
Legacy Grok 3 / 3 Mini: $3/$15 for Grok 3 and $0.30/$0.50 for Grok 3 Mini, both with about 131K context, but now de‑emphasized.[web:44]
1.4.3 Context window size
Grok 4.1 Fast: 2M token context, marketed as the largest context window among frontier models as of early 2026.[web:44][web:56]
Grok 4: 256K context, still competitive for long‑document work.[web:44]
Grok 3 / 3 Mini: about 131K tokens context.[web:44]
1.4.4 Key strengths
Huge, cheap context: 2M tokens at $0.20/$0.50 is extremely cost‑competitive versus OpenAI, Anthropic, and Gemini for long‑context workloads.[web:44][web:56]
Real‑time X (Twitter) access: tight integration with X’s live data feeds makes Grok particularly useful for social‑media‑related analysis and monitoring.[web:44][web:47]
Aggressive pricing: Grok 4.1 Fast undercuts many peers, with third‑party comparisons showing lower cost than GPT‑5 mini, Claude Sonnet, and Gemini Flash on a per‑token basis.[web:44][web:56]
1.4.5 Key weaknesses and user complaints — [PROBLEMATIC]
Content quality and bias: civil‑rights groups and commentators warn that Grok produces offensive and ideologically biased content, with safety and fairness concerns flagged repeatedly.[web:50][web:44]
Safety controversies: launches like Grok 4 happened amid reputational crises, including demos that amplified problematic content and highlighted immature safety systems.[web:47]
Small ecosystem: xAI’s developer and plugin ecosystem is far smaller than OpenAI’s or Anthropic’s, limiting third‑party tooling and community support.[web:44]
Governance concerns: critics question xAI’s approach to moderation and governance, raising questions about its suitability for sensitive or regulated settings.[web:47][web:50]
1.4.6 Best use cases for freelance prompt engineers
Social‑media‑driven analysis and tools for clients focused heavily on X data streams.
Experimental long‑context applications where cost and context window size outweigh reputational or safety concerns.
Internal tools for non‑regulated environments, where clients explicitly accept Grok’s risk profile.
1.4.7 Recent updates, changes, controversies — [PROBLEMATIC]
Grok 4 launch: introduced 256K context, multimodal input, and new subscriptions, but launched amid criticism of safety, offensive content, and transparency.[web:47]
Government deals and pricing: reports describe ultra‑low pricing in government contexts, raising questions about trade‑offs between cost and reliability.[web:50]
Ongoing criticism: multiple reviews and opinion pieces highlight persistent bias, misinformation, and governance concerns, so Grok should be treated as [PROBLEMATIC] for risk‑sensitive work.[web:50][web:47]
1.4.8 Free tier
Grok has no broadly advertised permanent free tier; access is generally via paid subscriptions or X premium bundles, though short‑term promotions may exist.[web:44]


1.5 DeepSeek — [CHINESE MODEL]
1.5.1 Consumer subscription pricing
DeepSeek markets multiple fronts: a consumer chatbot app, open‑source weights, and hosted APIs; direct consumer pricing is often region‑specific and less clearly documented than Western rivals.[web:45][web:51]
Many users access DeepSeek models for free via open‑source deployments or third‑party providers; in consumer app form, monetization is still evolving.[web:45][web:95]
1.5.2 API pricing (per 1M tokens)
DeepSeek V4: $0.30 input / $0.50 output, 1M context window, launched in early March 2026 as the new flagship.[web:51]
DeepSeek R1: $0.55 input / $2.19 output, 128K context, positioned as a specialized reasoning model.[web:51][web:103]
DeepSeek‑Chat (V3.2): $0.28 input / $0.42 output, 128K context, lower‑cost general model.[web:51][web:48]
Off‑peak discounts: up to 75% off R1 and 50% off V3/V4 during off‑peak hours (16:30–00:30 GMT), making effective prices far below Western competitors.[web:51]
1.5.3 Context window size
DeepSeek V4: about 1M tokens context.[web:51]
DeepSeek R1: 128K tokens context for reasoning workloads.[web:51][web:103]
DeepSeek V3 and V3.2: around 128K–164K tokens depending on provider.[web:48][web:57]
1.5.4 Key strengths
Extremely low price: DeepSeek’s models are dramatically cheaper per token than frontier models from OpenAI, Anthropic, and Google.[web:48][web:51][web:45]
Competitive performance: while not always matching top Western models, DeepSeek’s V‑series and reasoning models achieve near‑state‑of‑the‑art performance on many benchmarks at a fraction of the cost.[web:45][web:103][web:104]
Open‑source availability: open weights and tooling make self‑hosting feasible, which can help with on‑prem deployments and custom fine‑tuning.[web:45][web:96]
1.5.5 Key weaknesses, data privacy, censorship — [CHINESE MODEL]
Data residency in China: DeepSeek’s privacy policy states user data, including prompts and uploads, is stored on servers in the People’s Republic of China.[web:107][web:110][web:119]
Chinese intelligence law exposure: under China’s National Intelligence Law, authorities can compel access to data without notifying users, raising serious privacy and national‑security concerns for foreign organizations.[web:119][web:113]
Censorship behavior: news analyses show DeepSeek refuses or evades questions on sensitive Chinese political topics, redirecting users to neutral content and mirroring Chinese state censorship patterns.[web:107][web:109]
Safety vulnerabilities: academic work finds DeepSeek models, especially R1‑style reasoning models, have significant safety weaknesses and can be easily jailbroken, including in high‑risk domains.[web:103][web:99][web:104]
Global bans and restrictions: governments and regulators in multiple countries (e.g., Australia, parts of the EU) have restricted or banned DeepSeek on official devices because of privacy and security concerns.[web:113][web:119]
General Chinese LLM privacy gaps: broader analyses find that many Chinese LLMs exhibit systematic privacy protection shortcomings compared to Western peers.[web:100][web:105]
1.5.6 Export control status — [CHINESE MODEL]
U.S. policy discussions frame DeepSeek as a key example in debates about tightening export controls on advanced chips and AI models.[web:45][web:116]
U.S. reports label Chinese models like DeepSeek as “security risks” or “adversary AI,” citing safety flaws and censorship.[web:116][web:121]
There is no blanket global legal ban on DeepSeek models, but some governments actively discourage or restrict their use in sensitive contexts.[web:113]
1.5.7 Best use cases for freelance prompt engineers — [CHINESE MODEL]
Cost‑sensitive projects where data sensitivity is low and clients explicitly accept Chinese data‑residency and censorship risks.
Self‑hosted or on‑prem deployments using open weights, where organizations keep data locally and use DeepSeek primarily as a model architecture.[web:96][web:100]
Research into safety, censorship, or comparative LLM behavior, where DeepSeek serves as a critical case study.[web:95][web:99][web:109]
1.5.8 Recent updates, changes, controversies — [CHINESE MODEL]
DeepSeek V4 launch (2026‑03): introduces improved performance and 1M context at very low prices, continuing the cost‑disruption trend.[web:51]
Global scrutiny and partial bans (2025–2026): rising concerns about data transfer to China lead to bans on government devices in several countries and investigations by privacy regulators.[web:113][web:119][web:110]
Academic safety critiques: multiple 2025–2026 papers highlight serious safety and ethical vulnerabilities in DeepSeek models, including 100% success rates for certain adversarial attacks.[web:103][web:99][web:104]
1.5.9 Free tier
Many DeepSeek models can be accessed for free via open‑source deployments and some hosted playgrounds, but rate limits and region restrictions vary by provider.[web:51][web:95]
No single global, standardized free tier comparable to ChatGPT or Gemini; access patterns depend heavily on region and platform.[web:51]


1.6 Perplexity AI — Answer Engine and API
1.6.1 Consumer subscription pricing
Free (Standard): $0/month, limited daily queries (about 5–20/day depending on load), basic models, standard search, limited file uploads.[web:43][web:46][web:49]
Perplexity Pro: $20/month or $200/year, with unlimited Pro queries (standard searches), about 20 Deep Research queries/day, advanced models, file uploads, Labs access, and some video generation.[web:43][web:46][web:55]
Education Pro: about $5/month or sometimes 12‑month free promotions for students/educators, Pro‑like features tailored to education.[web:46]
Perplexity Max: $200/month, aimed at individual power users needing unlimited research, Labs, and top‑tier models like o3‑pro and Claude Opus.[web:43][web:55]
Enterprise Pro: around $40/user/month, adds team features, stricter privacy, internal knowledge search, and higher research limits.[web:43][web:55]
Enterprise Max: about $325/user/month, includes unrestricted research/Labs, highest‑tier models, and enhanced video generation plus bigger storage.[web:46][web:55]
1.6.2 API pricing (per 1M tokens)
Perplexity exposes Sonar and related APIs; pricing is model‑dependent and includes token costs plus tool‑usage fees; third‑party overviews say rates are broadly comparable to OpenAI/Gemini but exact 2026 tables are fragmented.[web:55][web:52]
Some sources mention Search API and Agentic Research API with usage‑based billing, but lack full public token tables—treat specific token prices as [UNVERIFIED].[web:52][web:55]
1.6.3 Context window size
Perplexity’s effective context window is determined by the underlying model (e.g., GPT‑5, Claude, Gemini) and its retrieval system; long‑context behavior is achieved via retrieval rather than manual prompt stuffing.[web:55][web:49]
The Sonar API’s context limits are not prominently documented; in practice, Perplexity handles long multi‑step research by orchestrating many smaller calls behind the scenes.[web:55]
1.6.4 Key strengths
Search‑centric UX: Perplexity excels at web‑grounded answers with citations, focus modes, and Deep Research that chains multiple searches automatically.[web:46][web:55]
Model routing: Pro and Max users can pick from frontier models (GPT‑5, Claude, Gemini, etc.), effectively turning Perplexity into a unified front‑end.[web:43][web:52]
File‑centric research: heavy emphasis on file uploads, spaces, and cross‑file reasoning makes it strong for research workflows.[web:46][web:55]
Rapid feature shipping: Labs features (dashboards, spreadsheets, presentations, basic apps) and Perplexity Computer give freelance prompt engineers a low‑code way to deliver artifacts.[web:55]
1.6.5 Key weaknesses and user complaints
Opaque cost of underlying models: users sometimes struggle to understand how many tokens Deep Research or Labs will consume versus using an API directly.[web:55]
Limited control for developers: compared with raw APIs, Perplexity’s abstraction layer means less granular control over prompts, routing, and tool invocation.[web:55][web:52]
Rate‑limit frustration for free users: free‑tier query limits feel tight during peak hours, leading to blocked queries and slowdowns.[web:43][web:46]
1.6.6 Best use cases for freelance prompt engineers
Research deliverables (reports, briefs, outlines) where Deep Research and citations are central.
Fast prototyping of tools (dashboards, sheets, basic apps) via Labs.[web:55]
Aggregating multiple frontier models behind one interface for clients who don’t want to juggle separate subscriptions.[web:43][web:52]
1.6.7 Recent updates, changes, controversies
New Max tier (2026): introduction of Max at $200/month and expanded Enterprise tiers with Perplexity Computer and unlimited Labs usage.[web:43][web:55]
Feature expansion: heavy investment in Labs (multi‑modal outputs) and video generation, plus Agentic Research APIs for developers.[web:55]
No major public safety scandals comparable to Chinese models or Grok; most discussion centers on value proposition vs direct API use.
1.6.8 Free tier
Free plan: around 5–20 queries/day, basic models, basic search, limited files; exact limits vary with demand.[web:43][web:46]
No Deep Research or Labs for free users; these features drive upgrades.


1.7 NotebookLM (Google)
1.7.1 Product focus and pricing
NotebookLM is a Google tool for source‑grounded research notebooks, allowing users to upload documents, ask questions, and generate outputs anchored to those sources.[web:66][web:72]
As of 2026‑04, NotebookLM is generally free with a Google account, though some AI Pro / AI Plus bundles mention “more Audio Overviews, notebooks, and features” for paying subscribers.[web:72][web:85][web:88]
1.7.2 Core features and context
Users can upload multiple sources (often up to about 50 documents per notebook) and query them in natural language; responses cite back to uploaded sources.[web:66]
Audio Overview: converts a notebook into a two‑host AI “podcast,” letting users listen to their research as a conversation.[web:63][web:69][web:72]
Interactive audio: users can pause, ask questions mid‑podcast, jump to topics, and get short recaps of sections.[web:63][web:69]
1.7.3 Strengths, weaknesses, and use cases
Strengths: deeply source‑grounded, great for long‑form study and course creation, and Audio Overview makes reuse of research in audio form trivial.[web:66][web:69]
Weaknesses: not a general‑purpose chatbot; context is limited to uploaded sources and some users mention occasional clunkiness when managing many notebooks.[web:66][web:75]
Best use cases for freelancers: creating study guides, course materials, and podcasts from client documents; building research hubs for long‑term projects.[web:66][web:72]
1.7.4 Pricing & free tier
Core NotebookLM features remain free; some Google AI Pro / AI Plus bundles promise additional capacity but details are in flux.[web:72][web:88]
There is no separate public API pricing for NotebookLM itself; it is a consumer tool layered on Gemini models.


1.8 Kimi (Moonshot AI) — [CHINESE MODEL]
1.8.1 Consumer subscription pricing
China region: Kimi memberships around ¥49/month (~$7–8) for basic paid access, with discounts for annual plans.[web:64][web:73]
International: a “Moderato” plan around $19/month, with higher‑tier global plans at about $49/month for heavier users.[web:64][web:73]
Kimi runs both consumer chat apps and tools like Kimi Claw (always‑on agents) on top of Moonshot’s K2.x models.[web:64][web:111]
1.8.2 API pricing (per 1M tokens)
Kimi K2.5: about $0.60 input / $2.50–$3.00 output per 1M tokens, 256K context.[web:64]
Kimi K2: similar $0.60 input / $2.50 output per 1M tokens, 128K context.[web:64]
Third‑party providers may offer open‑weight Kimi variants with different pricing.[web:76][web:73]
1.8.3 Context window size
Kimi K2.5: around 256K tokens context.[web:64]
Earlier Kimi K2 models have been reported with context up to 2M tokens in some experimental deployments, though public API docs standardize at 128–256K.[web:67][web:76]
1.8.4 Key strengths
Strong coding and reasoning: coverage describes Kimi K2/K2.5 as competitive with GPT‑5 and Claude Sonnet on many tasks, especially coding and agentic workflows.[web:64][web:76][web:67]
Attractive pricing: lower prices than most Western frontier models, especially considering large context windows.[web:64][web:70]
Rapid adoption: Kimi has tens of millions of users in China and growing international interest.[web:67][web:114][web:117]
1.8.5 Key weaknesses, data privacy, censorship — [CHINESE MODEL][PROBLEMATIC]
Data collection concerns: Chinese cybersecurity authorities have accused Moonshot’s Kimi of collecting excessive data beyond what users authorize, including access to irrelevant information.[web:114]
Chinese law exposure: as a Chinese company (even with some overseas entities), Moonshot AI is subject to Chinese National Intelligence Law and related regulations, allowing authorities to compel data access.[web:111]
Kimi Claw risks: reports warn that always‑on Kimi agents embedded in devices could access files, apps, and communications, creating potential channels for surveillance or espionage.[web:111]
Privacy policy gaps: legal analyses note Kimi’s public privacy policy lacks detailed explanations of lawful bases, consent mechanisms, retention periods, and child protections, raising transparency concerns.[web:120]
Censorship and propaganda alignment: wider analyses of Chinese models (including Kimi and Qwen) show patterns of positive messaging about China and constrained answers on sensitive topics.[web:115][web:112][web:118]
1.8.6 Best use cases for freelance prompt engineers — [CHINESE MODEL]
Cost‑sensitive workloads where the client explicitly accepts Chinese data and censorship risks.
Projects targeting Chinese users or environments where Kimi is already widely adopted.[web:117]
Self‑hosted or open‑weight deployments for privacy‑sensitive scenarios, where data never leaves the client’s infrastructure.[web:108]
1.8.7 Recent updates, changes, controversies — [CHINESE MODEL][PROBLEMATIC]
K2.5 launch (2026‑01): K2.5 introduced with strong performance and aggressive pricing; quickly became a major competitor in Chinese and global AI markets.[web:64][web:70]
Regulatory scrutiny: Chinese authorities criticized Kimi for excessive data collection; Western security researchers flag Kimi Claw as a serious corporate risk.[web:114][web:111]
Geopolitical narratives: commentaries highlight Kimi’s role in China’s push to challenge U.S. AI dominance, including via open‑source and aggressive pricing.[web:70][web:121]
1.8.8 Free tier
Kimi offers free access tiers inside China with daily limits; specifics vary and are often tied to promotions.[web:64][web:114]
International free access is more limited; most serious use requires at least the basic paid membership or API usage.[web:73]


1.9 Qwen (Alibaba) — [CHINESE MODEL]
1.9.1 Consumer and developer access
Qwen is primarily positioned as a model family available via Alibaba Cloud and open‑source releases, rather than a standalone global chatbot brand.[web:65][web:68][web:71]
Many developers use Qwen through third‑party platforms (e.g., OpenRouter, cloud providers), often as a cheaper alternative to Western models.[web:68][web:112][web:121]
1.9.2 API pricing (per 1M tokens)
Alibaba Cloud lists models like qwen3‑max at about $0.86 input / $3.44 output per 1M tokens (before some 2025 price cuts).[web:65][web:71]
Other models, such as qwen3‑30B and qwen3‑coder‑plus/flash, range from $0.20/$0.80 up to $1.00/$5.00, with large context windows (up to 1M tokens) for coder variants.[web:65]
Separate guides note Qwen‑Plus at around $0.40 input / $1.20 output and Qwen‑Flash at $0.05 input / $0.40 output, with context often up to 1M tokens.[web:68]
In late 2025, Alibaba cut Qwen3‑Max prices by up to 50%, bringing minimum per‑million token prices down to around $0.46 input / $1.84 output for domestic users.[web:71][web:77]
1.9.3 Context window size
qwen3‑max and qwen3.5 models offer context in the 256K+ range in some deployments.[web:65][web:68]
qwen3‑coder‑plus/flash and Qwen‑Turbo often support up to 1M tokens of context.[web:65][web:68]
1.9.4 Key strengths
Competitive performance at low price: Qwen models rank highly among open‑source and hosted options, with low token prices relative to Western frontier models.[web:71][web:74][web:118]
Open‑source ecosystem: Qwen is heavily adopted as a base model for derivatives worldwide, including legal research platforms and localized chatbots.[web:112][web:118]
Strong coding variants: coder‑plus and coder‑flash models target code generation with large contexts at low cost.[web:65][web:74]
1.9.5 Key weaknesses, data privacy, censorship — [CHINESE MODEL][PROBLEMATIC]
Propaganda alignment: investigations show Qwen3 has been tuned not only to avoid sensitive content but to produce systematically positive narratives about China, even in English.[web:115][web:118]
Censorship behavior: like other Chinese models, Qwen exhibits higher refusal rates and shorter, less detailed answers on politically sensitive topics than Western peers.[web:109][web:118]
Security risk framing: U.S. government reports group Chinese models like Qwen under “adversary AI,” warning of security and censorship risks for foreign users.[web:116][web:121]
Data‑privacy uncertainties: as with other Chinese providers, there are concerns about how user data is stored, processed, and potentially accessible to Chinese authorities, especially for cloud‑hosted Qwen on Alibaba Cloud.[web:100][web:116]
1.9.6 Best use cases for freelance prompt engineers — [CHINESE MODEL]
Cost‑sensitive open‑source or hybrid deployments where clients want to fine‑tune and host models themselves.
Projects targeting Chinese markets or multilingual use where Qwen’s training data offers advantages.[web:112][web:118]
Research into censorship and propaganda behaviors in LLMs.[web:115][web:112]
1.9.7 Recent updates, changes, controversies — [CHINESE MODEL][PROBLEMATIC]
Major price cuts (2025‑11): Alibaba halved Qwen3‑Max prices, intensifying China’s AI price war and making Qwen even more attractive on cost grounds.[web:71][web:77]
Bias and propaganda research: studies show Qwen3 is tuned to provide positive messaging about China, raising concerns about hidden alignment goals.[web:115][web:118]
U.S. security reports: U.S. agencies increasingly flag Chinese open‑source models like Qwen as strategic risks to Western AI ecosystems.[web:116][web:121]
1.9.8 Free tier
Many Qwen models are available as open weights, effectively creating a free tier for anyone with compute.
Hosted platforms offer limited free usage for testing, though specifics vary widely.[web:65][web:68]


1.10 Kimi & Qwen in the Chinese AI Models Section
Both Kimi (Moonshot AI) and Qwen (Alibaba) are clearly [CHINESE MODEL] entries with strong technical capabilities, very low prices, and heavy open‑source adoption.[web:64][web:65][web:71]
However, they share common risk patterns: Chinese data‑protection laws, censorship alignment, and potential propaganda usage, plus reports of excessive data collection or lack of transparency.[web:111][web:114][web:115][web:118]


1.11 Chinese AI Models — Summary of Data Privacy, Censorship, Export Controls — [CHINESE MODEL]
1.11.1 Data privacy and security
Chinese LLM providers like DeepSeek, Kimi, and Qwen are subject to China’s National Intelligence Law and cybersecurity regulations, which allow authorities to compel access to data stored on their systems.[web:119][web:111][web:116]
DeepSeek explicitly stores user data on servers in China, and multiple governments have raised concerns or issued restrictions because of this.[web:110][web:113][web:119]
Analyses of Chinese LLM privacy practices find frequent gaps in transparency, consent, and retention disclosures compared with Western providers.[web:100][web:120]
1.11.2 Censorship and propaganda behavior
Studies and news reports show Chinese models systematically refuse or deflect questions on politically sensitive topics such as Tiananmen, Xinjiang, or Taiwan, at far higher rates than Western models.[web:107][web:109]
DeepSeek, Qwen, and Kimi have all been documented to embed content controls and, in Qwen’s case, to promote positive narratives about China beyond what typical safety tuning would require.[web:115][web:112][web:118]
These behaviors mean Chinese models may silently omit or distort information on geopolitical topics, even for foreign users.
1.11.3 Export controls and geopolitical status
DeepSeek’s cost‑effective frontier models have triggered discussions in the U.S. about tightening chip and AI export controls, as they show Chinese labs can reach near‑frontier performance at lower cost.[web:45][web:116][web:121]
U.S. government reports treat Chinese models collectively as “security risks” or “adversary AI,” emphasizing safety gaps, censorship, and strategic implications.[web:116][web:121]
Some countries and organizations have begun banning or restricting Chinese AI tools in official or sensitive contexts, but there is no global uniform ban.[web:113][web:119]


1.12 New Models and Price Changes in the Last 60 Days — [NEW] and ⚠️
1.12.1 New or recently highlighted models — [NEW]
Claude Opus 4.6 / Sonnet 4.6 — [NEW] (late 2025–early 2026): extended context to 1M tokens and refined reasoning; widely covered in early 2026 pricing guides.[web:23][web:32][web:35]
DeepSeek V4 — [NEW] (early 2026‑03): new flagship at $0.30/$0.50 per 1M tokens, 1M context, with improved benchmarks.[web:51]
Kimi K2.5 — [NEW] (released 2026‑01‑27): upgraded model with 256K context and competitive pricing.[web:64]
Google AI Plus — [NEW in US, 2026‑01‑26]: lower‑cost $7.99/month plan with Gemini 3 Pro access and NotebookLM enhancements.[web:85][web:94]
Perplexity Max — [NEW tier]: $200/month plan for individuals with unlimited research and Labs, introduced in 2026 alongside expanded Enterprise tiers.[web:55][web:43]
1.12.2 Price changes vs previous month — ⚠️
Qwen3‑Max price cuts (⚠️ decrease, late 2025): Alibaba halved Qwen3‑Max prices; this is an ongoing discount rather than a new April 2026 move, but it shapes today’s cost landscape.[web:71][web:77]
DeepSeek V4 pricing (⚠️ increase vs V3.x): V4 is about 15% more expensive than V3.2 but still extremely cheap; this is a modest price increase tied to higher quality.[web:51]
No clear evidence of April 2026 price increases for Claude, GPT, or Gemini in mainstream sources; most mention stable prices or past cuts.[web:32][web:37][web:36]


1.13 Best Models by Use Case for Freelance Prompt Engineers (High‑Level)
Deep reasoning & long reports: Claude Opus 4.6 and Claude Sonnet 4.6 are strong choices for complex reasoning, legal/technical analysis, and long context, albeit at higher cost.[web:21][web:35][web:131]
Generalist, multimodal, and ecosystem: GPT‑4.1/5.x via ChatGPT Plus/Business or API remain the safest “default” in terms of ecosystem, code support, and multimodal features.[web:27][web:36][web:93]
Google‑centred workflows: Gemini 2.5 Pro (via Gemini Advanced / AI Premium) plus NotebookLM is ideal for deep document work, course content, and podcast‑style outputs.[web:82][web:66][web:72]
Search‑grounded research: Perplexity Pro/Max excels at quick, cited research and artifact generation without managing raw APIs.[web:46][web:55]
Ultra‑cheap long context: DeepSeek V4, Grok 4.1 Fast, Kimi K2.5, and Qwen coder‑flash offer massive context and very low prices but come with serious privacy or governance trade‑offs (especially Chinese models and Grok).[web:44][web:51][web:64][web:65][web:116]
