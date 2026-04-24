---
name: MODEL_TELLS
description: >
  Model-specific writing patterns for the avoid-ai-writing skill.
  Each major AI model has recognizable habits beyond generic AI tells.
  Use this file when the user wants model-specific pattern detection,
  or when a piece of writing has a distinctive model fingerprint.
part-of: avoid-ai-writing
version: 1.0.0
---

# Model Tells — Fingerprints by AI

Generic AI tells are covered in RULES_HARD.md and RULES_SOFT.md.
This file covers patterns that are associated with specific models.

Important caveat: these are tendencies, not proof.
No single pattern proves a specific model wrote something.
These are signals, not verdicts. Use them to guide revision, not accusation.

---

## ChatGPT (OpenAI)

ChatGPT is the most widely discussed model for writing tells.
Its patterns lean toward sounding insightful before it has earned it,
and toward dramatic structure that substitutes flair for substance.

### C1 — Contrastive Reframing
The single most recognized ChatGPT pattern. Already in RULES_HARD.md H3.
Listed here for completeness and cross-reference.

- "It's not X, it's Y."
- "It's not just X, it's Y."
- "This isn't about X. It's about Y."

Fix: state the positive claim directly without the negative setup.

### C2 — Tidy Symmetrical Structure
ChatGPT tends to build responses with even section sizes, equal bullet counts,
and matching paragraph weights. Every section gets roughly the same treatment.

What to flag:
- Three sections with almost the same word count
- Bullet lists where every item is one sentence of the same length
- Intro, three equal body sections, wrap-up — every time

Fix: break one section longer than the rest. Merge two short ones. Add a fragment.

### C3 — Rhetorical Question as Section Opener
ChatGPT drops a rhetorical question before almost every main point.

- "But what does this mean for teams?"
- "So why should you care about this?"
- "What's the real lesson here?"

Flag when: rhetorical questions appear at the start of multiple sections in a row.
One rhetorical question as a hook opener is fine. Three in one piece is a pattern.

Fix: if you know the answer, just say it. The question is filler.

### C4 — The Neat Wrap-Up
ChatGPT almost always ends with a polished summary sentence or closing thought
that could appear at the end of any piece on any topic.

Already covered in RULES_HARD.md H7.
Flag especially when the closing could be swapped into another article unchanged.

### C5 — Compulsive Rule of Three
ChatGPT stacks tricolons constantly. Three balanced items, three supporting points,
three reasons, three examples.

Flag when: rule-of-three appears more than once in a short piece.
Fix: use two items sometimes. Use four. Break the rhythm deliberately.

---

## Claude (Anthropic)

Claude's tells are more about tone than vocabulary.
Its writing is often clean, balanced, and thoughtful to the point of feeling
emotionally managed. It sounds like someone being very careful.

### CL1 — Warm Validating Tone
Claude frequently validates before responding.

- "You're absolutely right that..."
- "That's a really good point."
- "This is a thoughtful question."
- "I appreciate you raising this."

Fix: remove the validation and start with the actual response.

### CL2 — Over-Explanation
Claude tends to explain things more thoroughly than needed.
The answer appears, then gets explained, then gets summarized, sometimes in the same paragraph.

What to flag:
- A point that is stated, then expanded, then restated in slightly different words
- A paragraph that could end after the second sentence but keeps going
- Section endings that summarize what was just said

Fix: cut everything after the point is made. Trust the reader.

### CL3 — Diplomatic Both-Sidesism
Claude is trained to be balanced. This often produces writing that
presents two sides without taking a position — even when a position is appropriate.

Already covered in RULES_SOFT.md S11.
Flag especially when the concession in "while X, Y" is vague on both sides.

### CL4 — Elegant Smoothness
Claude's sentences tend to flow very cleanly. Too cleanly.
Every transition is smooth. Every paragraph connects to the last.
The rhythm is even and pleasant throughout.

This is a subtle tell because it is not a bad thing in isolation.
But human writing has rough spots. Claude often has none.

What to flag:
- A piece where every paragraph is the same approximate smoothness level
- No awkward sentence anywhere in a long piece
- Every transition working perfectly

Fix: leave a rough edge. Trust an imperfect sentence. Do not sand everything down.

### CL5 — Tasteful Over-Polish
Claude writes like it is always being evaluated.
The vocabulary is always appropriate. The tone is always considered.
Nothing is too casual, nothing too blunt.

What to flag:
- Formal vocabulary where casual would be more natural
- No strong opinion anywhere in a piece that should have one
- A piece that sounds like it was written to please everyone

Fix: take a position. Use a blunt word where a blunt word is right.
Say something is bad if it is bad.

---

## Grok (xAI)

Grok's tells tend toward confidence, edge, and internet-native tone.
It tries to sound like a smart person who is online a lot.

### G1 — Edgy or Cheeky Asides
Grok inserts casual, slightly provocative comments as if to signal it is not
like other AI models. These can feel forced.

What to flag:
- Parenthetical comments that are trying to be funny or irreverent
- Sentences that undercut a serious point with a wink
- "Not to be dramatic, but..." style asides

Fix: if the aside does not add information, cut it.

### G2 — Posting Voice
Grok often writes like someone composing a good social media post
rather than a thoughtful document. This shows up as:

- Short declarative sentences stacked for rhythm
- Confidence stated rather than demonstrated
- A conversational opener that feels like a tweet

What to flag:
- A document that reads like a thread
- Opening sentences that feel like they need a Like button

Fix: adjust the register to match the actual document type.

### G3 — Overconfident Claims
Grok can assert positions with more confidence than the evidence supports.

What to flag:
- Strong claims without supporting specifics
- "This is clearly..." or "Obviously..." without explanation
- Dismissing complexity too quickly

Fix: back the claim with a specific, or qualify it honestly.

---

## Perplexity (PPX)

PPX is built for search and research, so its writing tends to feel assembled
rather than authored. It sounds like a very competent librarian.

### P1 — Research-Summary Structure
PPX naturally organizes answers as: direct answer, then supporting points,
then structured breakdown. This is great for research. It reads as AI in a document.

What to flag:
- A piece that reads like a search result summary
- Headers that map exactly to the question asked
- Every paragraph starting with the answer to a sub-question

Fix: reorganize around argument and narrative, not question-and-answer.

### P2 — Citation-Heavy Assembly Feel
PPX writes as if it is aggregating sources even when it is not.
The tone is often "here is what the sources say" rather than "here is what I think."

What to flag:
- Sentences that feel attributed even without citations
- Writing that presents every claim as established fact from somewhere
- No voice, no opinion, no position — just reporting

Fix: take a position. Own a claim. Let the writing have a point of view.

### P3 — Competent Neutral Tone
PPX does not have warmth like Claude or edge like Grok.
It is accurate, organized, and flat. Reliably competent but rarely specific.

What to flag:
- A piece that is technically correct but has no distinctive voice
- Every sentence could belong to any answer on the same topic
- Nothing that sounds like a specific person said it

Fix: add one concrete detail, one specific example, or one stated opinion
that could only belong to this piece and no other.

---

## Gemini (Google)

Gemini tends toward organized, helpful, thorough responses.
Its patterns overlap with ChatGPT in structure but lean more toward
comprehensive coverage and less toward dramatic flair.

### GM1 — Thoroughness Over Focus
Gemini tries to cover all angles. This leads to longer answers that
address every possible interpretation of a question.

What to flag:
- An answer that covers three possible meanings of the question
  when the user clearly meant one
- Sections that exist for completeness rather than relevance
- "It depends" as a frequent answer structure

Fix: pick the most likely interpretation and answer that one directly.

### GM2 — Helpful Bot Energy
Gemini can lean into being helpful in a way that feels performative.

What to flag:
- Multiple offers to help at the end of a response
- Checking in mid-response: "Does this help? Let me know if you'd like more."
- Framing everything as a service: "Here is what you requested..."

Fix: already covered in RULES_HARD.md H2 chatbot artifacts.

---

## Cross-Model Tells (Any Model)

These patterns appear across all models and are already covered in the rules files.
Listed here as a quick cross-reference for model-agnostic audits.

| Pattern | Rule file | Rule number |
|---|---|---|
| Em dashes | RULES_HARD.md | H1 |
| Chatbot filler phrases | RULES_HARD.md | H2 |
| Contrastive reframing (not X, it's Y) | RULES_HARD.md | H3 |
| Self-posed questions answered immediately | RULES_HARD.md | H4 |
| Fake-insight signposting | RULES_HARD.md | H5 |
| Generic wrap-ups | RULES_HARD.md | H7 |
| Hype and significance inflation | RULES_HARD.md | H8 |
| Uniform sentence length | RULES_SOFT.md | S5 |
| Uniform paragraph length | RULES_SOFT.md | S6 |
| Bullet overuse | RULES_SOFT.md | S7 |
| False balance | RULES_SOFT.md | S11 |

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: OUTPUT_FORMAT.md*
