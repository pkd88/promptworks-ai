---
name: RULES_HARD
description: >
  Hard ban rules for the avoid-ai-writing skill.
  These patterns are always flagged and always fixed. No exceptions.
  No context makes them acceptable. Fix on sight.
part-of: avoid-ai-writing
version: 1.0.0
---

# Hard Rules — Always Flag, Always Fix

These are P0 and P1 patterns. No judgment call needed.
If you see them, flag them and fix them.

---

## H1 — Em Dashes

**Why:** The single most publicly recognized AI writing tell in 2026.
People actively hunt for these. Reddit jokes about them. They are a dead giveaway.

**What to ban:**
- The Unicode em dash: —
- The double-hyphen substitute: --

**What is NOT banned:**
- A regular hyphen used as a separator - like this - with spaces around it.
  This is human, intentional, and should never be touched.

**How to fix:**
Replace every em dash with one of these alternatives:
- A comma
- A period (split into two sentences)
- Parentheses for an aside
- A colon for an introduction or explanation
- Rewrite the sentence entirely to remove the pause structure

**Examples:**

❌ "The approach was simple — and it worked."
✅ "The approach was simple, and it worked."

❌ "Three things matter here — speed, clarity, and trust."
✅ "Three things matter here: speed, clarity, and trust."

❌ "It was fast -- faster than expected."
✅ "It was fast. Faster than expected."

---

## H2 — Chatbot Filler Phrases

**Why:** These are artifacts of chat interfaces leaking into writing.
They signal a machine performing helpfulness, not a person communicating.

**Full ban list — remove entirely, no replacement needed:**
- "Great question!"
- "Excellent question!"
- "That's a really insightful observation."
- "Certainly!"
- "Absolutely!"
- "Of course!"
- "Sure!"
- "I'd be happy to help."
- "I'd be happy to assist."
- "I hope this helps!"
- "Feel free to reach out."
- "Feel free to ask."
- "Let me know if you need anything else."
- "Don't hesitate to ask."
- "Don't hesitate to reach out."
- "Please let me know if you have any questions."
- "Is there anything else I can help you with?"
- "I trust this email finds you well."
- "I hope this email finds you well."
- "Best regards" / "Warm regards" (in AI-generated body text, not human sign-offs)

**Also ban these meta-narration openers:**
- "In this article, we will explore..."
- "In this post, I will cover..."
- "Let's dive in!"
- "Let's get started!"
- "Without further ado..."

---

## H3 — Contrastive Reframing (The "Not X, It's Y" Pattern)

**Why:** The most recognized ChatGPT writing tell.
AI uses this constantly to sound insightful. It usually just delays the point.

**Full pattern list — ban all forms:**
- "It's not X, it's Y."
- "It's not just X, it's Y."
- "This isn't about X, it's about Y."
- "This isn't just about X. It's about Y."
- "The question isn't X. The question is Y."
- "Not because X, but because Y."
- "You're not doing X. You're doing Y."
- "The goal isn't X. It's Y."
- "This isn't X — it's Y." (also catches the em dash version)

**How to fix:**
Remove the negative frame entirely. State the positive claim directly.

❌ "It's not just about speed. It's about building something people trust."
✅ "Building something people trust matters more than raw speed."

❌ "This isn't a writing problem. It's a thinking problem."
✅ "The real problem is unclear thinking, not unclear writing."

**Exception:**
One genuine contrastive reframe per piece is acceptable if it is doing
real rhetorical work — setting up a meaningful pivot, not just sounding clever.
Flag all instances. Let the writer decide if any one earns its place.

---

## H4 — Self-Posed Questions Answered Immediately

**Why:** AI asks questions nobody was asking, then answers them for dramatic effect.
It is filler wearing a rhetorical costume.

**Pattern:**
- "The result? Better outcomes."
- "The best part? It's free."
- "Why does this matter? Because..."
- "What's the takeaway? Simple."
- "The kicker? Nobody noticed."
- "The catch? There isn't one."

**How to fix:**
Remove the question. State the point directly.

❌ "The result? A 40% improvement in output quality."
✅ "Output quality improved 40%."

❌ "Why does this matter? Because most teams skip this step entirely."
✅ "Most teams skip this step entirely, which is why it matters."

---

## H5 — Fake-Insight Signposting

**Why:** These pre-announce importance instead of earning it.
If something is interesting, the content should prove it — not a label.

**Full ban list:**
- "Here's the thing..."
- "Here's what people miss..."
- "Here's the kicker..."
- "Here's what matters..."
- "Here's what most people get wrong..."
- "Here's what nobody's saying..."
- "Here's where it gets interesting..."
- "Here's what I mean..."
- "And here's the part most people miss."
- "But here's the truth..."
- "The truth is..."
- "Let's face it..."

**How to fix:**
Delete the signpost. Start with the actual point.

❌ "Here's the thing — most AI rules focus on words, not structure."
✅ "Most AI rules focus on words, not structure."

---

## H6 — Reader-Steering Emotional Claims

**Why:** Tell-don't-show. If something is surprising, the content should feel that way.
Announcing the emotion is a lazy substitute for making the reader feel it.

**Full ban list:**
- "What surprised me most..."
- "What stood out was..."
- "What caught my eye..."
- "I was fascinated to discover..."
- "The most interesting part..."
- "What struck me was..."
- "I was excited to learn..."
- "Interestingly," (as a sentence opener — see soft rules for density use)

**How to fix:**
Delete the frame. Present the content directly.

❌ "What surprised me most was that 70% of readers never finish the first paragraph."
✅ "70% of readers never finish the first paragraph."

---

## H7 — Generic Wrap-Ups and Filler Conclusions

**Why:** These are non-endings. They say nothing specific to the piece.
Any AI output could end with these words. That is the problem.

**Full ban list:**
- "The future looks bright."
- "Only time will tell."
- "One thing is certain..."
- "As we move forward..."
- "At the end of the day..."
- "In conclusion..."
- "To summarize..."
- "To wrap up..."
- "In summary..."
- "Ultimately..."
- "A key takeaway is..."
- "The bottom line is..."
- "Looking ahead..."
- "The possibilities are endless."
- "The journey is just beginning."

**How to fix:**
End on the last real point. Or write a closing sentence that is
specific to the actual argument — something that could only belong
to this piece and no other.

---

## H8 — Hype and Significance Inflation

**Why:** AI inflates routine events into history-making moments.
If the sentence still works after you delete the inflation clause, delete it.

**Always replace or remove:**
- "game-changing"
- "revolutionary"
- "transformative" (unless describing a specific, named transformation)
- "groundbreaking"
- "unprecedented" (unless you can name the precedent it breaks)
- "a watershed moment"
- "marking a pivotal moment in..."
- "marking a significant milestone"
- "pushing the boundaries of..."
- "unlocking the potential of..."
- "unleashing the power of..."
- "paving the way for..."
- "redefining the future of..."
- "a game-changer for the industry"
- "changing the way we [verb]"

**How to fix:**
State what specifically happened. Let the reader judge the significance.

❌ "This is a groundbreaking development that will revolutionize the way teams collaborate."
✅ "Teams can now edit the same document without version conflicts."

---

## H9 — Cutoff Disclaimers

**Why:** Model limitations leaking into prose. Never publish a sentence
that admits the writer did not look something up.

**Full ban list:**
- "As of my last update..."
- "As of my knowledge cutoff..."
- "Based on available information..."
- "While specific details are limited..."
- "I don't have access to real-time data..."
- "At the time of writing..."
- "This may have changed since..."

**How to fix:**
Either find the current information, or remove the sentence entirely.
Do not hedge in print. If you do not know, do not guess and disclaim.

---

## H10 — Vague Unsourced Attributions

**Why:** Manufactures authority without evidence.
If you cannot name the expert, study, or leader — drop the attribution.

**Full ban list:**
- "Experts believe..."
- "Studies show..."
- "Research suggests..."
- "Industry leaders agree..."
- "Many professionals say..."
- "It is widely accepted that..."
- "According to experts..."

**How to fix:**
Name a specific source with context, or drop the attribution and
state the claim directly on its own authority.

❌ "Experts believe AI will reshape most white-collar jobs by 2030."
✅ "AI will reshape most white-collar jobs by 2030." (if you believe it, own it)
✅ "In a 2024 McKinsey report, analysts estimated AI could affect 70% of work tasks." (if you have a source, cite it)

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: RULES_SOFT.md*
