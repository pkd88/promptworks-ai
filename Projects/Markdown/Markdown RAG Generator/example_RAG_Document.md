---
prefix: example_
priority: 13
authority: medium
filename: example_RAG_Document.md
version: 1.0
updated: 2026-04-19
owner: Phil Dawson
keywords: [example, RAG, formatting, reference, MG, myasthenia gravis]
---

# example_RAG_Document

This is a filled-in example of a correctly formatted RAG-ready Prompt Works document. It uses Myasthenia Gravis medication safety as the topic. Use this as the reference when DAM Gem 3 or any other Gem produces a new document — output should match this structure exactly.

## 1.0 Index Map

This section tells the AI what is in this document and where authority lives. Read this before processing any other section.

| Section | What It Covers | Authority |
|---|---|---|
| 1.0 | Index Map — document steering wheel | Highest |
| 2.0 | Medications to Avoid — hard safety rules | High |
| 3.0 | Medications That Require Caution | Medium |
| 4.0 | How to Use This Document | High |

---

## 2.0 Medications to Avoid with Myasthenia Gravis

This section lists medications that are contraindicated for MG patients. These drugs can trigger or worsen a myasthenic crisis and should never be taken without direct physician approval.

### 2.1 Antibiotics

Certain antibiotics block neuromuscular transmission and are dangerous for MG patients. The following should be avoided unless no alternative exists.

- Fluoroquinolones — ciprofloxacin, levofloxacin
- Aminoglycosides — gentamicin, tobramycin
- Macrolides — azithromycin, erythromycin (use with caution)

### 2.2 Cardiovascular Drugs

Several heart medications interfere with nerve-muscle signaling. Always inform your cardiologist of your MG diagnosis before starting any new cardiac drug.

- Beta-blockers — propranolol, atenolol
- Calcium channel blockers — verapamil (high risk)
- Quinidine and procainamide

---

## 3.0 Medications That Require Caution

This section covers drugs that are not fully contraindicated but carry elevated risk for MG patients. These require close monitoring and physician awareness.

### 3.1 Psychiatric Medications

Some antipsychotics and mood stabilizers can worsen MG symptoms in higher doses. Lithium has documented cases of worsening weakness.

- Lithium — monitor closely
- Chlorpromazine — use lowest effective dose
- Phenytoin — may impair neuromuscular function

### 3.2 Pain Medications

Opioids cause respiratory depression which is already a risk in MG. Use the lowest effective dose with respiratory monitoring.

- Morphine — use with caution, monitor breathing
- Oxycodone — same precautions as morphine

---

## 4.0 How to Use This Document

This section explains how the MG Gem and other AI tools should apply this document. This is the authority statement for retrieval behavior.

When a user asks about a medication, the Gem must check Section 2 first. If the drug appears there, flag it immediately as contraindicated and recommend physician contact. If the drug appears in Section 3, flag it as requiring caution and recommend disclosure to their doctor. If the drug does not appear in either section, state that it is not on the known risk list but that MG patients should always disclose all medications to their neurologist.

This document does not replace medical advice. It is a reference tool to support informed conversations with healthcare providers.

---

*Owner: Phil Dawson | Prompt Works | 2026-04-19*
