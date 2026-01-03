# SJ Brief Review Protocol

**Purpose:** Systematically review real attorney-drafted Summary Judgment briefs to improve LCP's brief generation quality.

**Session Start Prompt:**
```
Review Y:\LCP_v2.0\docs\SJ_BRIEF_REVIEW_PROTOCOL.md and continue the SJ brief review process.
```

---

## QUICK START (For New Sessions)

1. Read this file
2. Check `REVIEW_PROGRESS` section below for current status
3. Check `PENDING_INSIGHTS` section for insights awaiting integration
4. Either:
   - **Integrate pending insights** into instruction files (if any pending), OR
   - **Review next unreviewed brief** from the queue

---

## LOCATIONS

**Briefs to Review:**
```
Y:\resources\unprocessed_document_library\documents_by_case\
```

**Instruction Files to Update:**
```
Y:\LCP_v2.0\program_files\instructions\brief_drafting\sj_motion\
  - sj_motion_master.md
  - argument_instructions.md
  - statement_of_facts_instructions.md

Y:\LCP_v2.0\program_files\instructions\brief_drafting\sj_opposition\
  - sj_opposition_master.md
  - argument_instructions.md
  - counter_statement_instructions.md

Y:\LCP_v2.0\program_files\instructions\brief_drafting\sj_reply\
  - reply_brief_instructions.md
```

---

## KEY DIFFERENCES: SJ vs MTD

| Aspect | Motion to Dismiss | Summary Judgment |
|--------|-------------------|------------------|
| **Standard** | Failure to state a claim | No genuine issue of material fact |
| **Factual Basis** | Allegations in pleading | Evidence in record |
| **Key Document** | Complaint | Statement of Undisputed Material Facts |
| **Burden** | Plaintiff must state plausible claim | Movant must show no material fact dispute |
| **NY Rule** | CPLR 3211 | CPLR 3212 |
| **Federal Rule** | FRCP 12(b)(6) | FRCP 56 |
| **Evidence** | Documents integral to complaint | Affidavits, depositions, admissions, interrogatories |

---

## REVIEW WORKFLOW

### Step 1: Select Next Brief
- Check BRIEF_QUEUE below for next unreviewed brief
- Read the PDF (use Read tool on the file path)
- Note: Focus on MEMORANDUM files, not notices, affidavits, or Rule 19-a Statements (review those separately)

### Step 2: Extract Insights (While Reading)
Capture specific, actionable observations in these categories:

| Category | What to Look For |
|----------|------------------|
| **STRUCTURE** | Section ordering, heading styles, SOF/CSOF format, transitions |
| **STATEMENT_OF_FACTS** | How undisputed facts are presented, numbered paragraph format, record citations |
| **ARGUMENT_TECHNIQUES** | Burden shifting, marshaling evidence, defeating factual disputes |
| **LANGUAGE_PATTERNS** | "Undisputed that...", "No reasonable jury could...", persuasive constructions |
| **CITATION_PRACTICE** | How record evidence is cited, deposition excerpts, exhibit references |
| **JURISDICTION_SPECIFIC** | NY vs Federal differences, local rules (Rule 19-a, Local Rule 56.1) |
| **EVIDENCE_HANDLING** | Affidavit structure, authenticating documents, expert testimony |

### Step 3: Record Insights
Add to `PENDING_INSIGHTS` section below with:
- Brief identifier
- Category
- Specific insight (quote examples when possible)
- Which instruction file should be updated

### Step 4: Update This File
- Move brief from QUEUE to COMPLETED
- Save pending insights
- Note session end point

### Step 5: Integrate Insights (Same or Next Session)
When pending insights accumulate (3-5+):
- Read the target instruction file
- Add the insight in appropriate location
- Mark insight as INTEGRATED below

---

## SJ-SPECIFIC REVIEW FOCUS

### For Motion Briefs (Movant Seeking SJ)
- How are undisputed facts organized and numbered?
- How is record evidence cited (Exhibit #, Deposition page:line)?
- How does movant establish prima facie case / negate element?
- How are burden-shifting arguments structured?
- How are opponent's potential factual disputes preemptively addressed?

### For Opposition Briefs (Opposing SJ)
- How are factual disputes identified and highlighted?
- Counter-statement format (admit/deny with citations)?
- How is additional evidence introduced?
- "Genuine issue" language and framing?
- Credibility and weight arguments (not for court to decide)?

### For Reply Briefs
- How are opponent's "sham" affidavits attacked?
- How are purported disputes shown to be immaterial?
- How is opponent's evidence characterized as insufficient?
- Addressing newly raised arguments?

---

## BRIEF_QUEUE

### Motion Briefs (Moving for Summary Judgment)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Add cases as identified] | |

### Combined Opposition/Cross-Motion Briefs
| Status | Case | File Path |
|--------|------|-----------|
| REVIEWED | BofA v Prima | `unprocessed_bofa_v_prima_docs/...MEMORANDUM_OF_LAW_I_15.pdf` *(Combined Opposition to MTD + Cross-Motion for SJ, 35 pages, CDO/CMBS securitization, BigLaw (Kasowitz))* |

### Opposition Briefs (Opposing Summary Judgment)
| Status | Case | File Path |
|--------|------|-----------|
| REVIEWED | Bay Crane | `unprocessed_bay_crane_docs/...MEMORANDUM_IN_OPPOS_50.pdf` *(Combined Opposition + Cross-Motion, 12 pages, construction lien case)* |
| REVIEWED | Art Capital | `unprocessed_acb_v_bntb_docs/...MEMORANDUM_IN_OPPOS_209.pdf` *(Opposition + Cross-Motion for Leave to Amend, 30 pages, loan participation case)* |
| REVIEWED | Ragab v SHR Capital | `unprocessed_ragab/...MEMORANDUM_OF_LAW_I_132.pdf` *(Opposition to Partial SJ, 27 pages, LLC breach of fiduciary duty, bad faith valuation, Delaware law)* |
| PENDING | [Add cases as identified] | |

### Reply Briefs
| Status | Case | File Path |
|--------|------|-----------|
| REVIEWED | BofA v Prima Doc 27 | `unprocessed_bofa_v_prima_docs/...MEMORANDUM_OF_LAW_I_27.pdf` *(Reply + SJ Opposition, 35 pages, CDO/CMBS interpleader, BigLaw (Mayer Brown))* |
| REVIEWED | BofA v Prima Doc 30 | `unprocessed_bofa_v_prima_docs/...MEMORANDUM_OF_LAW_30.pdf` *(SJ Motion + Opposition, 19 pages, CDO/CMBS interpleader, boutique (Schindler Cohen & Hochman))* |
| PENDING | [Add cases as identified] | |

### Rule 19-a / Local Rule 56.1 Statements
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Add cases as identified] | |

---

## REVIEW_PROGRESS

### Completed Reviews
| Date | Brief | Reviewer | Insights Added | Status |
|------|-------|----------|----------------|--------|
| 2025-12-30 | Bay Crane MEMORANDUM_IN_OPPOS_50 | Claude | 12 insights (structure, argument, language, citation, evidence) | INTEGRATED |
| 2025-12-30 | Art Capital MEMORANDUM_IN_OPPOS_209 | Claude | 10 insights (structure, argument, language, citation) | INTEGRATED |
| 2025-12-30 | BofA v Prima MEMORANDUM_OF_LAW_I_15 | Claude | 10 insights (structure, citation, language, argument) | INTEGRATED |
| 2025-12-31 | Ragab v SHR Capital MEMORANDUM_OF_LAW_I_132 | Claude | 10 insights (structure, language, argument, citation, evidence) | INTEGRATED |
| 2025-12-31 | BofA v Prima MEMORANDUM_OF_LAW_I_27 | Claude | 10 insights (structure, argument, language, citation) | INTEGRATED |
| 2025-12-31 | BofA v Prima MEMORANDUM_OF_LAW_30 | Claude | 10 insights (structure, argument, language, citation) | INTEGRATED |

### Session Log
| Date | Session Notes |
|------|---------------|
| 2025-12-30 | Protocol created. Ready to begin SJ brief reviews. |
| 2025-12-30 | Reviewed Bay Crane brief (Doc 50). Combined Opposition + Cross-Motion for SJ (12 pages). Construction lien case - "no lien fund" defense. Extracted 12 insights. |
| 2025-12-30 | Integrated all 12 Bay Crane insights into instruction files: sj_motion_master.md, sj_motion/argument_instructions.md, sj_opposition_master.md, sj_opposition/argument_instructions.md, sj_motion/statement_of_facts_instructions.md. |
| 2025-12-30 | Reviewed Art Capital brief (Doc 209). Opposition + Cross-Motion for Leave to Amend (30 pages). Loan participation case - procedural bar, conditional tender, material breach defenses. Extracted 10 insights. |
| 2025-12-30 | Integrated all 10 Art Capital insights into instruction files: sj_opposition_master.md (3), sj_opposition/argument_instructions.md (7), sj_motion_master.md (1), statement_of_facts_instructions.md (1). |
| 2025-12-30 | Reviewed BofA v Prima brief (Doc 15). Combined Opposition to MTD + Cross-Motion for Dismissal and SJ (35 pages). CDO/CMBS interpleader case. BigLaw filing (Kasowitz). Notable features: Table of Authorities, dual legal standards section, extensive footnotes defining citation shorthands, "It is undisputed that..." framing. Extracted 10 insights. |
| 2025-12-31 | Verified all 10 BofA v Prima insights already integrated into instruction files. Moved insights from PENDING to INTEGRATED. Protocol file updated. Ready for next brief review. |
| 2025-12-31 | Reviewed Ragab v SHR Capital brief (Doc 132). Opposition to Partial SJ (27 pages). LLC breach of fiduciary duty case - bad faith valuation, Delaware law. Notable features: numbered catalogue of bad faith evidence, text message evidence with profanity showing true intent, expert report attack, "freeze out" narrative, word count certification. Extracted 10 insights. |
| 2025-12-31 | Integrated all 10 Ragab v SHR Capital insights into instruction files: sj_opposition/argument_instructions.md (9 insights), sj_opposition_master.md (1 insight - word count certification). |
| 2025-12-31 | Reviewed BofA v Prima Doc 27. Reply Memorandum + SJ Opposition (35 pages). BigLaw filing (Mayer Brown). Combined: Reply to MTD + Opposition to Cross-Motion for SJ. Notable features: Reply brief SOF cross-reference technique, argumentative lettered subheadings, "concession by silence" argument, Section VI dedicated to SJ denial grounds. Extracted 10 insights. |
| 2025-12-31 | Integrated all 10 BofA v Prima Doc 27 insights into instruction files: reply_brief_instructions.md (2: SOF cross-reference, concession by silence), sj_opposition_master.md (1: dedicated SJ opposition section), sj_opposition/argument_instructions.md (6: withdrawn offer, dual grounds, threshold framing, enumeration, turning cases, inconsistent conduct footnote). Note: Insight 2 (argumentative lettered subheadings) already covered in sj_motion_master.md under "Persuasive Background Subheadings". |
| 2025-12-31 | Reviewed BofA v Prima Doc 30. SJ Motion + Opposition (19 pages). Boutique firm filing (Schindler Cohen & Hochman) representing OZ Master Fund/Goldman Sachs entities. Third perspective on same CDO case. Notable features: "crux of dispute" opening, exposing opponent's economic motivation, contract block quote saturation, enumerated relief in conclusion. Extracted 10 insights. |
| 2026-01-01 | Verified all 10 BofA v Prima Doc 30 insights already integrated into instruction files: sj_motion_master.md (6 insights: crux of dispute, economic motivation, nothing remotely suggests, block quote saturation, points to no language, enumerated relief, at minimum impact list), sj_opposition/argument_instructions.md (4 insights: economic motivation, both meritless, contrary to contention, procedural bar). Moved from PENDING to INTEGRATED. Protocol current. |

---

## PENDING_INSIGHTS

### Awaiting Integration

*(No pending insights - all current insights have been integrated)*

---

## INTEGRATED_INSIGHTS

### Already Added to Instructions
| Date | Brief Source | Category | Target File | Summary |
|------|--------------|----------|-------------|---------|
| 2025-12-30 | Bay Crane #50 | STRUCTURE | sj_motion_master.md, sj_opposition_master.md | Combined Opposition + Cross-Motion brief title format |
| 2025-12-30 | Bay Crane #50 | STRUCTURE | sj_opposition_master.md | Narrative Statement of Facts format for combined briefs |
| 2025-12-30 | Bay Crane #50 | ARGUMENT_TECHNIQUES | sj_motion/argument_instructions.md | "No Fund to Attach" defense for derivative claims |
| 2025-12-30 | Bay Crane #50 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Attack opponent's failure to address essential element |
| 2025-12-30 | Bay Crane #50 | ARGUMENT_TECHNIQUES | sj_motion/argument_instructions.md, sj_opposition/argument_instructions.md | Use recent analogous trial court decisions |
| 2025-12-30 | Bay Crane #50 | ARGUMENT_TECHNIQUES | sj_motion/argument_instructions.md | Offset/completion cost defense |
| 2025-12-30 | Bay Crane #50 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Personal knowledge attack (Point II pattern) |
| 2025-12-30 | Bay Crane #50 | LANGUAGE_PATTERNS | sj_motion_master.md, sj_opposition_master.md | "has not proven, nor can it prove" language |
| 2025-12-30 | Bay Crane #50 | LANGUAGE_PATTERNS | sj_motion_master.md | "Based upon undisputed facts" attribution |
| 2025-12-30 | Bay Crane #50 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "Plaintiffs rely entirely on..." attack |
| 2025-12-30 | Bay Crane #50 | CITATION_PRACTICE | sj_motion_master.md | String cites with parallel parentheticals |
| 2025-12-30 | Bay Crane #50 | EVIDENCE_HANDLING | sj_motion/statement_of_facts_instructions.md | Corporate officer affidavit with specific figures |
| 2025-12-30 | Art Capital #209 | STRUCTURE | sj_opposition_master.md | Bulleted Preliminary Statement with case citations |
| 2025-12-30 | Art Capital #209 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Procedural bar as lead argument (Point I) |
| 2025-12-30 | Art Capital #209 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "Nothing to complain about" dismissive framing |
| 2025-12-30 | Art Capital #209 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | "No unconditional admission" defense |
| 2025-12-30 | Art Capital #209 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Failure to adduce proof of amounts attack |
| 2025-12-30 | Art Capital #209 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Material breach defense pattern |
| 2025-12-30 | Art Capital #209 | STRUCTURE | sj_opposition_master.md, statement_of_facts_instructions.md | Thematic subheadings in Statement of Facts |
| 2025-12-30 | Art Capital #209 | CITATION_PRACTICE | sj_motion_master.md | Parenthetical explanations for key holdings |
| 2025-12-30 | Art Capital #209 | ARGUMENT_TECHNIQUES | sj_opposition_master.md | Cross-motion for leave to amend combined with opposition |
| 2025-12-30 | Art Capital #209 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "At a minimum" fallback position |
| 2025-12-31 | BofA v Prima #15 | STRUCTURE | sj_opposition_master.md | Combined MTD Opposition + Cross-Motion title format (three procedural postures) |
| 2025-12-31 | BofA v Prima #15 | STRUCTURE | sj_motion_master.md | Table of Authorities with categorized sections (Cases, Statutes, Other) |
| 2025-12-31 | BofA v Prima #15 | STRUCTURE | sj_opposition_master.md | Dual Legal Standards section (MTD + SJ standards in one section) |
| 2025-12-31 | BofA v Prima #15 | CITATION_PRACTICE | sj_motion_master.md | Footnotes defining multiple citation shorthands early in brief |
| 2025-12-31 | BofA v Prima #15 | CITATION_PRACTICE | sj_motion_master.md | Combined SMF + documentary citations pattern |
| 2025-12-31 | BofA v Prima #15 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "It is undisputed that..." affirmative framing |
| 2025-12-31 | BofA v Prima #15 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | "without merit" dismissive transition |
| 2025-12-31 | BofA v Prima #15 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Opponent's conduct contradicts claimed position |
| 2025-12-31 | BofA v Prima #15 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "At the very least" escalating fallback argument |
| 2025-12-31 | BofA v Prima #15 | STRUCTURE | sj_motion/statement_of_facts_instructions.md | Narrative letter subheadings with argumentative framing |
| 2025-12-31 | Ragab v SHR #132 | STRUCTURE | sj_opposition/argument_instructions.md | Numbered catalogue of bad faith evidence with (1)-(10) format |
| 2025-12-31 | Ragab v SHR #132 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "The record shows just the opposite" turnabout |
| 2025-12-31 | Ragab v SHR #132 | EVIDENCE_HANDLING | sj_opposition/argument_instructions.md | Text message/informal communication evidence showing true intent |
| 2025-12-31 | Ragab v SHR #132 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Expert report attack enumerating specific errors |
| 2025-12-31 | Ragab v SHR #132 | STRUCTURE | sj_opposition_master.md | Commercial Division word count certification (Rule 202.8-b) |
| 2025-12-31 | Ragab v SHR #132 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Waiver footnote attack |
| 2025-12-31 | Ragab v SHR #132 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "Freeze out" narrative framing for exclusion pattern |
| 2025-12-31 | Ragab v SHR #132 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Turning opponent's cited cases against them |
| 2025-12-31 | Ragab v SHR #132 | CITATION_PRACTICE | sj_opposition/argument_instructions.md | Delaware Chancery LLC fiduciary duty citations |
| 2025-12-31 | Ragab v SHR #132 | EVIDENCE_HANDLING | sj_opposition/argument_instructions.md | Deposition discomfort as evidence of wrongdoing |
| 2025-12-31 | BofA v Prima #27 | STRUCTURE | sj_reply/reply_brief_instructions.md | Reply Brief SOF Cross-Reference technique |
| 2025-12-31 | BofA v Prima #27 | ARGUMENT_TECHNIQUES | sj_reply/reply_brief_instructions.md | "Concession by Silence" reply argument |
| 2025-12-31 | BofA v Prima #27 | STRUCTURE | sj_opposition_master.md | Dedicated SJ Opposition Section in combined briefs |
| 2025-12-31 | BofA v Prima #27 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Using Opponent's Withdrawn Offer Against Them |
| 2025-12-31 | BofA v Prima #27 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Dual Independent Grounds for SJ Denial |
| 2025-12-31 | BofA v Prima #27 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | "As an initial matter" threshold framing |
| 2025-12-31 | BofA v Prima #27 | LANGUAGE_PATTERNS | sj_opposition/argument_instructions.md | Structured Enumeration of Contract/Agreement Flaws |
| 2025-12-31 | BofA v Prima #27 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Turning Opponent's Cases Against Them (extended with misapplied cases variant) |
| 2025-12-31 | BofA v Prima #27 | CITATION_PRACTICE | sj_opposition/argument_instructions.md | Footnote Documenting Opponent's Inconsistent Conduct |
| 2026-01-01 | BofA v Prima #30 | LANGUAGE_PATTERNS | sj_motion_master.md | "Crux of the Dispute" opening framing |
| 2026-01-01 | BofA v Prima #30 | ARGUMENT_TECHNIQUES | sj_motion_master.md, sj_opposition/argument_instructions.md | Exposing Opponent's Economic Motivation |
| 2026-01-01 | BofA v Prima #30 | LANGUAGE_PATTERNS | sj_motion_master.md | "Nothing in [Document] Even Remotely Suggests" dismissive language |
| 2026-01-01 | BofA v Prima #30 | CITATION_PRACTICE | sj_motion_master.md | Contract Block Quote Saturation |
| 2026-01-01 | BofA v Prima #30 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | "Both arguments are meritless" collective dismissal |
| 2026-01-01 | BofA v Prima #30 | ARGUMENT_TECHNIQUES | sj_motion_master.md | Preemptive "Points to No Language" Attack |
| 2026-01-01 | BofA v Prima #30 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | "Contrary to [Opponent]'s Contention" Direct Rebuttal |
| 2026-01-01 | BofA v Prima #30 | STRUCTURE | sj_motion_master.md | Enumerated Relief Requests in Conclusion |
| 2026-01-01 | BofA v Prima #30 | ARGUMENT_TECHNIQUES | sj_opposition/argument_instructions.md | Procedural Bar for Unauthorized Action |
| 2026-01-01 | BofA v Prima #30 | LANGUAGE_PATTERNS | sj_motion_master.md | "Would, at a minimum" Enumerated Impact List |

---

## SJ LEGAL STANDARDS REFERENCE

### New York (CPLR 3212)
- Movant must make prima facie showing of entitlement to judgment as matter of law
- Must tender sufficient evidence to demonstrate absence of material factual issues
- Burden then shifts to opponent to produce evidentiary proof establishing triable issue
- "Shadowy semblance of an issue" insufficient to defeat motion

### Federal (FRCP 56)
- Movant must show no genuine dispute as to any material fact
- Court views evidence in light most favorable to non-movant
- Non-movant must go beyond pleadings and designate specific facts
- "Mere allegations or denials" insufficient to create genuine dispute

### Key Differences to Note
- NY: Movant has initial burden to affirmatively demonstrate entitlement
- Federal: Movant can satisfy burden by pointing to absence of evidence
- NY: "Drastic remedy" language more common
- Federal: *Celotex* trilogy framework

---

## STATEMENT OF FACTS FORMATS

### NY Practice (Rule 19-a Statement)
```
STATEMENT OF UNDISPUTED MATERIAL FACTS
PURSUANT TO COMMERCIAL DIVISION RULE 19-a

1. [Fact]. (Citation to Record)
2. [Fact]. (Citation to Record)
...
```

### Federal Practice (Local Rule 56.1 Statement)
```
STATEMENT OF UNDISPUTED MATERIAL FACTS
PURSUANT TO LOCAL RULE 56.1

1. [Fact]. (Citation to Record)
2. [Fact]. (Citation to Record)
...
```

### Counter-Statement Format
```
COUNTER-STATEMENT OF MATERIAL FACTS

1. Admitted.
2. Denied. [Contrary fact with citation].
3. Admitted in part; denied in part. [Explanation with citation].
...

ADDITIONAL MATERIAL FACTS

X. [Additional fact]. (Citation to Record)
...
```

---

## COMMON SJ ARGUMENT PATTERNS

### Motion Arguments
- Prima facie case established by [evidence]
- Plaintiff cannot establish element of [X]
- No evidence of [required element]
- Undisputed documentary evidence conclusively establishes
- Plaintiff's own testimony/admissions defeat claim

### Opposition Arguments
- Genuine issues of material fact preclude summary judgment
- Credibility determinations inappropriate at this stage
- Evidence must be viewed in light most favorable to non-movant
- Conflicting evidence creates triable issue
- Discovery not yet complete / Rule 56(d) continuance needed

### Reply Arguments
- Purported disputes are immaterial to outcome
- Opponent's evidence insufficient to create genuine issue
- Conclusory allegations cannot defeat motion
- Sham affidavit doctrine
- No new admissible evidence presented

---

## CONTEXT MANAGEMENT RULES

To prevent context exhaustion:

1. **One brief per session focus** - Don't try to review multiple briefs
2. **Extract, don't transcribe** - Capture the insight, not the full text
3. **Incremental updates** - Small additions to instruction files, not rewrites
4. **Save progress frequently** - Update this file before session ends
5. **Resume, don't restart** - Check this file first, continue from where left off

---

## END OF PROTOCOL
