ref_Markdown_RAG_Standard

Version: 2.1 | Updated: 2026-04-29 | Owner: Phil Dawson Purpose: The single source of truth for how every RAG document is structured, cited, and labeled at Prompt Works. Applies to: All RAG files for MG Gem, SWM, NotebookLM notebooks, and any future RAG project.

THE CORE RULES

One topic per file

Clean heading structure — H1 title, H2 sections, H3 sub-sections only if needed

Short summary after every heading (1–3 sentences)

One idea per paragraph or bullet — no walls of text

[REF-01] anchors inline after factual sentences

References section at the bottom of every file

Front matter block at the top of every file

Domain tag in every heading that contains domain-specific content

FRONT MATTER BLOCK

Every file starts with this block, immediately after the H1 title.

**Domain:** [MED / PHARM / TRIAGE / MAKE / EXCEL / GENERAL] **SME:** [Name and role, or "Not yet reviewed"] **Use:** [Internal only / Client-facing / Gem context] **Last reviewed:** YYYY-MM-DD 

HEADING STRUCTURE

# File Title — One Topic Only **Domain:** MED **SME:** Dr. X, Emergency Physician **Use:** Internal only — MG Gem context **Last reviewed:** 2026-04-29 --- ## [MED] Section Title Short summary of this section. 1–3 sentences. What is this about and why does it matter. Content goes here. Each factual claim gets a citation anchor. [REF-01] ### Sub-section if needed Summary of sub-section. More content. [REF-02] 

CITATION ANCHORS

Format

[REF-01] — simple, sequential, universal. Same format in every file across every project.

Placement

Inline, immediately after the factual sentence it supports.

Mestinon controls muscle weakness by blocking acetylcholinesterase. [REF-01] Heat and overexertion are primary triggers for MG flares. [REF-02] 

What the anchor is NOT

Not a category code — [MG-MED-01] adds no retrieval value

Not a hyperlink

Not generated at retrieval time — it is written into the document during creation

Why simple works

The retrieval system reads the surrounding natural language, not the anchor text. The anchor is a stable audit ID, not a semantic signal. Domain context comes from the heading tag, not the citation.

DOMAIN TAGS IN HEADINGS

When a section contains domain-specific content, prefix the heading with the domain tag.

TagDomain[MED]Medical — clinical information[PHARM]Pharmacy — medications, dosing, interactions[TRIAGE]Emergency triage — what to tell EMS/ER[MAKE]Make.com automation[EXCEL]Excel / Power Query[GENERAL]No specific domain 

Example:

## [MED] MG crisis red-flag symptoms ## [PHARM] MG medication interactions ## [TRIAGE] What to tell EMS and ER staff 

Mixed-domain files use the tag per heading. Single-domain files declare domain in front matter and can omit per-heading tags.

REFERENCES SECTION

Every file ends with a References section mapping each anchor to its real source.

--- ## References [REF-01] MGFA Myasthenia Gravis Treatment Guideline 2024, sec. 3.2 — Medical SME reviewed 2026-03-10. [REF-02] Hospital MG Dosing Protocol v5 — Pharmacy SME reviewed 2026-02-18. [REF-03] Make.com official docs — Webhooks module, accessed 2026-04-15. 

Reference entry format

[REF-XX] Source name, section if relevant — SME role and review date.

Real source name — not the filename of the stored .md file.

COMPLETE EXAMPLE

# MG Acute Care — Crisis Recognition **Domain:** MED / TRIAGE **SME:** Dr. A, Emergency Physician **Use:** Internal only — MG Gem context **Last reviewed:** 2026-04-29 --- ## [MED] What a myasthenic crisis looks like A myasthenic crisis is a rapid worsening of muscle weakness that affects breathing. It is a medical emergency requiring immediate intervention. [REF-01] Key signs: - Difficulty breathing or speaking - Rapidly worsening limb weakness - Inability to swallow or protect airway [REF-01] ## [TRIAGE] What to tell EMS and ER staff Tell EMS the patient has myasthenia gravis. [REF-02] This affects which medications are safe — some common drugs worsen MG severely. [REF-03] Give them the patient's current medication list immediately. ## [PHARM] Drugs to avoid in MG crisis Several common medications can precipitate or worsen a myasthenic crisis. [REF-03] Known high-risk drugs include fluoroquinolone antibiotics, magnesium, and some cardiac medications. Always verify with pharmacy before administration. [REF-03] --- ## References [REF-01] MGFA Clinical Guidance — Myasthenic Crisis Recognition, 2024 — Medical SME reviewed 2026-04-01. [REF-02] EMS MG Protocol, Regional Hospital System — Triage SME reviewed 2026-03-15. [REF-03] Hospital MG Medication Safety List v3 — Pharmacy SME reviewed 2026-02-20. 

WHAT AI MUST DO TO PREPARE A RAG DOCUMENT

Raw content does not arrive RAG-ready. Every document requires three passes:

Pass 1 — Structure

Set H1 title (one topic)

Build H2/H3 heading structure

Add domain tags to headings

Write front matter block

Pass 2 — Summaries

Write 1–3 sentence summary under each heading

Break long paragraphs into short focused chunks

Convert walls of text to bullets where appropriate

Pass 3 — Citations

Add [REF-XX] anchors inline after factual claims

Build References section at bottom

Verify reference entries point to real sources, not filenames

These three passes map directly to the three-Gem pipeline.

WHAT THIS STANDARD DOES NOT COVER

Vector database setup

Chunking strategy (handled by the retrieval system)

Embedding model selection

NotebookLM upload process

This standard covers document preparation only — what goes into the file before it enters any RAG system.

Confirmed against PPX research 2026-04-29 Replaces ref_Markdown_RAG_Standard v2.0

