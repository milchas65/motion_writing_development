# Rule 56.1 / 19-a Statement Review Protocol

**Purpose:** Systematically review real attorney-drafted Rule 56.1 (Federal) and Rule 19-a (NY) Statements to improve LCP's statement generation quality.

**Session Start Prompt:**
```
Review Y:\LCP_v2.0\docs\RULE_56_STATEMENT_REVIEW_PROTOCOL.md and continue the Rule 56.1 statement review process.
```

---

## QUICK START (For New Sessions)

1. Read this file
2. Check `REVIEW_PROGRESS` section below for current status
3. Check `PENDING_INSIGHTS` section for insights awaiting integration
4. Either:
   - **Integrate pending insights** into instruction files (if any pending), OR
   - **Review next unreviewed statement** from the queue

---

## LOCATIONS

**Statements to Review:**
```
Y:\resources\unprocessed_document_library\documents_by_case\
```

**Instruction Files to Update:**
```
Y:\LCP_v2.0\program_files\instructions\brief_drafting\sj_motion\
  - statement_of_facts_instructions.md

Y:\LCP_v2.0\program_files\instructions\brief_drafting\sj_opposition\
  - counter_statement_instructions.md
```

---

## DOCUMENT TYPES

### Movant's Statement (Rule 56.1(a) / Rule 19-a)
- Filed by party moving for summary judgment
- Numbered paragraphs of material facts
- Each fact supported by citation to admissible evidence
- Goal: Establish undisputed facts entitling movant to judgment

### Opponent's Counter-Statement (Rule 56.1(b) / Rule 19-a Response)
- Filed by party opposing summary judgment
- Responds paragraph-by-paragraph to movant's statement
- Admits, denies, or qualifies each fact with citations
- May include additional material facts

### Reply Statement (if permitted)
- Responds to opponent's counter-statement
- Addresses purported disputes
- May respond to additional facts

---

## KEY DIFFERENCES: Federal vs NY

| Aspect | Federal (Local Rule 56.1) | NY (Commercial Division Rule 19-a) |
|--------|---------------------------|-------------------------------------|
| **Rule** | Local Rule 56.1 (varies by district) | 22 NYCRR 202.70(g), Rule 19-a |
| **Paragraph Limit** | Often 25 (S.D.N.Y.) | Typically no limit |
| **Deemed Admitted** | Uncontroverted facts deemed admitted | Uncontroverted facts deemed admitted |
| **Citation Required** | Yes - to admissible evidence | Yes - to admissible evidence |
| **Separate Document** | Yes - filed separately from memo | Yes - filed separately from memo |
| **Counter-Statement** | Required to controvert | Required to controvert |

---

## REVIEW WORKFLOW

### Step 1: Select Next Statement
- Check STATEMENT_QUEUE below for next unreviewed document
- Read the PDF (use Read tool on the file path)
- Note document type (Movant's Statement, Counter-Statement, or Reply)

### Step 2: Extract Insights (While Reading)
Capture specific, actionable observations in these categories:

| Category | What to Look For |
|----------|------------------|
| **FORMAT** | Numbering style, paragraph structure, caption format, heading conventions |
| **FACT_DRAFTING** | How facts are phrased, specificity level, avoiding conclusions/argument |
| **CITATION_PRACTICE** | Exhibit references, deposition cites (page:line), affidavit paragraph cites |
| **EVIDENCE_TYPES** | Deposition transcripts, documents, affidavits, interrogatory answers, admissions |
| **COUNTER_STATEMENT** | Admit/deny language, how disputes are framed, citation to contrary evidence |
| **ADDITIONAL_FACTS** | How opponent's additional facts are structured, strategic placement |
| **JURISDICTION_SPECIFIC** | NY vs Federal formatting differences, local rule compliance |
| **MATERIALITY** | How facts are tied to legal elements, avoiding immaterial facts |

### Step 3: Record Insights
Add to `PENDING_INSIGHTS` section below with:
- Statement identifier
- Category
- Specific insight (quote examples when possible)
- Which instruction file should be updated

### Step 4: Update This File
- Move statement from QUEUE to COMPLETED
- Save pending insights
- Note session end point

### Step 5: Integrate Insights (Same or Next Session)
When pending insights accumulate (3-5+):
- Read the target instruction file
- Add the insight in appropriate location
- Mark insight as INTEGRATED below

---

## STATEMENT-SPECIFIC REVIEW FOCUS

### For Movant's Statements
- How are facts numbered and organized?
- What level of specificity is used (dates, amounts, names)?
- How are record citations formatted?
- Are facts purely factual or do they creep into argument/conclusions?
- How are facts grouped thematically?
- How is each legal element supported by specific facts?

### For Counter-Statements
- What language is used to admit facts? ("Admitted." / "Undisputed." / "Not disputed.")
- What language is used to deny facts? ("Denied." / "Disputed." / "Controverted.")
- How are partial admissions phrased? ("Admitted in part; denied in part.")
- How are contrary citations introduced?
- How are objections to form/admissibility noted?
- How are additional facts introduced and numbered?

### For Reply Statements
- How are purported disputes addressed?
- How is opponent's evidence characterized as insufficient?
- How are immaterial disputes dismissed?
- Response to additional facts?

---

## STATEMENT_QUEUE

### Movant's Statements (Rule 56.1(a) / Rule 19-a)
| Status | Case | File Path |
|--------|------|-----------|
| REVIEWED | Art Capital | `unprocessed_acb_v_bntb_docs/...STATEMENT_OF_MATERI_192.pdf` *(Movant's Statement, 8 pages, 39 ¶¶, loan participation case)* |
| REVIEWED | BofA v Prima | `unprocessed_bofa_v_prima_docs/...STATEMENT_OF_MATERI_14.pdf` *(Movant's Statement, 14 pages, 65 ¶¶, CDO/CMBS securitization)* |
| REVIEWED | BofA v Prima | `unprocessed_bofa_v_prima_docs/...STATEMENT_OF_MATERI_32.pdf` *(Combined: OZ Movant Statement 34 ¶¶ + Counter-Statement to Prima, 30 pages)* |
| REVIEWED | Hassan Ragab | `unprocessed_ragab/...STATEMENT_OF_MATERI_108.pdf` *(Movant's Statement, 19 pages, 55 ¶¶, LLC valuation/breach of fiduciary duty, BigLaw (Goodwin Procter))* |

### Counter-Statements (Rule 56.1(b) / Rule 19-a Response)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Add cases as identified] | |

### Reply Statements
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Add cases as identified] | |

---

## REVIEW_PROGRESS

### Completed Reviews
| Date | Statement | Reviewer | Insights Added |
|------|-----------|----------|----------------|
| 2025-12-30 | Art Capital STATEMENT_OF_MATERI_192 | Claude | 10 insights (format, fact drafting, citation, evidence, materiality) |
| 2025-12-30 | BofA v Prima STATEMENT_OF_MATERI_14 | Claude | 10 insights (thematic structure, block quotes, "no provision" pattern, collective citations) |
| 2025-12-30 | BofA v Prima STATEMENT_OF_MATERI_32 | Claude | 10 insights (3 movant patterns, 7 counter-statement patterns - FIRST COUNTER-STATEMENT REVIEWED) |
| 2025-12-30 | Hassan Ragab STATEMENT_OF_MATERI_108 | Claude | 10 insights (TOC, Roman numerals, deposition Q&A quotes, Bates numbers, opponent admissions) |

### Session Log
| Date | Session Notes |
|------|---------------|
| 2025-12-30 | Protocol created. 4 statements identified for review queue. |
| 2025-12-30 | Reviewed Art Capital Rule 19-a Statement (Doc 192). Movant's Statement by Defendant Bank (8 pages, 39 ¶¶). Loan participation case - 3 loans, failure to remit payments. Extracted 10 insights on format, fact drafting, citations, and organization. |
| 2025-12-30 | Integrated all 10 Art Capital insights into statement_of_facts_instructions.md: NY format, term definitions, contractual obligation pattern, negative facts, citation formats, footnotes, verified pleading admissions, parallel transaction pattern, extended quotes, element-tracking. |
| 2025-12-30 | Reviewed BofA v Prima Rule 19-a Statement (Doc 14). Movant's Statement by Prima Capital (14 pages, 65 ¶¶). Complex CDO/CMBS securitization case - trustee duties, Issuer Orders, payment distributions. Uses thematic subheadings, extensive block quotes, "no provision" pattern. Extracted 10 insights. |
| 2025-12-30 | Integrated all 10 BofA v Prima insights into statement_of_facts_instructions.md: formal introduction, thematic subheadings, multiple evidence source footnotes, collective citations, block quotes, "no provision" pattern, contract definitions, building block organization. |
| 2025-12-30 | Reviewed BofA v Prima Rule 19-a Statement (Doc 32). COMBINED DOCUMENT: OZ Movant's Statement (34 ¶¶, pages 1-9) + OZ Counter-Statement to Prima (pages 10-30). First counter-statement reviewed. CDO trustee cross-motions. Uses letter-numbered subheadings, General Responses section, paragraph-by-paragraph format. Extracted 10 insights (3 movant, 7 counter-statement). |
| 2025-12-30 | Integrated all 10 BofA v Prima #32 insights: 3 movant patterns → statement_of_facts_instructions.md (letter subheadings, "nowhere in definition", "does not state"); 7 counter-statement patterns → counter_statement_instructions.md (general responses, response format, response types, "refers the Court", correcting quotes, scope limitation, combined title). FIRST COUNTER-STATEMENT INTEGRATION. |
| 2025-12-30 | Reviewed Hassan Ragab Rule 19-a Statement (Doc 108). Movant's Statement by Defendants/Board (19 pages, 55 ¶¶). LLC valuation dispute - breach of fiduciary duty re: Performance Unit valuation. BigLaw filing (Goodwin Procter). Notable features: Table of Contents, Roman numeral sections, extensive deposition Q&A block quotes, Bates number citations, heavy use of opponent's admissions. Extracted 10 insights. |
| 2025-12-30 | Integrated all 10 Hassan Ragab #108 insights into statement_of_facts_instructions.md: Table of Contents, Roman numeral sections, affirmation exhibit bracketed descriptions, Bates numbers, deposition Q&A block quotes, "see also" cross-references, third-party business records, opponent's deposition admissions, "I do not recall" testimony pattern, element-by-element defense structure. QUEUE COMPLETE. |

---

## PENDING_INSIGHTS

### Awaiting Integration

*(No pending insights)*

---

## INTEGRATED_INSIGHTS

### Already Added to Instructions
| Date | Statement Source | Category | Target File | Summary |
|------|------------------|----------|-------------|---------|
| 2025-12-30 | Art Capital #192 | FORMAT | statement_of_facts_instructions.md | NY Rule 19-a format with introductory sentence |
| 2025-12-30 | Art Capital #192 | FACT_DRAFTING | statement_of_facts_instructions.md | Term definition pattern (parties, documents, evidence sources) |
| 2025-12-30 | Art Capital #192 | FACT_DRAFTING | statement_of_facts_instructions.md | Contractual obligation pattern ("Pursuant to [Agreement]...") |
| 2025-12-30 | Art Capital #192 | FACT_DRAFTING | statement_of_facts_instructions.md | Comprehensive negative fact pattern |
| 2025-12-30 | Art Capital #192 | CITATION_PRACTICE | statement_of_facts_instructions.md | Multiple source citation formats (combined citations) |
| 2025-12-30 | Art Capital #192 | CITATION_PRACTICE | statement_of_facts_instructions.md | Footnotes for definitions |
| 2025-12-30 | Art Capital #192 | EVIDENCE_TYPES | statement_of_facts_instructions.md | Verified pleading admissions technique |
| 2025-12-30 | Art Capital #192 | STRUCTURE | statement_of_facts_instructions.md | Parallel transaction pattern |
| 2025-12-30 | Art Capital #192 | FACT_DRAFTING | statement_of_facts_instructions.md | Extended quotes with written-out dollar amounts |
| 2025-12-30 | Art Capital #192 | MATERIALITY | statement_of_facts_instructions.md | Element-tracking organization |
| 2025-12-30 | BofA v Prima #14 | FORMAT | statement_of_facts_instructions.md | Formal introduction with CPLR 3212/Rule 19-a legal standard |
| 2025-12-30 | BofA v Prima #14 | STRUCTURE | statement_of_facts_instructions.md | Thematic subheadings with numbered paragraphs |
| 2025-12-30 | BofA v Prima #14 | CITATION_PRACTICE | statement_of_facts_instructions.md | Footnotes defining multiple evidence sources |
| 2025-12-30 | BofA v Prima #14 | CITATION_PRACTICE | statement_of_facts_instructions.md | Collective citation for parallel documents |
| 2025-12-30 | BofA v Prima #14 | FACT_DRAFTING | statement_of_facts_instructions.md | Indented block quotes for contract provisions |
| 2025-12-30 | BofA v Prima #14 | FACT_DRAFTING | statement_of_facts_instructions.md | "No provision" negative pattern |
| 2025-12-30 | BofA v Prima #14 | CITATION_PRACTICE | statement_of_facts_instructions.md | Cite entire document for "no provision" facts |
| 2025-12-30 | BofA v Prima #14 | EVIDENCE_TYPES | statement_of_facts_instructions.md | Multiple diverse source combinations |
| 2025-12-30 | BofA v Prima #14 | FACT_DRAFTING | statement_of_facts_instructions.md | Quote contract definitions with parenthetical |
| 2025-12-30 | BofA v Prima #14 | STRUCTURE | statement_of_facts_instructions.md | Building block organization |
| 2025-12-30 | BofA v Prima #32 | STRUCTURE | statement_of_facts_instructions.md | Letter-numbered thematic subheadings (A., B., C.) |
| 2025-12-30 | BofA v Prima #32 | FACT_DRAFTING | statement_of_facts_instructions.md | "Nowhere in the definition" negative pattern |
| 2025-12-30 | BofA v Prima #32 | FACT_DRAFTING | statement_of_facts_instructions.md | "Does not state/contain" negative pattern |
| 2025-12-30 | BofA v Prima #32 | COUNTER_STATEMENT | counter_statement_instructions.md | General Responses section for overarching objections |
| 2025-12-30 | BofA v Prima #32 | COUNTER_STATEMENT | counter_statement_instructions.md | Paragraph-by-paragraph response format |
| 2025-12-30 | BofA v Prima #32 | COUNTER_STATEMENT | counter_statement_instructions.md | Response type patterns (undisputed, disputed, scope-limited) |
| 2025-12-30 | BofA v Prima #32 | COUNTER_STATEMENT | counter_statement_instructions.md | "Refers the Court" technique |
| 2025-12-30 | BofA v Prima #32 | COUNTER_STATEMENT | counter_statement_instructions.md | Correcting incomplete/selective quotes |
| 2025-12-30 | BofA v Prima #32 | COUNTER_STATEMENT | counter_statement_instructions.md | Scope limitation with alternative response |
| 2025-12-30 | BofA v Prima #32 | FORMAT | counter_statement_instructions.md | Combined Statement + Response title format |
| 2025-12-30 | Hassan Ragab #108 | FORMAT | statement_of_facts_instructions.md | Table of Contents for lengthy statements (50+ ¶¶) |
| 2025-12-30 | Hassan Ragab #108 | STRUCTURE | statement_of_facts_instructions.md | Roman numeral thematic sections (I., II., III.) |
| 2025-12-30 | Hassan Ragab #108 | CITATION_PRACTICE | statement_of_facts_instructions.md | Affirmation exhibit bracketed descriptions with Bates |
| 2025-12-30 | Hassan Ragab #108 | CITATION_PRACTICE | statement_of_facts_instructions.md | Bates number formats (RAGAB002610, P0040553) |
| 2025-12-30 | Hassan Ragab #108 | EVIDENCE_TYPES | statement_of_facts_instructions.md | Deposition Q&A block quotes (Q:/A: format) |
| 2025-12-30 | Hassan Ragab #108 | CITATION_PRACTICE | statement_of_facts_instructions.md | "See also" cross-references with parentheticals |
| 2025-12-30 | Hassan Ragab #108 | EVIDENCE_TYPES | statement_of_facts_instructions.md | Third-party business records (Sec. of State, NACVA) |
| 2025-12-30 | Hassan Ragab #108 | FACT_DRAFTING | statement_of_facts_instructions.md | Opponent's deposition admissions pattern |
| 2025-12-30 | Hassan Ragab #108 | FACT_DRAFTING | statement_of_facts_instructions.md | "I do not recall" testimony for establishing negatives |
| 2025-12-30 | Hassan Ragab #108 | MATERIALITY | statement_of_facts_instructions.md | Element-by-element defense structure |

---

## STATEMENT FORMATTING REFERENCE

### Movant's Statement Format (Federal)
```
STATEMENT OF UNDISPUTED MATERIAL FACTS
PURSUANT TO LOCAL RULE 56.1

1. On [date], [party] [action]. (Ex. A at 1; Smith Dep. 23:4-15.)

2. [Party] is a [description]. (Compl. ¶ 3; Answer ¶ 3.)

3. The [document] provides that "[quoted language]." (Ex. B at 4.)

...
```

### Movant's Statement Format (NY Commercial Division)
```
STATEMENT OF MATERIAL FACTS NOT IN DISPUTE
PURSUANT TO COMMERCIAL DIVISION RULE 19-a

1. [Fact]. (Citation to Record.)

2. [Fact]. (Citation to Record.)

...
```

### Counter-Statement Format
```
COUNTER-STATEMENT OF MATERIAL FACTS
PURSUANT TO LOCAL RULE 56.1(b)

1. Admitted.

2. Denied. The [correct fact] is [X]. (Ex. C at 2; Jones Dep. 45:10-20.)

3. Admitted in part; denied in part. It is admitted that [X]. It is denied
   that [Y]. (Ex. D at 3.)

4. The statement contains argument and conclusions of law to which no
   response is required. To the extent a response is required, denied.

STATEMENT OF ADDITIONAL MATERIAL FACTS

5. [Additional fact favorable to opponent]. (Citation to Record.)

6. [Additional fact favorable to opponent]. (Citation to Record.)

...
```

---

## COMMON CITATION FORMATS

### Deposition Citations
```
(Smith Dep. 23:4-15.)
(Deposition of John Smith, dated Jan. 5, 2024 ("Smith Dep."), at 23:4-15.)
(Smith Dep. Tr. at 23:4-15, annexed as Ex. A.)
```

### Exhibit Citations
```
(Ex. A.)
(Ex. A at 3.)
(Ex. A, p. 3.)
(Plaintiff's Ex. A at 3.)
```

### Affidavit Citations
```
(Smith Aff. ¶ 5.)
(Affidavit of John Smith, sworn to Jan. 5, 2024 ("Smith Aff."), ¶ 5.)
```

### Pleading Citations
```
(Compl. ¶ 12.)
(Answer ¶ 12.)
(Counterclaim ¶ 5.)
```

### Interrogatory/Admission Citations
```
(Pl.'s Resp. to Interrog. No. 5.)
(Def.'s Resp. to Req. for Admis. No. 3.)
```

---

## BEST PRACTICES TO CAPTURE

### Effective Fact Drafting
- One discrete fact per paragraph
- Specific dates, amounts, names (not "approximately" or "various")
- Direct quotes from key documents
- Avoid characterization or argument
- Chronological or thematic organization

### Effective Counter-Statement Practice
- Never ignore a paragraph (deemed admission risk)
- Object to form when appropriate, but still respond
- Cite to specific contrary evidence
- Additional facts should fill gaps, not repeat denials

### Common Deficiencies to Avoid
- Argumentative facts ("Defendant wrongfully...")
- Compound facts (multiple facts in one paragraph)
- Missing citations
- Vague citations ("the record shows...")
- Legal conclusions disguised as facts
- Immaterial facts that don't support any element

---

## CONTEXT MANAGEMENT RULES

To prevent context exhaustion:

1. **One statement per session focus** - Don't try to review multiple statements
2. **Extract, don't transcribe** - Capture the insight, not the full text
3. **Incremental updates** - Small additions to instruction files, not rewrites
4. **Save progress frequently** - Update this file before session ends
5. **Resume, don't restart** - Check this file first, continue from where left off

---

## END OF PROTOCOL
