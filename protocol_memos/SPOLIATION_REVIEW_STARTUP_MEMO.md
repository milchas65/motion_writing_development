# Spoliation Motion Review - Startup Memo

**Date:** January 1, 2026
**Purpose:** Guide for reviewing spoliation sanctions motion packages using the expanded Motion Review Protocol

---

## Quick Start

**Session Start Prompt:**
```
Review Y:\LCP_v2.0\docs\MOTION_REVIEW_PROTOCOL.md and continue the spoliation motion package review process.
```

---

## Phased Document Review Process

### Step 1: Inventory First

Provide the folder path containing the motion documents. Claude will:
- List all contents (files and subfolders)
- Create an inventory in the protocol file
- NOT read the documents yet

### Step 2: Review in Motion Lifecycle Order

Documents are reviewed one at a time in this sequence:

| Order | Document | What to Extract |
|-------|----------|-----------------|
| 1 | Notice of Motion | Relief sought, return date, procedural elements |
| 2 | Attorney Affirmation (moving) | Exhibit authentication, procedural recitals |
| 3 | Substantive Affidavit(s) (moving) | Facts establishing spoliation elements |
| 4 | Memorandum of Law in Support | Writing style, argument structure, case citations |
| 5 | Opposition Affirmation | Counter-evidence, procedural responses |
| 6 | Counter-Affidavit(s) | Defense facts, good faith explanations |
| 7 | Memorandum in Opposition | Defense strategies, case distinctions |
| 8 | Reply Affirmation (if any) | Rebuttal evidence |
| 9 | Reply Memorandum (if any) | Rebuttal arguments, narrowing issues |
| 10 | Court Decision/Order | What court found persuasive, outcome |

### Step 3: Extract → Save → Clear

After each document:
1. **Extract insights** across all 4 categories:
   - Motion Arc (structure, lifecycle)
   - Case Law Effectiveness (which cases worked)
   - Writing Style (language, structure, tone)
   - Strategy (what won/lost)

2. **Save to protocol file** under `PENDING_INSIGHTS`

3. **Move to next document**

### Step 4: Integrate in Batches

After completing the full package (or when insights accumulate):
- Read target instruction file
- Add insights in appropriate location
- Mark as `INTEGRATED` in protocol

---

## Four Insight Categories

| Category | Destination File | What to Capture |
|----------|------------------|-----------------|
| **Motion Arc** | `MOTION_ARC.md` | Required components, timeline, court analysis structure |
| **Case Law** | `CASE_LAW_EFFECTIVENESS.md` | Which cases won/lost, how distinguished |
| **Writing Style** | `*_master.md`, `argument_instructions.md` | Language patterns, structure, tone |
| **Strategy** | `STRATEGY_GUIDE.md` | Winning arguments, common mistakes, evidence that mattered |

---

## Information to Provide for Each Motion Package

Before beginning review of a new motion package, provide:

1. **Folder path**
   - Example: `Y:\resources\spoliation_cases\case_name\`

2. **Brief case description:**
   - Type of spoliation (ESI, video, documents, physical evidence)
   - Jurisdiction (NY State or Federal)
   - Result (sanctions granted/denied/partial)
   - Any notable features

---

## File Locations

### Protocol File
```
Y:\LCP_v2.0\docs\MOTION_REVIEW_PROTOCOL.md
```

### Instruction Files (Spoliation Sanctions)
```
Y:\LCP_v2.0\program_files\instructions\brief_drafting\spoliation_sanctions\
├── MOTION_ARC.md
├── CASE_LAW_EFFECTIVENESS.md
├── STRATEGY_GUIDE.md
├── motion\
│   ├── spoliation_motion_master.md
│   ├── argument_instructions.md
│   └── statement_of_facts_instructions.md
├── opposition\
│   ├── spoliation_opposition_master.md
│   ├── argument_instructions.md
│   └── counter_statement_instructions.md
└── reply\
    └── reply_brief_instructions.md
```

---

## Context Management

To prevent context exhaustion:

- **One document at a time** - Don't try to read multiple documents simultaneously
- **One motion package per session** - Complete full package before starting next
- **Extract, don't transcribe** - Capture insights, not full text
- **Save progress frequently** - Update protocol file before session ends
- **Resume, don't restart** - Check protocol file first each session

---

## Ready to Begin

When ready to start reviewing a spoliation motion package:

1. Provide folder path
2. Provide brief case description
3. Claude will inventory documents
4. Begin sequential review

---
