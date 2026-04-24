---
name: RULES_SOFT
description: >
  Soft flag rules for the avoid-ai-writing skill.
  These patterns are flagged but not automatically fixed.
  Context determines whether they are problems.
  Use judgment. Not every instance needs a rewrite.
part-of: avoid-ai-writing
version: 1.0.0
---

# Soft Rules — Flag With Judgment

These are P1 and P2 patterns. They are real AI tells, but context matters.
Flag them. Explain why. Let severity and density guide the fix.

A single instance of most of these is fine.
Two or three in the same paragraph or page is a signal.
Saturation across a whole piece means the structure itself needs work.

---

## S1 — Tier 1 Words (Flag on Sight, Replace With Better Option)

These words appear far more often in AI text than human text.
They are not banned from existence — they are banned from being the default.
If a simpler word works, use it.

| Replace | With |
|---|---|
| delve / delve into | look at, explore, dig into |
| leverage (verb) | use |
| utilize | use |
| robust | strong, solid, reliable |
| seamless / seamlessly | smooth, easy, without friction |
| comprehensive | thorough, complete, full |
| cutting-edge | latest, newest, advanced |
| pivotal | key, important, critical |
| meticulous / meticulously | careful, precise, detailed |
| underscores | shows, highlights |
| embark | start, begin |
| testament to | shows, proves, demonstrates |
| showcase / showcasing | show, demonstrate |
| deep dive / dive into | look at, examine, explore |
| unpack / unpacking | explain, break down, walk through |
| actionable | practical, useful, concrete |
| impactful | effective, significant |
| holistic / holistically | complete, full, whole |
| synergy / synergies | describe the actual combined effect |
| tapestry | describe the actual complexity |
| realm | area, field, domain |
| paradigm | model, approach, framework |
| thought leader / thought leadership | expert, authority |
| best practices | what works, standard approach |
| at its core | cut — just state the thing |
| in order to | to |
| due to the fact that | because |
| serves as | is |
| boasts | has |
| features (inflated verb) | has, includes |
| presents (inflated) | is, shows, gives |
| commence | start, begin |
| endeavor | effort, attempt, try |
| nestled | is located, sits, is in |
| vibrant | describe what makes it active, or cut |
| bustling | busy, active |
| intricate / intricacies | complex, detailed |
| ever-evolving | changing, growing |
| enduring | lasting, long-running |
| daunting | hard, difficult, challenging |
| learnings | lessons, findings, takeaways |
| interplay | relationship, connection, interaction |
| keen (as intensifier) | interested, eager |
| embrace (metaphor) | adopt, accept, use |
| beacon | rewrite entirely |
| symphony (metaphor) | describe the actual coordination |
| watershed moment | turning point, shift |

---

## S2 — Tier 2 Words (Flag When Two or More Appear in the Same Paragraph)

These words are individually fine. When two or more cluster together,
the paragraph likely needs a rewrite. AI uses them as filler when
it runs out of specific things to say.

Flag the cluster. Do not flag individual words in isolation.

harness, navigate, foster, elevate, unleash, streamline, empower, bolster,
spearhead, resonate, revolutionize, facilitate, underpin, nuanced,
multifaceted, ecosystem, myriad, plethora, encompass, catalyze, reimagine,
cultivate, illuminate, elucidate, juxtapose, cornerstone, paramount,
poised, burgeoning, nascent, quintessential, overarching, underpinning,
transformative, galvanize, augment

**How to fix:**
Rewrite the paragraph with plain words. If the ideas are real,
plain language will carry them. If plain language makes the paragraph
feel empty, the ideas were not there to begin with.

---

## S3 — Tier 3 Words (Flag at High Density Only)

These are common words. Only flag them when the text is saturated —
a sign that AI filled space with vague praise instead of specific details.
Rough threshold: if any of these make up a noticeable fraction of
descriptive words across the piece, flag the pattern.

When flagging, the fix is always the same: replace vague praise with
a specific number, comparison, example, or name.

| Word | Fix |
|---|---|
| significant / significantly | Give a number or comparison |
| innovative / innovation | Describe what is actually new |
| effective / effectively | Say how, or cite a metric |
| dynamic / dynamics | Name the actual forces or changes |
| scalable / scalability | Describe what scales and to what |
| compelling | Say why it compels |
| unprecedented | Name the precedent it breaks, or cut |
| exceptional / exceptionally | Cite what makes it an exception |
| remarkable / remarkably | Say what is worth remarking on |
| sophisticated | Describe the sophistication |
| instrumental | Say what role it played |
| world-class / state-of-the-art / best-in-class | Cite a benchmark or comparison |

---

## S4 — Stacked Transitions

**Why it matters:**
One transition is normal. Three in the same piece is a metronomic AI rhythm.
AI uses these to simulate logical flow without actually connecting ideas.

**Flag when stacked:**
- "Additionally," / "Moreover," / "Furthermore," / "In addition,"
- "Notably," / "Importantly," / "Crucially," / "Significantly,"
- "Consequently," / "Subsequently," / "Therefore," / "Thus,"
- "Nevertheless," / "Nonetheless," / "That said," / "That being said,"
- "Interestingly," (as sentence opener)

**How to fix:**
Restructure so the connection between ideas is obvious without a label.
Or use plain connectors: "and," "but," "also," "on top of that," "even so."

❌ "The model improved accuracy. Furthermore, it reduced processing time.
    Additionally, it cut costs by 30%."
✅ "The model improved accuracy, cut processing time, and reduced costs by 30%."

---

## S5 — Rhythm and Sentence Length Uniformity

**Why it matters:**
AI sentences cluster tightly between 15 and 20 words.
Human writing swings from 3-word fragments to 40-word sprawls.
If every sentence is roughly the same length, the text reads robotic
even when the vocabulary is fine.

**What to flag:**
- More than two consecutive sentences in the same approximate length range
- A full paragraph where no sentence is under 8 words or over 25 words
- An entire piece with no fragments, no short punchy lines, no long flowing sentences

**How to fix:**
Break the pattern deliberately.
- Cut a long sentence into two. Keep one short.
- Combine two short sentences into one flowing one.
- Add a fragment for punch. Like this.
- Let one sentence run longer than feels comfortable.

---

## S6 — Paragraph Length Uniformity

**Why it matters:**
If every paragraph is 3 to 5 sentences and roughly the same word count,
the visual rhythm is a structural AI tell — even if every word is clean.

**What to flag:**
- More than four consecutive paragraphs at the same approximate length
- No single-sentence paragraphs anywhere in a long piece
- Every section ends with a wrap-up sentence of similar structure

**How to fix:**
Vary deliberately.
- Make one paragraph one sentence.
- Let one paragraph run longer than the rest.
- Break a medium paragraph into two short ones.
- Merge two short paragraphs into one longer one.

---

## S7 — Bullet Overuse

**Why it matters:**
Bullets work for genuinely list-like content.
AI defaults to bullets for everything because they look organized.
When a short post has three bullet sections and minimal prose,
it reads as AI-generated regardless of word choice.

**What to flag:**
- More than two bullet sections in under 400 words
- Bullet lists where each item is a full sentence that could be prose
- Bullet lists where every item starts with a bold header (inline-header lists)
- Numbered lists padded to hit a count: "5 Things to Know," "7 Key Takeaways"

**How to fix:**
Convert bullet-heavy sections into prose paragraphs.
Reserve bullets for: feature comparisons, step-by-step instructions,
parameter lists, or any content that is genuinely parallel and list-like.

---

## S8 — Bold Overuse

**Why it matters:**
AI bolds random words throughout a piece for "readability."
This is a deeply embedded training habit from SEO content.
When every third sentence has a bolded phrase, nothing is actually emphasized.

**What to flag:**
- More than one bolded phrase per major section
- Bolding that highlights the obvious rather than the surprising
- Bolding used as a substitute for strong sentence structure

**How to fix:**
Strip bold from most phrases.
If something is important enough to bold, restructure the sentence to lead with it.
One bolded phrase per section at most. Zero is often cleaner.

---

## S9 — Copula Avoidance

**Why it matters:**
AI avoids "is" and "has" by substituting fancier verbs.
It sounds like a press release.

**Flag these substitutions:**
- "serves as" → is
- "features" (as verb) → has, includes
- "boasts" → has
- "presents" (inflated) → is, shows
- "represents" → is
- "functions as" → is, works as
- "acts as" → is

**How to fix:**
Default to "is" or "has" unless a more specific verb genuinely adds meaning.

❌ "The platform features a robust dashboard that serves as a central hub."
✅ "The platform has a dashboard that shows all your key metrics in one place."

---

## S10 — Synonym Cycling

**Why it matters:**
AI rotates synonyms to avoid repeating a word.
Human writers repeat the clearest word and vary only when it is natural.
Forced variation reads as thesaurus abuse and is actually an AI tell.

**What to flag:**
- Same concept referred to by three or more different words in one paragraph:
  "developers… engineers… practitioners… builders"
- A word replaced by an obviously weaker synonym just to avoid repetition

**How to fix:**
If "developers" is the right word, use it three times in a row if needed.
Repeat the clearest word. Only vary when variation is natural, not forced.

---

## S11 — False Balance and Both-Sidesism

**Why it matters:**
AI is trained to be neutral. The result is compulsive balance that
never takes a position. "While X has advantages, Y also has merits."
This sounds analytical but says nothing.

**What to flag:**
- "While X is impressive, Y remains a challenge." (vague on both sides)
- "Although X has made strides, Y is still an open question."
- "On one hand... on the other hand..." with no resolution
- Concession sentences that do not name the specific concession

**How to fix:**
Either make both sides specific — name what is impressive, name the actual challenge —
or pick a position and argue it. Not everything needs a counterpoint.

---

## S12 — Superficial Present-Participle Endings

**Why it matters:**
AI tacks shallow analysis onto sentence endings with present participles.
They sound analytical but introduce no new information.

**What to flag:**
- "...contributing to the region's rich cultural heritage."
- "...highlighting its importance in the broader ecosystem."
- "...reflecting broader trends in the industry."
- "...solidifying its position as a leader."
- "...demonstrating the power of this approach."
- "...underscoring the need for further research."

**How to fix:**
Cut the trailing clause entirely. If the analysis matters, give it its own sentence
with specific content. If cutting it loses nothing, it was never there.

❌ "The team shipped on time, demonstrating their commitment to quality."
✅ "The team shipped on time."

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: RULES_LEAVE_ALONE.md*
