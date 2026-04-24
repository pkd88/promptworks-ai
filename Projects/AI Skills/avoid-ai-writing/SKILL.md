---
name: avoid-ai-writing
description: >
  Audit and rewrite content to remove AI writing patterns ("AI-isms").
  Use this skill when asked to "remove AI-isms," "clean up AI writing,"
  "edit writing for AI patterns," "audit writing for AI tells," or
  "make this sound less like AI." Supports a detection-only mode that
  flags patterns without rewriting.
version: 1.0.0
license: MIT
compatibility: >
  Any AI assistant that supports agentskills.io SKILL.md format
  (Claude Code, Cursor, VS Code Copilot, OpenHands, etc.),
  Gemini Gems (as knowledge file), Perplexity Spaces (as attached file),
  or any system prompt that supports markdown instructions.
  No external tools or APIs required.
metadata:
  type: writing-audit
  tags: writing editing voice quality AI-detection humanizer
  companion: ref_Chat-Behavior-No-AI-Voice.md
---

# Avoid AI Writing — Audit & Rewrite Skill

This skill audits content for AI writing patterns and either flags them,
rewrites them, or both. It is a post-draft tool. It runs on demand, not
in the background.

For always-on chat behavior rules, see the companion file:
`ref_Chat-Behavior-No-AI-Voice.md`

---

## How to Invoke This Skill

Trigger this skill when the user says any of the following:

- "audit this for AI tells"
- "remove AI-isms"
- "clean up AI writing"
- "make this sound less like AI"
- "humanize this"
- "check this draft"
- "flag the AI patterns"
- "detect only" / "just flag, don't rewrite"
- "scan this"

---

## Skill Files

Load these files in order when this skill is invoked.
Each file covers one area of the audit. Do not load all files at once
unless doing a full deep audit — load only what the task requires.

| File | Load when |
|---|---|
| `MODES.md` | Always — determines detect vs rewrite behavior |
| `RULES_HARD.md` | Always — hard bans, fix immediately |
| `RULES_SOFT.md` | Full audits, or when user asks for thorough review |
| `RULES_LEAVE_ALONE.md` | Always — protects human voice from over-editing |
| `PROFILES.md` | When content type is known (blog, email, docs, social, casual) |
| `MODEL_TELLS.md` | When user wants model-specific pattern detection |
| `OUTPUT_FORMAT.md` | Always — controls how results are presented |
| `EXAMPLES.md` | When user wants examples, or to verify flagged patterns |

---

## Quick-Start Rules

If you cannot load individual files, apply these core rules directly:

**Always fix:**
- Em dashes (— or --) — replace with comma, period, parentheses, or colon
- Chatbot filler: "Great question," "Certainly!" "I hope this helps"
- "It's not X, it's Y" contrastive reframing
- Self-posed questions answered immediately: "The result? Better outcomes."
- Hype language: game-changing, revolutionary, transformative, groundbreaking
- Generic wrap-ups: "The future looks bright," "Only time will tell"
- Fake-insight signposting: "Here's the thing," "Here's what people miss"

**Flag with judgment:**
- Stacked transitions: Additionally, Moreover, Furthermore in the same piece
- Tier 1 word clusters: delve, leverage, robust, seamless, pivotal, meticulous
- Over-uniform sentence and paragraph length
- Too many bullets in short text

**Never touch:**
- Regular hyphen used as separator - like this - it is human and intentional
- Normal inconsistency and rough edges
- Repeating the clearest word instead of forcing synonyms
- Deliberate fragments and personality quirks

---

## Severity Tiers

Prioritize fixes in this order:

**P0 — Fix immediately (credibility killers)**
- Chatbot artifacts: "Great question!" "I hope this helps!"
- Cutoff disclaimers: "As of my last update," "Based on available information"
- Vague unsourced attributions: "Experts believe," "Studies show"
- Significance inflation on routine events

**P1 — Fix before publishing (obvious AI smell)**
- Em dashes
- Tier 1 word list violations
- Contrastive reframing ("It's not X, it's Y")
- Fake-insight signposting
- "Let's" transition openers
- Formulaic openings ("In today's rapidly evolving world of...")
- Bold overuse

**P2 — Fix when time allows (stylistic polish)**
- Uniform paragraph and sentence length
- Stacked transitions
- Generic conclusions
- Rule-of-three overuse
- Copula avoidance (serves as, features, boasts)

---

## When to Rewrite vs Patch

**Patch individual phrases when:**
- Fewer than 5 P1 hits across the whole piece
- Structure and rhythm feel natural
- Issues are isolated word or phrase choices

**Recommend full rewrite when:**
- 5 or more P1 hits across multiple categories
- Uniform sentence and paragraph length throughout
- Structure itself feels AI-generated
- Patching phrases would leave the rhythm untouched

When recommending a full rewrite, say so directly:
"The structure itself reads as AI-generated. Patching phrases won't fix it.
State the core point in one sentence, then rebuild from there."

---

## Core Principle

The goal is writing that sounds like a specific person wrote it.
Not "a real person" in general. A specific person, in this context,
saying it this way.

Direct. Specific. Confident without asserting confidence.
Vary the rhythm. Have an opinion. Leave some human mess intact.

Over-editing toward perfection pushes writing back toward AI statistical
profiles. Natural disfluency, uneven pacing, and idiosyncratic word
choices are what keep text human. Do not sand them away.

---

*Version 1.0.0 — April 2026*
*Companion: ref_Chat-Behavior-No-AI-Voice.md (always-on chat behavior)*
*Next: MODES.md*
