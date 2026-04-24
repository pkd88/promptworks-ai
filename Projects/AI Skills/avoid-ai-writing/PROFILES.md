---
name: PROFILES
description: >
  Context profiles for the avoid-ai-writing skill.
  Rules do not apply equally in every context.
  A blog post and a Slack message are not the same job.
  Load the right profile before auditing or writing.
part-of: avoid-ai-writing
version: 1.0.0
---

# Profiles — Context Changes the Rules

Not every rule applies in every situation.
Match the profile to the content before auditing or writing.
If no profile is specified, auto-detect from the content cues below.
If auto-detection feels wrong, say which profile you are using and why.

---

## Auto-Detection Cues

| Signal in the content | Inferred profile |
|---|---|
| Under 300 words, hashtags, or @ mentions | social |
| Code blocks, API references, technical architecture | technical |
| Salutation ("Hi [name]", "Dear") + business language | email |
| Step-by-step instructions, parameters, README structure | docs |
| Casual, short, no formal structure | casual |
| None of the above | blog (default) |

---

## Profile: blog (Default)

**What it is:** Standard long-form prose. Articles, newsletters, opinion pieces, guides.

**Rule strictness:** Full strength. All hard rules and soft rules apply.

**Special notes:**
- Vary sentence and paragraph length deliberately
- No generic conclusions — end on something specific to the argument
- No excessive headers in short pieces
- Bold used sparingly, not for decoration

---

## Profile: social

**What it is:** LinkedIn posts, Twitter/X threads, short-form public posts, Reddit comments.

**Rule strictness:** Strict on hard rules. Relaxed on structure rules.

**Apply at full strength:**
- All H rules (hard bans) — no chatbot filler, no contrastive reframing, no hype
- Tier 1 word replacements
- Fake-insight signposting

**Relax or skip:**
- Em dash limit: 2 per post is acceptable on social
- Bullet overuse: lists work well on social, skip this rule
- Uniform paragraph length: short-form, skip this rule
- Transition phrases: skip, too short for stacking to matter
- Generic conclusions: skip for short-form

**Special notes:**
- One or two emoji at the end of a line are acceptable — never mid-sentence
- A single rhetorical question as a hook opener is fine
- Voice can be punchier and more direct than blog

---

## Profile: email

**What it is:** Direct outreach, client emails, follow-ups, proposals.

**Rule strictness:** Strict across the board. Promotional language is the biggest risk.

**Apply at full strength:**
- All H rules
- All Tier 1 and Tier 2 word replacements
- Significance inflation — extra strict in professional email
- Generic conclusions — extra strict, never end with "Looking forward to connecting"
- False balance — pick a position

**Apply extra strictly:**
- Promotional language: a single "thriving ecosystem" or "game-changing solution"
  can undermine the entire email
- Significance inflation: one inflated phrase and the reader stops trusting you
- Chatbot closers: "Best regards" from AI-generated body text is acceptable
  as a sign-off only, never in the body

**Relax or skip:**
- Emoji: skip entirely in professional email
- Bullet overuse: structured lists are fine in email

**Special notes:**
- Read the closing line last. Generic email closers are a P0 problem in this profile.
- If the email sounds like a template, it probably is one. Rewrite from the specific point.

---

## Profile: docs

**What it is:** Documentation, READMEs, technical guides, how-to instructions, help articles.

**Rule strictness:** Clarity over voice. Most style rules are relaxed. Accuracy rules are strict.

**Apply at full strength:**
- All H rules — especially cutoff disclaimers and vague attributions
- Chatbot artifacts and filler phrases
- Hype language — docs should never describe features as game-changing

**Relax or skip:**
- Uniform paragraph length: skip, docs have natural structural units
- Copula avoidance: skip, "serves as" is fine in technical description
- Bullet overuse: skip, lists are the correct format in docs
- Transition phrases: relax, some transitions help navigation in long docs
- Synonym cycling: relax, consistent terminology is required in docs
  (use the same term every time, do not vary for style)
- Bold overuse: relax, bold is used functionally for scanning in docs

**Special notes:**
- Repeat terms consistently — docs are not the place for synonym variation
- Numbered lists are correct when steps are sequential
- Headers are functional here, not decorative — use as many as the content needs

---

## Profile: technical

**What it is:** Technical blog posts, architecture writeups, API explanations,
engineering discussions. Long-form with code or technical specifications.

**Rule strictness:** Full strength on hard rules. Partial on word list.

**Apply at full strength:**
- All H rules
- Hype language — especially game-changing, revolutionary, groundbreaking
- Chatbot artifacts
- Fake-insight signposting

**Word list exceptions — these terms have legitimate technical meaning, do not flag:**
- robust (as in "robust error handling")
- comprehensive (as in "comprehensive test coverage")
- seamless (as in "seamless API integration")
- ecosystem (as in "the JavaScript ecosystem")
- leverage (when discussing actual platform capabilities or APIs)
- facilitate (as in "facilitates communication between services")
- underpin (as in "the protocol that underpins this system")
- streamline (as in "streamlines the build process")

**Still flag in technical context:**
- delve, tapestry, beacon, embark, testament to, game-changer, harness
  (these have no legitimate technical meaning)

**Relax or skip:**
- Uniform paragraph length: relax, technical writing has natural breaks
- Numbered lists: relax, sequential steps need numbers
- Emoji in headers: skip entirely

---

## Profile: casual

**What it is:** Slack messages, internal notes, quick replies, texts, informal team chat.

**Rule strictness:** Minimal. Only the worst offenders matter here.

**Apply:**
- P0 hard bans only: chatbot artifacts, cutoff disclaimers, vague attributions
- Em dashes (still ban these — they look wrong even in casual writing)

**Skip everything else:**
- All soft rules
- Transition phrases
- Paragraph and sentence uniformity
- Word tier lists
- Bold and bullet rules
- Promotional language
- Generic conclusions

**Special notes:**
- Casual writing is supposed to be rough. Do not sand it down.
- If it sounds like a person dashing off a message, that is correct.
- Only flag something in casual mode if it would make someone stop and
  think "that sounds like a bot."

---

## Tolerance Summary

Rules not listed as relaxed or skipped apply at full strength.

| Rule | blog | social | email | docs | technical | casual |
|---|---|---|---|---|---|---|
| Em dashes | strict | 2 per post OK | strict | strict | strict | strict |
| Bold overuse | strict | relaxed | strict | relaxed | strict | skip |
| Emoji in headers | strict | end-of-line OK | skip | skip | skip | skip |
| Bullet overuse | strict | skip | relaxed | skip | relaxed | skip |
| Uniform paragraph length | strict | skip | strict | relaxed | relaxed | skip |
| Transition phrases | strict | skip | strict | relaxed | strict | skip |
| Generic conclusions | strict | skip | extra strict | skip | strict | skip |
| Promotional language | strict | relaxed | extra strict | strict | strict | skip |
| Significance inflation | strict | strict | extra strict | relaxed | strict | skip |
| Copula avoidance | strict | skip | strict | skip | relaxed | skip |
| Tier 1 word list | strict | strict | strict | relaxed | partial | P0 only |
| Numbered list inflation | strict | relaxed | strict | skip | relaxed | skip |
| Rhetorical questions | strict | 1 as hook OK | strict | strict | strict | skip |
| Synonym cycling | strict | strict | strict | skip | skip | skip |

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: MODEL_TELLS.md*
