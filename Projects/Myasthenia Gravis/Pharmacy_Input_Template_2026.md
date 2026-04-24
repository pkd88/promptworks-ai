# Pharmacy Input Template 2026

## Purpose
This file is **data only**.
It should NOT give instructions, rules, or advice.
It is only a clean place to store medicines, supplements, and related notes so the Gem can review them when prompted.

## Design Decision
- **Overall RAG** = clean MG medical knowledge base
- **Pharmacy file** = separate personal medicine list
- **Prompt logic** = done in the Gem instruction, not in this file

## Accepted Input Types
The Gem may receive medicine information from:
- Typed text
- Voice / spoken medicine names
- Photo of bottle or label
- PDF medication list
- Copied list from portal or pharmacy handout

## Normalized Medication List
Use one item per block.

### Entry 001
- Name:
- Generic name:
- Strength:
- Form: tablet / capsule / liquid / injection / nasal / patch / other
- Dose used:
- Frequency:
- Why taking it:
- Prescriber:
- Start date:
- Stop date:
- Status: current / stopped / unsure / as-needed
- Notes:

### Entry 002
- Name:
- Generic name:
- Strength:
- Form:
- Dose used:
- Frequency:
- Why taking it:
- Prescriber:
- Start date:
- Stop date:
- Status:
- Notes:

## Supplements
### Supplement 001
- Name:
- Ingredient:
- Strength:
- Frequency:
- Why taking it:
- Status: current / stopped / unsure / as-needed
- Notes:

## OTC and PRN
### OTC 001
- Name:
- Ingredient:
- Strength:
- Frequency:
- Why taking it:
- Status:
- Notes:

## Input Processing Notes
When med information is added from bottle photo, PDF, or speech, convert it into the normalized format above.
Keep uncertain fields blank instead of guessing.
Store exact label wording in Notes when useful.
