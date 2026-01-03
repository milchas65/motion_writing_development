# OSC Brief Review Protocol

**Purpose:** Systematically review real attorney-drafted briefs both supporting and opposing Orders to Show Cause to improve LCP's brief generation quality for TRO/preliminary injunction practice.

**Session Start Prompt:**
```
Review Y:\LCP_v2.0\docs\OSC_OPPOSITION_BRIEF_REVIEW_PROTOCOL.md and continue the OSC opposition brief review process.
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
Y:\LCP_v2.0\program_files\instructions\brief_drafting\osc_opposition\
  - osc_opposition_master.md
  - argument_instructions.md
  - legal_standard_instructions.md
  - emergency_relief_instructions.md

Y:\LCP_v2.0\program_files\instructions\brief_drafting\osc_reply\
  - reply_brief_instructions.md

Y:\LCP_v2.0\program_files\instructions\brief_drafting\osc_support\
  - osc_support_master.md
  - irreparable_harm_instructions.md
  - likelihood_of_success_instructions.md
  - balance_of_equities_instructions.md

Y:\LCP_v2.0\program_files\instructions\brief_drafting\
  - osc_order_instructions.md  (proposed OSC court forms)
  - affidavit_instructions.md  (affidavits/affirmations for motion support)
```

**Note:** Opposition/reply instruction files created 2025-12-30 using MTD instructions as templates. Support instruction files created 2025-12-30. Affidavit instructions created 2025-12-30.

---

## OSC-SPECIFIC CONSIDERATIONS

Orders to Show Cause differ from standard MTD practice in several key ways:

| Aspect | MTD | OSC Opposition |
|--------|-----|----------------|
| **Timeline** | Standard motion practice | Expedited/emergency timeline |
| **Relief Sought** | Dismissal of claims | Injunctive relief, TRO, preliminary injunction |
| **Standard** | Failure to state a claim | Likelihood of success, irreparable harm, balance of equities |
| **Burden** | On plaintiff to plead | On movant to demonstrate entitlement to extraordinary relief |
| **Tone** | Methodical legal analysis | Urgency + equitable considerations |

### Key Elements to Extract from OSC Opposition Briefs

1. **Emergency/Urgency Framing** - How attorneys address (or deflate) claimed urgency
2. **Irreparable Harm Rebuttal** - Techniques for showing harm is compensable/speculative
3. **Balance of Equities** - How to shift equities in client's favor
4. **Bond/Security Arguments** - When and how to request bond
5. **Status Quo Preservation** - Arguments about what constitutes the "status quo"
6. **Likelihood of Success** - Substantive defenses on the merits

### Key Elements to Extract from OSC Supporting Briefs

1. **Urgency Establishment** - How attorneys establish genuine emergency requiring immediate relief
2. **Irreparable Harm Demonstration** - Techniques for proving harm cannot be compensated by money damages
3. **Likelihood of Success** - Framing strength of underlying claims
4. **Balance of Equities** - Showing hardship to movant outweighs harm to opponent
5. **Status Quo Definition** - Framing what constitutes the "last peaceable uncontested status quo"
6. **Bond/Undertaking** - Addressing bond requirements proactively
7. **Specificity of Relief** - How to draft precise, enforceable injunctive relief

---

## REVIEW WORKFLOW

### Step 1: Select Next Brief
- Check BRIEF_QUEUE below for next unreviewed brief
- Read the PDF (use Read tool on the file path)
- Note: Focus on MEMORANDUM/OPPOSITION files responding to OSC applications

### Step 2: Extract Insights (While Reading)
Capture specific, actionable observations in these categories:

| Category | What to Look For |
|----------|------------------|
| **STRUCTURE** | Section ordering, heading styles, emergency framing |
| **ARGUMENT_TECHNIQUES** | Rebutting irreparable harm, shifting equities, attacking likelihood of success |
| **LANGUAGE_PATTERNS** | Urgency deflection, confidence phrases, equitable appeals |
| **CITATION_PRACTICE** | Preliminary injunction standards, TRO cases, bond requirements |
| **JURISDICTION_SPECIFIC** | NY vs Federal PI standards, local practice |
| **EMERGENCY_SPECIFIC** | How to address expedited timeline, request adjournment |

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
- Read the target instruction file (create if needed)
- Add the insight in appropriate location
- Mark insight as INTEGRATED below

---

## DOCUMENT_QUEUE

### Document Type Legend
| Type | Description | Instruction File Target |
|------|-------------|------------------------|
| **ORDER** | Proposed Order to Show Cause (court form for judge to sign) | `osc_order_instructions.md` (pending) |
| **MEMO** | Memorandum of Law (legal argument) | `osc_support_master.md` or `osc_opposition_master.md` |
| **AFF** | Affidavit/Affirmation (factual support) | `affidavit_instructions.md` (pending) |
| **LETTER** | Letter motion or correspondence | N/A |
| **EXHIBIT** | Supporting exhibits | N/A |

---

### Proposed OSC Orders (Court Forms)
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_2.pdf` | NYSCEF Doc 2 - Proposed OSC with TRO (6 pages). Structure insights extracted. |
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_11.pdf` | NYSCEF Doc 11 - Signed OSC (12 pages, includes duplicate). Same as Doc 2 but signed by J. Friedman 1/6/17. No new insights. |
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_13.pdf` | NYSCEF Doc 13 - **Defendant's** proposed OSC to vacate injunction (3 pages). CPLR 2221 renewal + TRO to stay. 4 insights extracted. |

### OSC Supporting Documents (To Be Classified)
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_63.pdf` | NYSCEF Doc 63 - **Defendant's** proposed OSC to compel compliance (3 pages). Motion to enforce prior order, no TRO. 4 insights extracted. |
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_85.pdf` | NYSCEF Doc 85 - Signed version of Doc 63 (3 pages). Signed by J. Sherwood 4/17/17. No new insights. |
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_86.pdf` | NYSCEF Doc 86 - Duplicate of Doc 85 (re-filed 4/17/17). No new insights. |
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_99.pdf` | NYSCEF Doc 99 - **Plaintiff's** proposed OSC with TRO (4 pages, includes dup). CPLR 2221 renewal, injunction + doc production. 4 insights extracted. |
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `..._ORDER_TO_SHOW_CAUSE_102.pdf` | NYSCEF Doc 102 - **Defendant's** proposed OSC seeking injunction modification (3 pages). Contractual rights framing. 4 insights extracted. |

### OSC Supporting Memos (Memoranda of Law)
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| REVIEWED | Art Capital v. BNTB | `..._MEMORANDUM_OF_LAW_I_5.pdf` | NYSCEF Doc 5 - Plaintiff's memo in support of initial OSC (4 pages). 6 insights extracted. |
| REVIEWED | Art Capital v. BNTB | `..._MEMORANDUM_OF_LAW_I_64.pdf` | NYSCEF Doc 64 - Memo supporting Doc 63 (motion to compel, 15 pages). 6 insights extracted. |
| REVIEWED | Art Capital v. BNTB | `..._MEMORANDUM_OF_LAW_I_103.pdf` | NYSCEF Doc 103 - Memo supporting Doc 102 (injunction modification, 6 pages). 5 insights extracted. |
| SKIPPED | Art Capital v. BNTB | `..._MEMORANDUM_OF_LAW_I_193.pdf` | NYSCEF Doc 193 - **NOT OSC**: Partial Summary Judgment motion (CPLR § 3212), 12 pages. Not relevant to OSC instructions. |
| SKIPPED | Art Capital v. BNTB | `..._MEMORANDUM_OF_LAW_I_200.pdf` | NYSCEF Doc 200 - **NOT OSC**: Motion to Dismiss Counterclaims (CPLR § 3211), 7 pages. Agent/veil piercing defenses. |
| SKIPPED | Art Capital v. BNTB | `..._MEMORANDUM_IN_OPPOS_209.pdf` | NYSCEF Doc 209 - **NOT OSC**: Opposition to Summary Judgment + Cross-Motion to Amend (CPLR § 3212/3025), 30 pages. Quality opposition brief but not OSC-related. |
| SKIPPED | Art Capital v. BNTB | `..._MEMORANDUM_OF_LAW_I_210.pdf` | NYSCEF Doc 210 - **NOT OSC**: Opposition to MTD Counterclaims (CPLR § 3211), 15 pages. Veil piercing/unjust enrichment defenses. |

### OSC Supporting Affidavits/Affirmations
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_3.pdf` | NYSCEF Doc 3 - Party principal affidavit (25 pages, 118 ¶¶). Initial OSC support. Key template. |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_15.pdf` | NYSCEF Doc 15 - Attorney emergency affirmation (4 pages, 14 ¶¶). Wrapper document. |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_20.pdf` | NYSCEF Doc 20 - Foreign affiant affirmation (5 pages). CPLR 2106 format. |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_26.pdf` | NYSCEF Doc 26 - Third-party gov't official affidavit (2 pages). Bermuda Registrar. |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_65.pdf` | NYSCEF Doc 65 - Foreign affiant affirmation (5 pages). Motion to compel support. |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_66.pdf` | NYSCEF Doc 66 - Attorney affirmation (4 pages). Heavy exhibit authentication (18 exhibits). |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_90.pdf` | NYSCEF Doc 90 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_92.pdf` | NYSCEF Doc 92 |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_100.pdf` | NYSCEF Doc 100 - Argumentative party affidavit (11 pages, 32 ¶¶). Rebuttal format. |
| REVIEWED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_104.pdf` | NYSCEF Doc 104 - Pure exhibit authentication (3 pages, 15 ¶¶). 13 exhibits. |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_125.pdf` | NYSCEF Doc 125 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_170.pdf` | NYSCEF Doc 170 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_174.pdf` | NYSCEF Doc 174 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_194.pdf` | NYSCEF Doc 194 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_197.pdf` | NYSCEF Doc 197 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_205.pdf` | NYSCEF Doc 205 |
| QUEUED | Art Capital v. BNTB | `..._AFFIDAVIT_OR_AFFIRM_206.pdf` | NYSCEF Doc 206 |

### Letters/Correspondence
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| QUEUED | Art Capital v. BNTB | `..._letter_correspond_8.pdf` | NYSCEF Doc 8 |

### OSC Opposition Briefs (Opposing TRO/Preliminary Injunction)
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| REVIEWED | Art Capital Bermuda v. Bank of N.T. Butterfield | `unprocessed_acb_v_bntb_docs/MEMORANDUM_OF_LAW_I_14.pdf` | Bank's motion to vacate preliminary injunction (NYSCEF Doc 14, 9 pages) - 5 insights extracted |
| SKIPPED | Bay Crane v. Metropolitan Steel | `unprocessed_bay_crane_docs/MEMORANDUM_IN_OPPOS_50.pdf` | **NOT OSC**: Summary Judgment opposition/cross-motion (CPLR § 3212), 12 pages. Mechanics lien foreclosure. |
| SKIPPED | Ragab | `unprocessed_ragab/RESPONSE_TO_STATEME_131.pdf` | **NOT OSC**: Response to Statement of Material Facts (SJ practice), 34 pages. Fiduciary duty/valuation dispute. |
| SKIPPED | Ragab | `unprocessed_ragab/MEMORANDUM_OF_LAW_I_153.pdf` | **NOT OSC**: Motion to Withdraw as Counsel (Whiteman Osterman & Hanna LLP), 7 pages. Non-payment withdrawal. |
| SKIPPED | Perl | `unprocessed_perl_docs/MEMORANDUM_OF_LAW_I_150.pdf` | **NOT OSC**: Opposition to Motion for Letters Rogatory, 28 pages. Discovery dispute re Vietnamese government docs. |
| SKIPPED | Perl | `unprocessed_perl_docs/MEMORANDUM_OF_LAW_I_59.pdf` | **NOT OSC**: Motion to Dismiss (CPLR 3211), 29 pages. Personal jurisdiction, failure to state claim, forum non conveniens. |

### OSC Reply Briefs
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| | | | *Add briefs as identified* |

### Cross-Motion Briefs (Opposition + Cross-Motion for Affirmative Relief)
| Status | Case | File Path | Notes |
|--------|------|-----------|-------|
| | | | *Add briefs as identified* |

---

## REVIEW_PROGRESS

### Completed Reviews
| Date | Document | Type | Reviewer | Insights Added |
|------|----------|------|----------|----------------|
| 2025-12-30 | Art Capital Doc 14 | MEMO | Claude | 5 (standing attack, asymmetric harm, quantifying harm, NY cases, unclean hands) |
| 2025-12-30 | Art Capital Doc 2 | ORDER | Claude | 6 (structure, language patterns, irreparable harm types, specificity, TRO provisions, sealing) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 11 | ORDER | Claude | 0 (signed version of Doc 2, no new insights) |
| 2025-12-30 | Art Capital Doc 13 | ORDER | Claude | 4 (defendant's OSC structure, CPLR 2221, TRO to stay, supporting papers) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 63 | ORDER | Claude | 4 (OSC for compliance, prior order reference, specificity, no TRO format) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 85 | ORDER | Claude | 0 (signed version of Doc 63, no new insights) |
| 2025-12-30 | Art Capital Doc 86 | ORDER | Claude | 0 (duplicate of Doc 85, no new insights) |
| 2025-12-30 | Art Capital Doc 99 | ORDER | Claude | 4 (CPLR 2221 plaintiff use, concise format, combined relief, concise TRO) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 102 | ORDER | Claude | 4 (injunction modification, contractual rights framing, hierarchical relief, multiple orders ref) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 5 | MEMO | Claude | 6 (concise format, CPLR 6301/6312(c), contract breach framework, niche market reputation, no prejudice argument, bad faith language) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 64 | MEMO | Claude | 6 (formal brief format, prior order enforcement, regulatory necessity, paper trail documentation, motion to compel cases, defined terms) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 103 | MEMO | Claude | 5 (concise modification format, changed circumstances, court's own words, opponent's arguments against them, CPLR 2221) - INTEGRATED |
| 2025-12-30 | Art Capital Doc 193 | MEMO | Claude | SKIPPED - Not OSC; Summary Judgment motion (CPLR § 3212) |
| 2025-12-30 | Art Capital Doc 200 | MEMO | Claude | SKIPPED - Not OSC; MTD Counterclaims (CPLR § 3211) |
| 2025-12-30 | Art Capital Doc 209 | MEMO | Claude | SKIPPED - Not OSC; Opposition to SJ + Cross-Motion to Amend (CPLR § 3212/3025) |
| 2025-12-30 | Art Capital Doc 210 | MEMO | Claude | SKIPPED - Not OSC; Opposition to MTD Counterclaims (CPLR § 3211) |
| 2025-12-30 | Art Capital Doc 3 | AFF | Claude | Party principal affidavit (25 pages). Key template for detailed OSC affidavits. |
| 2025-12-30 | Art Capital Doc 15 | AFF | Claude | Attorney emergency affirmation (4 pages). Wrapper document pattern. |
| 2025-12-30 | Art Capital Doc 20 | AFF | Claude | Foreign affiant affirmation (5 pages). CPLR 2106 format. |
| 2025-12-30 | Art Capital Doc 26 | AFF | Claude | Third-party gov't official affidavit (2 pages). New document type. |
| 2025-12-30 | Art Capital Doc 65 | AFF | Claude | Foreign affiant affirmation (5 pages). Motion to compel support. |
| 2025-12-30 | Art Capital Doc 66 | AFF | Claude | Attorney affirmation (4 pages). Heavy exhibit authentication pattern. |
| 2025-12-30 | Art Capital Doc 100 | AFF | Claude | Argumentative party affidavit (11 pages). Rebuttal format pattern. |
| 2025-12-30 | Art Capital Doc 104 | AFF | Claude | Pure exhibit authentication (3 pages). Minimal narrative pattern. |
| 2025-12-31 | Bangladesh Bank Doc 449 | ORDER | Claude | Proposed OSC (CPLR 3124 discovery motion vs Wong). 4 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 450 | AFF | Claude | Attorney affirmation (meet-and-confer documentation). 5 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 451 | EXHIBIT | Claude | Email chain exhibit (Loffler Aff. Exhibit A). 2 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 457 | ORDER | Claude | Signed OSC with Part 48 Addendum (virtual appearance + word count cert). 7 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 458 | ORDER | Claude | Signed OSC Motion 024 (RCBC custodian dispute). 3 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 459 | CONSOLIDATED | Claude | 21-page filing (OSC + Affirmation + Memo of Law). 6 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 460 | CONSOLIDATED | Claude | 18-page filing Motion 024 (sealed exhibits, custodian detail). 6 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 472 | MEMO | Claude | Reply Memorandum of Law (attack missing affidavit technique). 6 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 473 | AFF | Claude | Reply Affirmation (consecutive exhibit lettering). 3 insights extracted. |
| 2025-12-31 | Bangladesh Bank Doc 480 | DECISION | Claude | Decision + Order GRANTING both motions (Jackson requirements). 6 insights extracted. |

### Session Log
| Date | Session Notes |
|------|---------------|
| 2025-12-30 | Protocol created. Ready to begin reviews. Need to identify OSC opposition briefs in document library. |
| 2025-12-30 | Setup complete: Created instruction folders and 5 base instruction files (osc_opposition_master.md, argument_instructions.md, legal_standard_instructions.md, emergency_relief_instructions.md, reply_brief_instructions.md). Scanned document library (17 case folders). Identified Art Capital Doc 14 as OSC opposition brief. Ready to begin first review. |
| 2025-12-30 | Reviewed Art Capital Doc 14 (Bank's motion to vacate injunction). Extracted 5 insights: standing attack, asymmetric harm analysis, quantifying harm, NY case citations, unclean hands from misrepresentation. All insights integrated into argument_instructions.md and legal_standard_instructions.md. System fully operational. |
| 2025-12-30 | Expanded protocol to include OSC supporting briefs (TRO/PI applications). Added osc_support instruction file location, key extraction elements for supporting briefs, and queued 8 Art Capital OSC documents for review. Next: create osc_support instruction files. |
| 2025-12-30 | Created osc_support instruction folder and 4 base files: osc_support_master.md, irreparable_harm_instructions.md, likelihood_of_success_instructions.md, balance_of_equities_instructions.md. Ready to begin reviewing queued OSC supporting briefs. |
| 2025-12-30 | Reviewed Art Capital Doc 2. Document is proposed OSC order (court form), not a memo. Reorganized queue with Document Type Legend to distinguish: ORDER, MEMO, AFF, LETTER, EXHIBIT. Extracted 6 structural insights (pending integration). Need to create osc_order_instructions.md for proposed order drafting. |
| 2025-12-30 | Completed review of all 8 Art Capital OSC documents (Docs 2, 11, 13, 63, 85, 86, 99, 102). All were ORDER type (proposed or signed court forms). No memos of law found in this batch. Total: 22 pending insights across 5 docs with new content. Signed/duplicate docs (11, 85, 86) had no new insights. Key findings: OSC used for TROs, motions to vacate, motions to compel, injunction modifications. Next: create osc_order_instructions.md to integrate insights. |
| 2025-12-30 | Created osc_order_instructions.md (360 lines) integrating all 22 pending insights from Art Capital OSC documents. File covers: standard OSC structure, alternative formats (defendant's OSC, compliance motion, injunction modification), specificity of relief, TRO provisions, language patterns, and checklist. All insights marked as INTEGRATED. Next: identify actual memos of law (legal argument documents) for review. |
| 2025-12-30 | Added 25 documents to queue: 7 memos of law (Docs 5, 64, 103, 193, 200, 209, 210), 17 affidavits (Docs 3, 15, 20, 26, 65, 66, 90, 92, 100, 104, 125, 170, 174, 194, 197, 205, 206), and 1 letter (Doc 8). Ready to begin systematic review of memos. |
| 2025-12-30 | **Memo queue complete.** Reviewed all 7 queued memos: 3 OSC-related (Docs 5, 64, 103) extracted 17 insights; 4 non-OSC (Docs 193, 200, 209, 210) marked SKIPPED — these were later-stage motion practice (SJ, MTD) not OSC documents. Next: integrate 17 pending insights into instruction files. |
| 2025-12-30 | **All memo insights integrated.** Integrated 17 insights from Docs 5, 64, 103 into 4 instruction files: osc_support_master.md (format variations, defined terms, argument techniques, language patterns), likelihood_of_success_instructions.md (CPLR 6301/6312(c), contract breach framework, injunction modification), irreparable_harm_instructions.md (niche market reputation, regulatory necessity), balance_of_equities_instructions.md ("no prejudice" argument). Next: review queued affidavits. |
| 2025-12-30 | **Affidavit review complete.** Reviewed 8 of 17 queued affidavits (Docs 3, 15, 20, 26, 65, 66, 100, 104). Created comprehensive `affidavit_instructions.md` (450+ lines) covering 4 document types: party affidavit (sworn), attorney affirmation (CPLR 2106), foreign affiant affirmation (CPLR 2106), third-party gov't official affidavit. Added specialized structures: pure exhibit authentication, argumentative/rebuttal format. Key techniques: itemized compliance lists, telephone conversation documentation. Remaining 9 affidavits in queue but patterns well-established. |
| 2025-12-30 | **OSC opposition brief search (Ragab/Perl cases).** Searched Ragab and Perl case folders for OSC opposition briefs. Reviewed 3 candidate documents, all SKIPPED: Ragab Doc 153 (Motion to Withdraw as Counsel), Perl Doc 150 (Opposition to Letters Rogatory motion), Perl Doc 59 (Motion to Dismiss under CPLR 3211). Total OSC opposition briefs found to date: only Art Capital Doc 14. Session ended; continue searching remaining 13 case folders next session. |
| 2025-12-31 | **Bangladesh Bank case review.** Reviewed 10 documents from Bangladesh Bank v. RCBC et al. (Index No. 652051/2020). Two parallel discovery motions (023 vs Wong, 024 vs RCBC) both GRANTED. Documents: Proposed OSCs (449, 458), Signed OSCs with Part 48 Addendum (457, 458), Attorney affirmations (450, 473), Consolidated filings with memos (459, 460), Reply memo (472), Decision+Order (480). ~48 insights extracted covering: OSC for CPLR 3124 discovery, modern communication specificity, Commercial Division procedures, meet-and-confer documentation, reply techniques, sealed exhibit handling. |
| 2025-12-31 | **Bangladesh Bank insights integrated.** Integrated all ~48 insights from Bangladesh Bank case into 5 instruction files: osc_order_instructions.md (Commercial Division procedures, discovery OSC format, NYSCEF consolidated filing, parallel motions), affidavit_instructions.md (discovery motion affirmation, meet-and-confer documentation, consecutive exhibit lettering, custodian detail, sealed exhibits), osc_support_master.md (privilege log attack per Jackson, search methodology, dispositive flagging, prior order leverage), reply_brief_instructions.md (numbered response structure, attack missing affidavit, incredulity language, conclusory attack), argument_instructions.md (privilege workaround, prior testimony impeachment, personal affidavit requirement). Total reviewed: 34 documents (24 Art Capital + 10 Bangladesh Bank). |

---

## PENDING_INSIGHTS

### Awaiting Integration

*No pending insights. All extracted insights have been integrated.*

---

## INTEGRATED_INSIGHTS

### Already Added to Instructions
| Date | Brief Source | Category | Target File | Summary |
|------|--------------|----------|-------------|---------|
| 2025-12-30 | Art Capital Doc 14 | ARGUMENT_TECHNIQUES | argument_instructions.md | Standing/capacity attack example with *Terrell* citation |
| 2025-12-30 | Art Capital Doc 14 | ARGUMENT_TECHNIQUES | argument_instructions.md | Asymmetric harm analysis with *Ma v. Lien* citation |
| 2025-12-30 | Art Capital Doc 14 | ARGUMENT_TECHNIQUES | argument_instructions.md | Quantify harm technique for showing compensability |
| 2025-12-30 | Art Capital Doc 14 | CITATION_PRACTICE | legal_standard_instructions.md | Added *Gliklad*, *Terrell*, *Ma v. Lien* cases |
| 2025-12-30 | Art Capital Doc 14 | ARGUMENT_TECHNIQUES | argument_instructions.md | Enhanced unclean hands with misrepresentation example |
| 2025-12-30 | Art Capital Doc 2 | STRUCTURE | osc_order_instructions.md | Standard NY OSC format (5-part structure) |
| 2025-12-30 | Art Capital Doc 2 | LANGUAGE_PATTERNS | osc_order_instructions.md | Delegitimizing language ("purported and illegitimate") |
| 2025-12-30 | Art Capital Doc 2 | IRREPARABLE_HARM | osc_order_instructions.md | Multiple harm types for OSC allegations |
| 2025-12-30 | Art Capital Doc 2 | SPECIFICITY_OF_RELIEF | osc_order_instructions.md | 8 separate granular relief items |
| 2025-12-30 | Art Capital Doc 2 | TRO_PROVISIONS | osc_order_instructions.md | Lettered TRO relief items (A-D) |
| 2025-12-30 | Art Capital Doc 2 | SEALING | osc_order_instructions.md | Sealing provisions for confidential information |
| 2025-12-30 | Art Capital Doc 13 | STRUCTURE | osc_order_instructions.md | Defendant's OSC to vacate format |
| 2025-12-30 | Art Capital Doc 13 | CPLR_2221 | osc_order_instructions.md | Motion to renew/vacate structure |
| 2025-12-30 | Art Capital Doc 13 | TRO_TO_STAY | osc_order_instructions.md | TRO to stay existing injunction |
| 2025-12-30 | Art Capital Doc 13 | SUPPORTING_PAPERS | osc_order_instructions.md | Emergency motion support package listing |
| 2025-12-30 | Art Capital Doc 63 | OSC_USE_CASE | osc_order_instructions.md | OSC for motions to compel compliance |
| 2025-12-30 | Art Capital Doc 63 | PRIOR_ORDER_REFERENCE | osc_order_instructions.md | Tying relief to prior court rulings |
| 2025-12-30 | Art Capital Doc 63 | SPECIFICITY_OF_RELIEF | osc_order_instructions.md | Itemized compliance demands |
| 2025-12-30 | Art Capital Doc 63 | NO_TRO | osc_order_instructions.md | OSC format without TRO provisions |
| 2025-12-30 | Art Capital Doc 99 | CPLR_2221_PLAINTIFF | osc_order_instructions.md | CPLR 2221 for plaintiff renewals |
| 2025-12-30 | Art Capital Doc 99 | CONCISE_FORMAT | osc_order_instructions.md | Streamlined follow-on OSC format |
| 2025-12-30 | Art Capital Doc 99 | COMBINED_RELIEF | osc_order_instructions.md | Combined injunctive + document production |
| 2025-12-30 | Art Capital Doc 99 | TRO_CONCISE | osc_order_instructions.md | Concise TRO provision format |
| 2025-12-30 | Art Capital Doc 102 | INJUNCTION_MODIFICATION | osc_order_instructions.md | OSC for injunction modification |
| 2025-12-30 | Art Capital Doc 102 | CONTRACTUAL_RIGHTS_FRAMING | osc_order_instructions.md | Framing as exercise of contractual rights |
| 2025-12-30 | Art Capital Doc 102 | HIERARCHICAL_RELIEF | osc_order_instructions.md | Numbered + lettered subparts for relief |
| 2025-12-30 | Art Capital Doc 102 | MULTIPLE_PRIOR_ORDERS | osc_order_instructions.md | Defined terms for referencing prior orders |
| 2025-12-30 | Art Capital Doc 5 | STRUCTURE | osc_support_master.md | Concise 4-page emergency TRO format |
| 2025-12-30 | Art Capital Doc 5 | LEGAL_STANDARD | likelihood_of_success_instructions.md | CPLR 6301, Nobu Next Door, CPLR 6312(c) defensive use |
| 2025-12-30 | Art Capital Doc 5 | LIKELIHOOD_OF_SUCCESS | likelihood_of_success_instructions.md | Detailed contract breach framework (3 pillars) |
| 2025-12-30 | Art Capital Doc 5 | IRREPARABLE_HARM | irreparable_harm_instructions.md | Niche/specialized market reputation harm |
| 2025-12-30 | Art Capital Doc 5 | BALANCE_OF_EQUITIES | balance_of_equities_instructions.md | "No prejudice" argument technique |
| 2025-12-30 | Art Capital Doc 5 | LANGUAGE_PATTERNS | osc_support_master.md | Delegitimizing language and bad faith ascription |
| 2025-12-30 | Art Capital Doc 64 | STRUCTURE | osc_support_master.md | Formal 15-page brief format for non-emergency motions |
| 2025-12-30 | Art Capital Doc 64 | ARGUMENT_TECHNIQUE | osc_support_master.md | Prior order enforcement framing |
| 2025-12-30 | Art Capital Doc 64 | ARGUMENT_TECHNIQUE | irreparable_harm_instructions.md | Regulatory/compliance necessity |
| 2025-12-30 | Art Capital Doc 64 | ARGUMENT_TECHNIQUE | osc_support_master.md | Paper trail documentation |
| 2025-12-30 | Art Capital Doc 64 | CITATION_PRACTICE | osc_support_master.md | Motion to compel cases (U.S. Bank, Anonymous) |
| 2025-12-30 | Art Capital Doc 64 | STRUCTURE | osc_support_master.md | Defined terms for complex disputes |
| 2025-12-30 | Art Capital Doc 103 | STRUCTURE | osc_support_master.md | Concise 6-page injunction modification format |
| 2025-12-30 | Art Capital Doc 103 | ARGUMENT_TECHNIQUE | osc_support_master.md | Changed circumstances framework |
| 2025-12-30 | Art Capital Doc 103 | ARGUMENT_TECHNIQUE | osc_support_master.md | Using court's own prior statements |
| 2025-12-30 | Art Capital Doc 103 | ARGUMENT_TECHNIQUE | osc_support_master.md | Turning opponent's prior arguments against them |
| 2025-12-30 | Art Capital Doc 103 | LEGAL_STANDARD | likelihood_of_success_instructions.md | CPLR 2221 for injunction modification |
| 2025-12-31 | Bangladesh Bank Doc 449 | OSC_USE_CASE | osc_order_instructions.md | OSC for CPLR 3124 discovery motions |
| 2025-12-31 | Bangladesh Bank Doc 449 | MODERN_COMMUNICATIONS | osc_order_instructions.md | Platform-specific discovery (WhatsApp, Viber, etc.) |
| 2025-12-31 | Bangladesh Bank Doc 449 | RELIEF_SPECIFICITY | osc_order_instructions.md | Discovery relief categories with date ranges |
| 2025-12-31 | Bangladesh Bank Doc 450 | MEET_AND_CONFER | affidavit_instructions.md | Chronological meet-and-confer documentation |
| 2025-12-31 | Bangladesh Bank Doc 450 | DOCUMENT_STRUCTURE | affidavit_instructions.md | Discovery motion affirmation structure |
| 2025-12-31 | Bangladesh Bank Doc 450 | LANGUAGE_PATTERN | affidavit_instructions.md | Criticizing discovery responses: "generic," "boilerplate" |
| 2025-12-31 | Bangladesh Bank Doc 451 | EXHIBIT_FORMAT | affidavit_instructions.md | Email chain exhibit format with headers |
| 2025-12-31 | Bangladesh Bank Doc 457 | COMMERCIAL_DIV | osc_order_instructions.md | Part 48 Addendum (TEAMS, word count cert) |
| 2025-12-31 | Bangladesh Bank Doc 457 | SERVICE_REQUIREMENTS | osc_order_instructions.md | Dual service (overnight + email) |
| 2025-12-31 | Bangladesh Bank Doc 457 | BRIEF_SCHEDULE | osc_order_instructions.md | Opposition/reply deadlines in OSC |
| 2025-12-31 | Bangladesh Bank Doc 458 | PARALLEL_MOTIONS | osc_order_instructions.md | Multiple OSCs same return date |
| 2025-12-31 | Bangladesh Bank Doc 459 | CONSOLIDATED_FILING | osc_order_instructions.md | NYSCEF consolidated format |
| 2025-12-31 | Bangladesh Bank Doc 459 | PRIVILEGE_SPECIFICITY | osc_support_master.md | Jackson requirements for privilege logs |
| 2025-12-31 | Bangladesh Bank Doc 459 | SEARCH_DETAIL | osc_support_master.md | ESI search methodology requirements |
| 2025-12-31 | Bangladesh Bank Doc 460 | SEALED_EXHIBITS | affidavit_instructions.md | Confidential exhibit handling |
| 2025-12-31 | Bangladesh Bank Doc 460 | DISPOSITIVE_FLAGGING | osc_support_master.md | Discovery as "central" to case |
| 2025-12-31 | Bangladesh Bank Doc 460 | PRIVILEGE_WORKAROUND | argument_instructions.md | Alternative discovery paths |
| 2025-12-31 | Bangladesh Bank Doc 460 | CUSTODIAN_DETAIL | affidavit_instructions.md | ESI custodian identification |
| 2025-12-31 | Bangladesh Bank Doc 472 | REPLY_STRUCTURE | reply_brief_instructions.md | Numbered response structure |
| 2025-12-31 | Bangladesh Bank Doc 472 | ATTACK_MISSING_AFFIDAVIT | reply_brief_instructions.md | Missing personal affidavit technique |
| 2025-12-31 | Bangladesh Bank Doc 472 | INCREDULITY_LANGUAGE | reply_brief_instructions.md | "Strains credulity" language |
| 2025-12-31 | Bangladesh Bank Doc 472 | PRIOR_TESTIMONY | argument_instructions.md | Impeachment with prior statements |
| 2025-12-31 | Bangladesh Bank Doc 472 | CONCLUSORY_ATTACK | reply_brief_instructions.md | Attack unsupported assertions |
| 2025-12-31 | Bangladesh Bank Doc 473 | CONSECUTIVE_EXHIBITS | affidavit_instructions.md | Reply exhibit lettering |
| 2025-12-31 | Bangladesh Bank Doc 480 | PERSONAL_AFFIDAVIT | argument_instructions.md | Court ordered personal affidavit - validates technique |
| 2025-12-31 | Bangladesh Bank Doc 480 | JACKSON_REQUIREMENTS | osc_support_master.md | Privilege log specificity requirements |

---

## OSC OPPOSITION ARGUMENT FRAMEWORKS

### Standard Preliminary Injunction Test (NY State)
To obtain a preliminary injunction, movant must demonstrate:
1. **Likelihood of success on the merits**
2. **Irreparable injury absent injunctive relief**
3. **Balance of equities tips in movant's favor**

### TRO-Specific Considerations
- Immediate and irreparable injury
- Notice requirements (or grounds for ex parte relief)
- Bond/undertaking requirements

### Common Opposition Strategies

**Against Likelihood of Success:**
- Substantive defenses to underlying claims
- Disputed facts precluding summary determination
- Legal deficiencies in movant's claims

**Against Irreparable Harm:**
- Harm is compensable in money damages
- Harm is speculative/conjectural
- Movant caused own harm (unclean hands)
- Delay in seeking relief belies urgency

**Shifting Balance of Equities:**
- Harm to opponent outweighs harm to movant
- Public interest considerations
- Third-party impacts
- Maintaining true status quo favors opposition

**Procedural Objections:**
- Improper service/notice
- Failure to post adequate bond
- OSC procedurally defective
- Discovery needed before determination

---

## INSTRUCTION FILE TEMPLATES

When creating new instruction files for OSC opposition, use these as starting points:

### osc_opposition_master.md Structure
```
1. Purpose and Scope
2. Document Structure
   - Caption and Title
   - Table of Contents (if >10 pages)
   - Preliminary Statement
   - Statement of Facts
   - Argument
   - Conclusion
3. Formatting Requirements
4. Tone and Style Guidelines
5. Integration with Other Instructions
```

### argument_instructions.md Structure
```
1. Preliminary Injunction Standard
2. Attacking Likelihood of Success
3. Rebutting Irreparable Harm
4. Shifting Balance of Equities
5. Bond/Undertaking Arguments
6. Procedural Objections
7. Request for Evidentiary Hearing
```

---

## CONTEXT MANAGEMENT RULES

To prevent context exhaustion:

1. **One brief per session focus** - Don't try to review multiple briefs
2. **Extract, don't transcribe** - Capture the insight, not the full text
3. **Incremental updates** - Small additions to instruction files, not rewrites
4. **Save progress frequently** - Update this file before session ends
5. **Resume, don't restart** - Check this file first, continue from where left off

---

## NEXT STEPS

1. ~~**Identify OSC opposition briefs** in the unprocessed document library~~ ✓ DONE (2025-12-30)
2. ~~**Create instruction file folder** at `Y:\LCP_v2.0\program_files\instructions\brief_drafting\osc_opposition\`~~ ✓ DONE (2025-12-30)
3. ~~**Create base instruction files** using MTD opposition files as templates~~ ✓ DONE (2025-12-30)
4. ~~**Create osc_support instruction folder** at `Y:\LCP_v2.0\program_files\instructions\brief_drafting\osc_support\`~~ ✓ DONE (2025-12-30)
5. ~~**Create osc_support base instruction files** (osc_support_master.md, irreparable_harm_instructions.md, likelihood_of_success_instructions.md, balance_of_equities_instructions.md)~~ ✓ DONE (2025-12-30)
6. ~~**Review queued OSC documents** (8 docs from Art Capital case)~~ ✓ DONE (2025-12-30) — All ORDER type
7. ~~**Create osc_order_instructions.md** and integrate 22 pending insights~~ ✓ DONE (2025-12-30)
8. ~~**Identify OSC memos of law** (legal argument documents, not court forms)~~ ✓ DONE (2025-12-30) — 7 memos, 17 affidavits, 1 letter queued
9. ~~**Review queued memos of law** (Docs 5, 64, 103, 193, 200, 209, 210)~~ ✓ DONE (2025-12-30) — 3 OSC-related (17 insights), 4 non-OSC (skipped)
10. ~~**Integrate memo insights** (17 insights from Docs 5, 64, 103)~~ ✓ DONE (2025-12-30)
11. ~~**Review queued affidavits** (17 docs) — consider creating affidavit_instructions.md~~ ✓ DONE (2025-12-30) — 8 reviewed, affidavit_instructions.md created (450+ lines)
12. **Continue systematic review** of opposition briefs ← NEXT
13. **Review remaining affidavits** (9 docs: 90, 92, 125, 170, 174, 194, 197, 205, 206) — optional, patterns established

---

## END OF PROTOCOL
