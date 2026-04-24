---
name: RULES_LEAVE_ALONE
description: >
  Defines what the avoid-ai-writing skill must never flag, fix, or touch.
  These are human voice markers. Editing them out pushes writing back
  toward AI statistical profiles. Protect them.
part-of: avoid-ai-writing
version: 1.0.0
---

# Leave Alone — Protect the Human Voice

This file is as important as the rules files.
Over-editing is a real failure mode. Aggressively removing every irregularity
can make human writing sound more like AI, not less.

If something on this list is flagged by a rule elsewhere in this skill,
this file wins. Do not touch it.

---

## L1 — The Regular Hyphen Separator

A regular hyphen used as a separator - like this - with spaces around it
is human, intentional, and often a personal writing habit.

Do not flag it.
Do not suggest replacing it.
Do not confuse it with an em dash.

The difference:
- Em dash: no spaces, longer line —  ← ban this
- Hyphen separator: spaces on both sides -  ← leave this alone

This distinction is noted in RULES_HARD.md rule H1.
It is repeated here because it is important enough to say twice.

---

## L2 — Normal Inconsistency

Real people are inconsistent. Punctuation varies. Spacing varies.
Capitalization drifts. Sentence structure shifts between paragraphs.

Do not flag inconsistency as an AI tell.
Inconsistency is a human tell.

What to leave alone:
- Inconsistent comma placement
- Inconsistent capitalization in casual writing
- Mixed sentence structures across a piece
- Spacing quirks that do not affect readability
- Punctuation habits that vary without a rule

---

## L3 — Deliberate Fragments

Fragments are a legitimate writing tool.
Short punchy sentences that are technically incomplete are fine.
They are often the best choice for emphasis.

Leave these alone:
- "Like this."
- "Exactly right."
- "Not even close."
- One-word sentences used for rhythm or emphasis
- Any fragment that is clearly intentional

Flag only fragments that appear to be accidental — where meaning is lost
or the sentence is genuinely confusing without a subject or verb.

---

## L4 — Sentences Starting With And, But, Or So

Starting a sentence with a coordinating conjunction is correct English.
It is also how people naturally write and talk.

Do not flag:
- "And that is the real problem."
- "But nobody checked."
- "So here is what happened."
- "Or you could skip it entirely."

These are natural connectors. AI avoidance rules sometimes ban them
as "casual." That is wrong. Leave them alone.

---

## L5 — Contractions

In casual and conversational writing, contractions are the human default.
Removing them pushes writing toward stiff formal prose.

Always leave contractions in casual, conversational, and informal writing:
- it's, can't, don't, won't, isn't, wasn't, they're, we're, you're
- I'd, I've, I'll, we'd, we've, that's, there's, here's

Only remove contractions when:
- The content is genuinely formal (legal, academic, official documents)
- The user explicitly asks for formal register
- The profile is investor-email or docs and formal tone is required

---

## L6 — Repeated Words When Repetition Is Right

Human writers repeat the clearest word. AI cycles synonyms to avoid repetition.
Forced synonym variation is itself an AI tell (see RULES_SOFT.md S10).

Do not flag or fix:
- Using "developers" three times in a paragraph when that is the right word
- Repeating a key term for clarity and consistency
- Deliberate anaphora used for rhetorical effect

Only flag repetition when it is clearly accidental or when a more specific
word genuinely improves meaning.

---

## L7 — Personal Voice Quirks

If a piece of writing has consistent idiosyncratic patterns that appear
to be intentional stylistic choices, leave them alone.

Examples of personal quirks to protect:
- Unusually short paragraphs as a consistent habit
- A signature phrase or turn of expression used repeatedly
- Unconventional but consistent punctuation choices
- A distinctive rhythm that runs through the whole piece
- Casual asides or digressions that feel like the writer's voice

The goal of this skill is to remove AI patterns, not to impose a house style.
If something does not look like an AI pattern — if it looks like a person —
leave it alone.

---

## L8 — Rough Edges That Do Not Hurt Meaning

Not every imperfection is a problem.
Rough edges, minor awkwardness, and small irregularities are often what
keep writing in the "human" classification.

Do not flag:
- A slightly awkward sentence that is still clear
- A word choice that is not optimal but is natural
- Minor structural looseness that does not confuse the reader
- A transition that is not perfectly smooth but feels genuine

Only flag rough edges when they genuinely hurt clarity or meaning.
Never fix something just because a cleaner version exists.

---

## L9 — Casual Register in Casual Contexts

In casual writing — Slack messages, quick replies, informal posts, notes —
almost all soft rules should be skipped entirely.

In casual context, leave alone:
- Transition words used freely
- Informal phrasing and slang
- Shorter and looser structure
- Minimal punctuation
- All the things that would be flagged in a blog post

See PROFILES.md for the casual profile definition.
When in casual mode, only P0 hard bans apply.

---

## L10 — The One Test For This File

Before flagging or fixing anything, ask:

**Does this look like a person wrote it, or does it look like a machine wrote it?**

If it looks like a person — even an imperfect, inconsistent, quirky person —
leave it alone.

This skill exists to remove machine patterns.
It does not exist to make writing perfect.
Perfect is often its own AI tell.

---

*Version 1.0.0 — April 2026*
*Part of: avoid-ai-writing skill*
*Next: PROFILES.md*
