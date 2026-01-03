# Document Request & Response Review Protocol

**Purpose:** Systematically review real attorney-drafted Document Requests AND Responses to Document Requests to improve LCP's discovery document generation quality.

**Session Start Prompt:**
```
Review Y:\LCP_v2.0\docs\DOCUMENT_REQUEST_REVIEW_PROTOCOL.md and continue the Document Request/Response review process.
```

---

## QUICK START (For New Sessions)

1. Read this file
2. Check `REVIEW_PROGRESS` section below for current status
3. Check `PENDING_INSIGHTS` section for insights awaiting integration
4. Either:
   - **Integrate pending insights** into instruction files (if any pending), OR
   - **Review next unreviewed document** from the queue

---

## LOCATIONS

**Documents to Review:**
```
Y:\resources\unprocessed_document_library\documents_by_case\
Y:\resources\Sample Discovery\  (if created)
```

**Instruction Files to Update:**
```
Y:\LCP_v2.0\program_files\instructions\discovery\

For Document Requests:
  - document_request_master.md
  - definitions_instructions.md
  - instructions_section.md
  - request_drafting_instructions.md

For Responses to Document Requests:
  - response_master.md
  - objection_instructions.md
  - response_drafting_instructions.md
  - privilege_log_instructions.md

Y:\LCP_v2.0\program_files\instructions\discovery\interrogatories\
  - interrogatory_master.md (if applicable)
```

---

## REVIEW WORKFLOW

### Step 1: Select Next Document
- Check DOCUMENT_QUEUE below for next unreviewed document request
- Read the PDF (use Read tool on the file path)
- Note: Focus on actual discovery demands, not notices or motions

### Step 2: Extract Insights (While Reading)
Capture specific, actionable observations in these categories:

#### For Document Requests:
| Category | What to Look For |
|----------|------------------|
| **DEFINITIONS** | How terms are defined, scope language, temporal limits |
| **INSTRUCTIONS** | Production format, privilege log requirements, continuing obligations |
| **REQUEST_STRUCTURE** | Numbering, grouping by topic, specificity vs. breadth |
| **LANGUAGE_PATTERNS** | Precise phrasing, "including but not limited to," catch-all clauses |
| **SCOPE_TECHNIQUES** | Date ranges, party/non-party coverage, document type specificity |
| **JURISDICTION_SPECIFIC** | NY CPLR vs Federal FRCP differences, local rules |

#### For Responses to Document Requests:
| Category | What to Look For |
|----------|------------------|
| **OBJECTION_PATTERNS** | Common objections (overbroad, unduly burdensome, privilege, relevance) |
| **OBJECTION_LANGUAGE** | Precise phrasing, preservation of rights, specificity of objections |
| **PARTIAL_COMPLIANCE** | "Subject to and without waiving objections" production language |
| **PRIVILEGE_ASSERTIONS** | Attorney-client, work product, other privilege claims |
| **SCOPE_LIMITATIONS** | How responding party narrows overbroad requests |
| **DOCUMENT_IDENTIFICATION** | Bates numbering references, document descriptions |
| **SUPPLEMENTATION** | Continuing duty language, reservation of rights to supplement |

### Step 3: Record Insights
Add to `PENDING_INSIGHTS` section below with:
- Document identifier
- Category
- Specific insight (quote examples when possible)
- Which instruction file should be updated

### Step 4: Update This File
- Move document from QUEUE to COMPLETED
- Save pending insights
- Note session end point

### Step 5: Integrate Insights (Same or Next Session)
When pending insights accumulate (3-5+):
- Read the target instruction file
- Add the insight in appropriate location
- Mark insight as INTEGRATED below

---

## DOCUMENT_QUEUE

### Document Requests

#### Plaintiff's Document Requests (Seeking Production from Defendant)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Case Name] | `[path to document]` |

#### Defendant's Document Requests (Seeking Production from Plaintiff)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Case Name] | `[path to document]` |

#### Third-Party Document Requests (Subpoena Duces Tecum)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Case Name] | `[path to document]` |

### Responses to Document Requests

#### Plaintiff's Responses (Responding to Defendant's Requests)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Case Name] | `[path to document]` |

#### Defendant's Responses (Responding to Plaintiff's Requests)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Case Name] | `[path to document]` |

#### Third-Party Responses (Responding to Subpoenas)
| Status | Case | File Path |
|--------|------|-----------|
| PENDING | [Case Name] | `[path to document]` |

---

## REVIEW_PROGRESS

### Completed Reviews
| Date | Document | Reviewer | Insights Added |
|------|----------|----------|----------------|
| 2025-12-30 | MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 162) | Claude | 10 |
| 2025-12-30 | MH Sub I v. Muehter - Defendant's 1st Expedited RFP + Plaintiffs' Response (NYSCEF Doc. 178) | Claude | 10 |
| 2025-12-30 | MH Sub I v. Muehter - NYSCEF Doc. 179 Parts 1-2 (Defendant's 2nd RFP + Plaintiffs' Response) | Claude | 10 |
| 2025-12-30 | MH Sub I v. Muehter - NYSCEF Doc. 179 Part 3 (Plaintiffs' Response to Requests 31-62) | Claude | 5 |
| 2025-12-30 | MH Sub I v. Muehter - NYSCEF Doc. 179 Part 4 (Plaintiffs' Response to Requests 62-88) | Claude | 5 |

### Session Log
| Date | Session Notes |
|------|---------------|
| 2025-12-30 | Protocol created. Queue empty - awaiting document request samples to be added. |
| 2025-12-30 | Added REFERENCE DECISIONS section with 10 recent NY discovery dispute cases (2024) from nycourts.gov and Justia. Cases cover proportionality, specificity, sanctions, and procedural requirements. |
| 2025-12-30 | Expanded protocol to cover RESPONSES to Document Requests. Added response-specific insight categories (objection patterns, privilege assertions, partial compliance, etc.), quality markers, document queue sections, and document types to collect. |
| 2025-12-30 | Reviewed first document: MH Sub I v. Muehter Plaintiffs' Response to 2nd RFP. Extracted 10 insights covering objection patterns, language, partial compliance, privilege assertions, and supplementation. |
| 2025-12-30 | Created discovery instruction files: objection_instructions.md, response_drafting_instructions.md, privilege_log_instructions.md. Integrated all 10 insights into appropriate instruction files. |
| 2025-12-30 | Reviewed NYSCEF Doc. 178: Compound document with Defendant's 1st Expedited RFP (10 requests) and Plaintiffs' Responses. Extracted 10 insights (3 REQUEST, 7 RESPONSE) covering expedited discovery patterns, interrogatory cross-references, and proportionality objections. |
| 2025-12-30 | Integrated Insights 11-20: Created request_drafting_instructions.md and instructions_section.md. Updated objection_instructions.md and response_drafting_instructions.md. Total instruction files now: 5. |
| 2025-12-30 | Reviewed NYSCEF Doc. 179 Parts 1-2: Large compound document with Defendant's 2nd RFP (88 requests, 23 definitions, 8 instructions) + Plaintiffs' Responses (18 General Objections, responses to Requests 1-31). Extracted 10 insights (5 REQUEST, 5 RESPONSE). Parts 3-4 deferred to next session. |
| 2025-12-30 | Integrated Insights 21-30: Created definitions_instructions.md. Updated request_drafting_instructions.md (anchoring techniques, time period overrides, high-volume warnings), objection_instructions.md (legal conclusion, definition suite, prior discovery cross-reference), and response_drafting_instructions.md (meet-and-confer default pattern). Total instruction files now: 6. All pending insights integrated. |
| 2025-12-30 | Reviewed NYSCEF Doc. 179 Part 3: Plaintiffs' Responses to Requests 31-62. Extracted 5 insights covering novel objection patterns (events that did not occur, overbroad party scope, undefined legal terms) and response techniques (turnabout production, conditional search-and-produce). Part 4 pending. |
| 2025-12-30 | Integrated Insights 31-35: Updated objection_instructions.md (factual premise objections section with events-that-did-not-occur, overbroad party scope, undefined legal terms) and response_drafting_instructions.md (conditional search-and-produce, turnabout production). All pending insights integrated. |
| 2025-12-30 | Reviewed NYSCEF Doc. 179 Part 4: Plaintiffs' Responses to Requests 62-88. Extracted 5 insights covering unintelligible request objections, expert discovery deferral with commitment, third-party relevance objections, high-volume duplicative cross-reference strategy, and discovery misconduct amplifier for fees. |
| 2025-12-30 | Integrated Insights 36-40: Updated objection_instructions.md (unintelligible request objection, third-party relevance objection, high-volume duplicative cross-reference strategy, discovery misconduct amplifier) and response_drafting_instructions.md (expert discovery deferral with commitment). All pending insights integrated. NYSCEF Doc. 179 review complete. |

---

## PENDING_INSIGHTS

### Awaiting Integration

*No pending insights at this time.*

---

### Integrated Insights Log

**Insight 1:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 162)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Comprehensive General Objections section (18 numbered objections) incorporated by reference

**Insight 2:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Case law citations in General Objections (*Editel*, *Dicostanzo*)

**Insight 3:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** PARTIAL_COMPLIANCE
- **Target File:** response_drafting_instructions.md
- **Insight:** Three-tier response structure

**Insight 4:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** "Known to Defendant" objection pattern

**Insight 5:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Cascading cross-reference technique for duplicative requests

**Insight 6:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** PRIVILEGE_ASSERTIONS
- **Target File:** privilege_log_instructions.md
- **Insight:** Clawback reservation language

**Insight 7:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** SCOPE_LIMITATIONS
- **Target File:** response_drafting_instructions.md
- **Insight:** Expert discovery deferral technique

**Insight 8:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Trade secret objection amplifier

**Insight 9:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Definition-by-definition objections

**Insight 10:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP
- **Category:** SUPPLEMENTATION
- **Target File:** response_drafting_instructions.md
- **Insight:** Comprehensive reservation of rights language

**Insight 11:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 1st Expedited RFP (NYSCEF Doc. 178)
- **Category:** REQUEST_STRUCTURE
- **Target File:** request_drafting_instructions.md
- **Insight:** Expedited discovery volume guidelines (10-15 targeted requests)

**Insight 12:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 1st Expedited RFP
- **Category:** INSTRUCTIONS
- **Target File:** instructions_section.md
- **Insight:** Default time period instruction with per-request override

**Insight 13:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 1st Expedited RFP
- **Category:** SCOPE_TECHNIQUES
- **Target File:** request_drafting_instructions.md
- **Insight:** Hearing exhibit request for expedited/injunction context

**Insight 14:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP (NYSCEF Doc. 178)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Expedited discovery proportionality objection

**Insight 15:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Interrogatory cross-reference technique

**Insight 16:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Circular definition objection

**Insight 17:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Arbitrary timeframe objection

**Insight 18:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP
- **Category:** PARTIAL_COMPLIANCE
- **Target File:** response_drafting_instructions.md
- **Insight:** "Documents sufficient to show" production technique

**Insight 19:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP
- **Category:** SCOPE_LIMITATIONS
- **Target File:** response_drafting_instructions.md
- **Insight:** Redirect to public sources

**Insight 20:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 1st Expedited RFP
- **Category:** SUPPLEMENTATION
- **Target File:** response_drafting_instructions.md
- **Insight:** Reciprocity caveat for opposing party's discovery failures

**Insight 21:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 2nd RFP (NYSCEF Doc. 179)
- **Category:** REQUEST_STRUCTURE
- **Target File:** request_drafting_instructions.md
- **Insight:** Complaint Paragraph-Anchored Requests technique

**Insight 22:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 2nd RFP (NYSCEF Doc. 179)
- **Category:** DEFINITIONS
- **Target File:** definitions_instructions.md
- **Insight:** Multi-Part "Identify" Definition with subparts for persons, entities, documents, communications, actions

**Insight 23:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 2nd RFP (NYSCEF Doc. 179)
- **Category:** SCOPE_TECHNIQUES
- **Target File:** request_drafting_instructions.md
- **Insight:** Time Period Override in Individual Requests for historical context

**Insight 24:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 2nd RFP (NYSCEF Doc. 179)
- **Category:** LANGUAGE_PATTERNS
- **Target File:** request_drafting_instructions.md
- **Insight:** Affidavit Cross-Referencing technique

**Insight 25:** INTEGRATED (2025-12-30)
- **Document Type:** REQUEST
- **Source:** MH Sub I v. Muehter - Defendant's 2nd RFP (NYSCEF Doc. 179)
- **Category:** REQUEST_STRUCTURE
- **Target File:** request_drafting_instructions.md
- **Insight:** High-Volume Request Strategy warning (Editel precedent)

**Insight 26:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179)
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Misconduct-Enhanced Trade Secret Objection

**Insight 27:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179)
- **Category:** PARTIAL_COMPLIANCE
- **Target File:** response_drafting_instructions.md
- **Insight:** "Meet and Confer" as Default Response Pattern

**Insight 28:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Legal Conclusion Objection for undefined legal terms

**Insight 29:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Definition Objection Suite with lettered subparts

**Insight 30:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Prior Discovery Cross-Reference Objection

**Insight 31:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 3)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** "Events That Did Not Occur" Objection

**Insight 32:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 3)
- **Category:** SCOPE_LIMITATIONS
- **Target File:** response_drafting_instructions.md
- **Insight:** Turnabout Production technique

**Insight 33:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 3)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Overbroad Party Scope Objection

**Insight 34:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 3)
- **Category:** PARTIAL_COMPLIANCE
- **Target File:** response_drafting_instructions.md
- **Insight:** Conditional Search-and-Produce Language

**Insight 35:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 3)
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Undefined Legal Term Objection

**Insight 36:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 4)
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** "Makes No Sense" / Unintelligible Request Objection

**Insight 37:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 4)
- **Category:** PARTIAL_COMPLIANCE
- **Target File:** response_drafting_instructions.md
- **Insight:** Expert Discovery Deferral with Commitment

**Insight 38:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 4)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** Third-Party/Collateral Matter Relevance Objection

**Insight 39:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 4)
- **Category:** OBJECTION_PATTERNS
- **Target File:** objection_instructions.md
- **Insight:** High-Volume Duplicative Cross-Reference Strategy

**Insight 40:** INTEGRATED (2025-12-30)
- **Document Type:** RESPONSE
- **Source:** MH Sub I v. Muehter - Plaintiffs' Response to 2nd RFP (NYSCEF Doc. 179, Part 4)
- **Category:** OBJECTION_LANGUAGE
- **Target File:** objection_instructions.md
- **Insight:** Discovery Misconduct Amplifier for Attorneys' Fees

---

## INSIGHT CATEGORIES EXPLAINED

### DEFINITIONS
- **Standard Definitions:** "Document," "Communication," "Person," "You," "Relating to"
- **Custom Definitions:** Case-specific terms, party names, transaction names
- **Temporal Scope:** "Relevant Period," date ranges
- **Inclusive Language:** "Including subsidiaries, affiliates, agents..."

### INSTRUCTIONS
- **Production Format:** Native files, Bates numbering, load files, metadata
- **Privilege Handling:** Privilege log requirements, redaction protocols
- **Continuing Obligations:** Duty to supplement
- **Objection Procedures:** How to note objections while still producing

### REQUEST_STRUCTURE
- **Topic Grouping:** Organizing requests by subject matter
- **Progressive Specificity:** General → Specific request ordering
- **Cross-References:** Requests that build on earlier definitions
- **Numbered Sub-Requests:** Breaking complex requests into components

### LANGUAGE_PATTERNS
- **Catch-All Phrases:** "Including but not limited to," "any and all"
- **Relational Language:** "Relating to," "concerning," "regarding," "reflecting"
- **Temporal Qualifiers:** "During the Relevant Period," "from [date] to present"
- **Party Coverage:** "You, your agents, employees, representatives, attorneys..."

### SCOPE_TECHNIQUES
- **Breadth Control:** Balancing comprehensive coverage vs. proportionality
- **Specificity Markers:** Document types, custodians, date ranges
- **Exclusions:** Carving out privileged or duplicative materials
- **Prioritization:** "First" and "Second" request sets for phased discovery

---

## INSIGHT CATEGORIES EXPLAINED - RESPONSES

### OBJECTION_PATTERNS
- **Overbroad Objections:** "Unduly broad in time and scope," "not reasonably calculated"
- **Burden Objections:** "Unduly burdensome," cost/benefit analysis language
- **Relevance Objections:** "Not relevant to any claim or defense"
- **Privilege Objections:** Attorney-client, work product, other privileges
- **Vagueness Objections:** "Vague and ambiguous as to [term]"
- **Compound Objections:** Objecting to requests seeking multiple categories

### OBJECTION_LANGUAGE
- **Preservation Language:** "Without waiving the foregoing objections..."
- **Specificity Markers:** Explaining WHY request is objectionable
- **Good Faith Qualifiers:** "To the extent [request seeks X], Defendant objects..."
- **Partial Response Signals:** "Subject to and without waiving these objections, Defendant responds..."

### PARTIAL_COMPLIANCE
- **Scope Narrowing:** "Defendant will produce documents limited to [narrowed scope]"
- **Time Limitations:** "Defendant will produce documents from [date] to [date]"
- **Custodian Limitations:** "Defendant will search the files of [specific custodians]"
- **Format Specifications:** How documents will be produced (native, PDF, etc.)

### PRIVILEGE_ASSERTIONS
- **Attorney-Client:** Communications with counsel for legal advice
- **Work Product:** Materials prepared in anticipation of litigation
- **Common Interest:** Shared privilege among co-parties
- **Other Privileges:** Trade secret, deliberative process, etc.
- **Privilege Log References:** "See accompanying privilege log"

### SCOPE_LIMITATIONS
- **Reasonable Interpretation:** "Defendant interprets this request to seek..."
- **Proportionality Arguments:** Burden vs. likely benefit analysis
- **Alternative Proposals:** Offering narrower production as compromise
- **Phased Discovery:** Proposing staged production approach

### DOCUMENT_IDENTIFICATION
- **Bates References:** "See documents Bates-stamped [XXX] through [XXX]"
- **Category Descriptions:** Describing types of documents produced
- **Location References:** Where documents were maintained
- **Custodian Identification:** Who maintained the documents

### SUPPLEMENTATION
- **Reservation of Rights:** "Defendant reserves the right to supplement..."
- **Continuing Duty:** Acknowledgment of ongoing discovery obligations
- **Rolling Production:** Language for phased document production

---

## SAMPLE INSIGHT FORMAT

```
**Insight [#]:** PENDING
- **Document Type:** [REQUEST/RESPONSE]
- **Category:**
  For Requests: [DEFINITIONS/INSTRUCTIONS/REQUEST_STRUCTURE/LANGUAGE_PATTERNS/SCOPE_TECHNIQUES/JURISDICTION_SPECIFIC]
  For Responses: [OBJECTION_PATTERNS/OBJECTION_LANGUAGE/PARTIAL_COMPLIANCE/PRIVILEGE_ASSERTIONS/SCOPE_LIMITATIONS/DOCUMENT_IDENTIFICATION/SUPPLEMENTATION]
- **Target File:** [instruction file to update]
- **Insight:** [Clear description of the technique or pattern]
- **Example:** "[Quoted example from the document]"
```

---

## QUALITY MARKERS TO IDENTIFY

### For Document Requests:

#### High-Quality Indicators
- [ ] Clear, unambiguous definitions
- [ ] Logical grouping of requests by topic
- [ ] Appropriate scope limitations (not overbroad)
- [ ] Specific document types identified
- [ ] Relevant custodians named
- [ ] Reasonable date ranges
- [ ] Professional formatting
- [ ] Proportional to case needs

#### Patterns to Avoid (Note as Anti-Patterns)
- [ ] Vague "any and all documents" without limits
- [ ] Missing definitions for key terms
- [ ] Overbroad temporal scope
- [ ] Duplicative requests
- [ ] Compound requests that should be separated
- [ ] Missing privilege log instructions

### For Responses to Document Requests:

#### High-Quality Indicators
- [ ] Specific objections (not boilerplate)
- [ ] Clear explanation of WHY objection applies
- [ ] Good faith partial compliance where possible
- [ ] Precise privilege assertions with basis stated
- [ ] Bates number references for produced documents
- [ ] Clear statement of what IS being produced
- [ ] Reasonable scope limitations with justification
- [ ] Reservation of rights to supplement
- [ ] Reference to accompanying privilege log

#### Patterns to Avoid (Note as Anti-Patterns)
- [ ] Boilerplate objections without specificity
- [ ] Blanket refusal to produce without justification
- [ ] Missing privilege log when privilege claimed
- [ ] Failure to identify what documents ARE being produced
- [ ] Vague "will produce responsive documents" without detail
- [ ] Objecting but failing to respond at all
- [ ] Missing verification/signature

---

## DOCUMENT TYPES TO COLLECT

Priority document types to add to queue:

### Document Requests

1. **Commercial Litigation Document Requests**
   - Contract disputes
   - Fraud/misrepresentation cases
   - Business torts

2. **Employment Litigation Document Requests**
   - Discrimination cases
   - Wrongful termination
   - Wage/hour disputes

3. **Securities Litigation Document Requests**
   - Shareholder derivative actions
   - Securities fraud

4. **Real Estate/Construction Litigation**
   - Contract disputes
   - Mechanic's liens

5. **Third-Party Subpoenas (Duces Tecum)**
   - Bank records
   - Employment records
   - Medical records

### Responses to Document Requests

1. **Responses with Strong Objections**
   - Well-crafted objection language
   - Successful scope limitations
   - Effective burden/proportionality arguments

2. **Responses with Partial Compliance**
   - "Subject to objections" production examples
   - Reasonable narrowing of overbroad requests
   - Good faith production with reservations

3. **Privilege-Heavy Responses**
   - Multiple privilege assertions
   - Well-structured privilege log references
   - Work product and attorney-client examples

4. **Third-Party/Subpoena Responses**
   - Non-party objection language
   - Cost-shifting requests
   - Privacy/confidentiality objections

5. **Supplemental Responses**
   - Rolling production language
   - Amended responses after meet-and-confer
   - Court-ordered production responses

---

## REFERENCE DECISIONS - NY DISCOVERY DISPUTE CASE LAW (2024)

Recent New York court decisions on discovery disputes. Use these to understand what courts approve/reject in discovery practice.

### Civil Discovery Decisions

#### 1. MH Sub I, LLC v. Muehter
- **Citation:** 2024 NY Slip Op 33382(U) (Sept. 25, 2024)
- **Court:** NY Supreme Court
- **URL:** https://www.nycourts.gov/Reporter/pdfs/2024/2024_33382.pdf
- **Issue:** Motion to compel production of communications (CPLR 3124/3126)
- **Holding:** Motion DENIED - request was "not reasonably tailored by subject matter" as it demanded all communications regardless of subject matter
- **Key Lesson:** Requests must be specifically tailored to relevant subject matter; overly broad demands will be rejected

#### 2. Stevens v. New York City Transit Authority
- **Citation:** 2024 NY Slip Op 34279(U) (Dec. 4, 2024)
- **Court:** NY Supreme Court
- **URL:** https://www.nycourts.gov/reporter//pdfs/2024/2024_34279.pdf
- **Issue:** Scope of document production for witness identification
- **Holding:** Request for butcher books of all persons at scene deemed OVERLY BROAD and unduly burdensome
- **Key Lesson:** "Competing interests must always be balanced; the need for discovery must be weighed against any special burden"

#### 3. Bagatelle Little W. 12th LLC v. JEC II, LLC
- **Citation:** 2024 NY Slip Op 50453(U)
- **Court:** NY Supreme Court
- **URL:** https://nycourts.gov/reporter/3dseries/2024/2024_50453.htm
- **Issue:** Letters rogatory for international document production (CPLR 3102/3108)
- **Holding:** Motion DENIED - to compel production from international entities, movant must establish information is "crucial" to resolution of key issue
- **Key Lesson:** Heightened standard for international discovery; must show information is crucial, not merely relevant

#### 4. Gibson v. Delemos
- **Citation:** 2024 (Second Department)
- **Court:** Appellate Division, Second Department
- **URL:** https://law.justia.com/cases/new-york/appellate-division-second-department/2024/2021-01129.html
- **Issue:** CPLR 3126 sanctions - motion to strike complaint for discovery failures
- **Holding:** REVERSED lower court - plaintiff substantially complied; conduct was not willful and contumacious
- **Key Lesson:** Striking a pleading requires clear showing of WILLFUL AND CONTUMACIOUS conduct; substantial compliance defeats sanctions

#### 5. Muhammad v. Ramadan
- **Citation:** 2024 (Second Department)
- **Court:** Appellate Division, Second Department
- **URL:** https://law.justia.com/cases/new-york/appellate-division-second-department/2024/2021-08344.html
- **Issue:** CPLR 3126 motion to strike answer for discovery failures
- **Holding:** AFFIRMED striking of defendants' answer - willful conduct inferred from "repeated failures over an extended period" without adequate excuse
- **Key Lesson:** Pattern of non-compliance over extended period supports severe sanctions even without express finding of willfulness

#### 6. Breitman v. Tax Commission of City of N.Y.
- **Citation:** 2024 NY Slip Op 50246(U)
- **Court:** NY Supreme Court
- **URL:** https://www.nycourts.gov/reporter/3dseries/2024/2024_50246.htm
- **Issue:** Motion to compel response to Request for Information in tax certiorari
- **Holding:** Court addressed concerns about "cherry-picked" documents; ordered production of comparable materials
- **Key Lesson:** Responding party cannot selectively produce only favorable documents; court may order comparable documents to prevent cherry-picking

#### 7. Bayview Loan Servicing, LLC v. Evanson
- **Citation:** Sept. 11, 2024 (Second Department)
- **Court:** Appellate Division, Second Department
- **URL:** https://www.nycourts.gov/courts/ad2/Handdowns/2024/Decisions/D74728.pdf
- **Issue:** Motion to strike under CPLR 3126(3) for discovery failures
- **Holding:** Court reminded litigants to follow requisite procedures before seeking sanctions (22 NYCRR 202.20-f)
- **Key Lesson:** Procedural prerequisites (good faith conference, proper notice) must be satisfied before court will consider discovery sanctions

#### 8. O'Rourke v. Hammerstein Ballroom
- **Citation:** 2024 (Manhattan Commercial Division)
- **Court:** NY Supreme Court, Commercial Division (Justice Margaret Chan)
- **URL:** https://www.nycomdiv.com/category/discovery/
- **Issue:** CPLR 3124/3126 sanctions for repeated failure to appear at deposition
- **Holding:** Court STRUCK complaint for plaintiff's repeated failure to appear for scheduled deposition
- **Key Lesson:** Repeated deposition no-shows warrant case-dispositive sanctions; Commercial Division enforces discovery obligations strictly

### Criminal Discovery Decisions (CPL Article 245)

#### 9. People v. Jackson
- **Citation:** 2024-2025
- **Court:** NY Criminal Court
- **URL:** https://law.justia.com/cases/new-york/other-courts/2025/2025-ny-slip-op-51635-u.html
- **Issue:** Certificate of Compliance validity - undisclosed photographs
- **Holding:** Court assessed due diligence using *Bay* factors: efforts to comply, volume of discovery, complexity, how obvious missing material would have been
- **Key Lesson:** COC validity depends on good faith and due diligence, not perfection; courts apply multi-factor test

#### 10. People v. Snyder
- **Citation:** 2024 NY Slip Op 51877(U)
- **Court:** NY Criminal Court
- **URL:** https://www.nycourts.gov/reporter//3dseries/2024/2024_51877.htm
- **Issue:** Sanction for late disclosure of video evidence
- **Holding:** Court PRECLUDED all video evidence disclosed late AND precluded testimony regarding those videos
- **Key Lesson:** CPL 245 sanctions can include complete preclusion of late-disclosed evidence and related testimony

### Key Themes from 2024 Decisions

#### For Document Requests:
| Theme | Cases | Drafting Implication |
|-------|-------|---------------------|
| **Proportionality** | Stevens, MH Sub I | Tailor requests to case needs; avoid "any and all" |
| **Specificity Required** | MH Sub I, Bagatelle | Requests must identify subject matter, not just document types |
| **Procedural Prerequisites** | Bayview | Must confer in good faith before motion practice |

#### For Responses:
| Theme | Cases | Drafting Implication |
|-------|-------|---------------------|
| **No Cherry-Picking** | Breitman | Responses must be complete, not selective |
| **Substantial Compliance** | Gibson, Jackson | Good faith partial compliance defeats sanctions |
| **Willful Non-Compliance** | Muhammad, O'Rourke | Repeated failures = severe sanctions; respond timely |
| **Specific Objections** | MH Sub I | Objections should explain WHY request is deficient |

---

## CONTEXT MANAGEMENT RULES

To prevent context exhaustion:

1. **One document per session focus** - Don't try to review multiple documents
2. **Extract, don't transcribe** - Capture the insight, not the full text
3. **Incremental updates** - Small additions to instruction files, not rewrites
4. **Save progress frequently** - Update this file before session ends
5. **Resume, don't restart** - Check this file first, continue from where left off

---

## END OF PROTOCOL
