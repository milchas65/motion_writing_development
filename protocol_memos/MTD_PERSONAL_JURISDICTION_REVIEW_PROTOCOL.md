# Motion to Dismiss for Lack of Personal Jurisdiction - Review Protocol

**Purpose:** Systematically review complete motion packages—from Notice of Motion through Final Decision—to extract insights for AI instruction across four categories: Motion Arc, Case Law Effectiveness, Writing Style, and Strategy.

**Session Start Prompt:**
```
Review Y:\motion_writing_development\protocol_memos\MTD_PERSONAL_JURISDICTION_REVIEW_PROTOCOL.md and continue the motion package review process.
```

---

## QUICK START (For New Sessions)

1. Read this file
2. Check `ACTIVE_MOTION_TYPE` section for current motion type being studied
3. Check `REVIEW_PROGRESS` section for current status
4. Check `PENDING_INSIGHTS` section for insights awaiting integration
5. **Before reviewing any new document:**
   - Check file size (see `DOCUMENT SIZE ASSESSMENT` section)
   - If > 500 KB, plan chunking strategy before reading
   - Token estimate: `characters ÷ 1.5` (threshold: 60,000 tokens)
6. Either:
   - **Integrate pending insights** into instruction files (if any pending), OR
   - **Review next document** in the current motion package, OR
   - **Begin new motion package** if current one is complete

---

## KEY DIFFERENCE FROM BRIEF REVIEW PROTOCOLS

| Aspect | Brief Review Protocols | This Protocol |
|--------|------------------------|---------------|
| **Scope** | Individual memoranda of law | Complete motion package (all filings) |
| **Documents** | Memorandum only | Notice, Affirmations, Affidavits, Exhibits, Memos, Opposition, Reply, Decision |
| **Output** | Writing style insights only | Four categories: Arc, Case Law, Writing, Strategy |
| **Destination** | `*_master.md`, `argument_instructions.md` | Multiple files per motion type |

---

## FOUR INSIGHT CATEGORIES

### 1. MOTION_ARC
**What it captures:** The structure, progression, and lifecycle of the motion type from filing to decision.

**Look for:**
- Required components (what must be filed)
- Typical sequence of filings
- Timing patterns (return dates, response deadlines)
- How courts structure their analysis in decisions
- Procedural prerequisites and conditions
- Common procedural pitfalls
- Whether motion is pre-answer or post-answer
- Interaction with CPLR 3211(e) single-motion rule

**Destination:** `MOTION_ARC.md`

---

### 2. CASE_LAW_EFFECTIVENESS
**What it captures:** Which precedents succeed vs. fail in supporting/opposing the motion.

**Look for:**
- Cases cited by winning party that court adopted
- Cases cited by losing party that court rejected or distinguished
- How courts characterize "leading" vs. "inapplicable" cases
- Patterns in which cases courts find persuasive
- Cases that are consistently cited vs. ignored
- How parties distinguish unfavorable precedent
- Long-arm statute cases vs. constitutional due process cases
- Forum selection clause enforceability precedents

**Destination:** `CASE_LAW_EFFECTIVENESS.md`

---

### 3. WRITING_STYLE
**What it captures:** Tone, structure, and rhetorical approaches that work.

**Look for:**
- Effective point heading formulations
- Persuasive language patterns
- Citation practices
- Structure and organization
- Argument framing techniques
- Statement of facts presentation (jurisdictional facts focus)
- How contacts are marshaled and presented

**Destination:** Motion-type instruction files (`*_master.md`, `argument_instructions.md`, etc.)

---

### 4. STRATEGY
**What it captures:** Tactical considerations for both movant and opponent.

**Look for:**
- What arguments won vs. lost
- Timing considerations (when to bring motion, waiver risks)
- Evidence marshaling (what evidence was dispositive for jurisdiction)
- Burden allocation and shifting dynamics
- Opponent's successful defenses
- Common mistakes that courts penalize
- Winning combinations of arguments
- Jurisdictional discovery issues

**Destination:** `STRATEGY_GUIDE.md`

---

## DOCUMENT TYPES IN A MOTION PACKAGE

### Moving Papers
| Document | What to Extract |
|----------|-----------------|
| **Notice of Motion** | Required procedural elements, relief sought, CPLR 3211(a)(8) citation |
| **Attorney Affirmation** | How exhibits are authenticated, procedural recitals |
| **Defendant Affidavit** | Personal knowledge statements about lack of NY contacts, business operations |
| **Exhibits** | Types of evidence used (contracts, correspondence, corporate records), how organized |
| **Memorandum of Law** | Writing style, argument structure, case citations |

### Opposition Papers
| Document | What to Extract |
|----------|-----------------|
| **Attorney Affirmation in Opposition** | How jurisdictional facts are presented |
| **Plaintiff Affidavits** | How contacts with NY are established, transactions described |
| **Opposition Exhibits** | Types of jurisdictional evidence (emails, contracts, visits, business records) |
| **Memorandum in Opposition** | Writing style, defensive strategies, case distinctions |

### Reply Papers
| Document | What to Extract |
|----------|-----------------|
| **Reply Affirmation** | How to address new jurisdictional evidence |
| **Reply Memorandum** | Narrowing issues, rebuttal techniques |

### Court Decision
| Document | What to Extract |
|----------|-----------------|
| **Decision/Order** | What arguments the court found persuasive, legal standards applied, which cases court relied on, how court applied long-arm statute and due process analysis |

---

## REVIEW WORKFLOW

### Phase 0: Assess Document Sizes
Before beginning any review, check document sizes and plan chunking:

1. **List all files with sizes:**
   ```bash
   ls -lhS /path/to/motion/package/
   ```

2. **Categorize by size:**
   - **Green (< 500 KB):** Single-pass review
   - **Yellow (500 KB - 1 MB):** Check content, may need chunking
   - **Red (> 1 MB):** Requires chunking plan

3. **Add size column to inventory table** (see template below)

4. **Flag documents requiring chunking** with `[CHUNK]` marker

### Phase 1: Inventory the Package
Before reviewing content, catalog all documents in the motion package (include file sizes):

```
MOTION PACKAGE: [Case Name] - Motion to Dismiss for Lack of Personal Jurisdiction

MOVING PAPERS:
| Status | Document | Size | Chunking |
|--------|----------|------|----------|
| [ ] | Notice of Motion | ___ KB | Single |
| [ ] | Attorney Affirmation (__ exhibits) | ___ KB | Single |
| [ ] | Affidavit of [Defendant] | ___ KB | Single |
| [ ] | Memorandum of Law (__ pages) | ___ KB | [Check] |

OPPOSITION PAPERS:
| Status | Document | Size | Chunking |
|--------|----------|------|----------|
| [ ] | Attorney Affirmation in Opposition | ___ KB | Single |
| [ ] | Affidavit of [Plaintiff/Witness] | ___ KB | Single |
| [ ] | Opposition Exhibits (__ exhibits) | ___ KB | [Check] |
| [ ] | Memorandum in Opposition (__ pages) | ___ KB | [Check] |

REPLY PAPERS:
| Status | Document | Size | Chunking |
|--------|----------|------|----------|
| [ ] | Reply Affirmation | ___ KB | Single |
| [ ] | Reply Memorandum (__ pages) | ___ KB | Single |

DECISION:
| Status | Document | Size | Chunking |
|--------|----------|------|----------|
| [ ] | Decision/Order dated [date] | ___ KB | Single |

RESULT: [GRANTED/DENIED/GRANTED IN PART]
JURISDICTIONAL BASIS ANALYZED: [General/Specific/Both]

CHUNKING SUMMARY:
- Total documents: __
- Single-pass (< 500 KB): __
- May need chunking (500 KB - 1 MB): __
- Requires chunking (> 1 MB): __
```

### Phase 2: Review in Order
Review documents in filing sequence to understand the motion's arc:

1. **Moving papers** - Understand the motion's foundation and defendant's jurisdictional challenge
2. **Opposition papers** - See how plaintiff establishes jurisdictional contacts
3. **Reply papers** - See how defendant rebuts jurisdictional showing
4. **Decision** - See what the court credited and how it applied the legal framework

### Phase 3: Extract Insights by Category
As you review each document, capture insights in ALL FOUR categories:

| Category | Questions to Ask |
|----------|------------------|
| **MOTION_ARC** | What was required to file? What sequence? What did court expect? How did court structure its analysis? |
| **CASE_LAW** | Which cases were cited? Which did court adopt? Which rejected? How were Daimler, Goodyear, International Shoe treated? |
| **WRITING** | What language/structure was effective? What templates emerge? How were contacts organized? |
| **STRATEGY** | What arguments won? What mistakes were made? What evidence of contacts mattered? Discovery issues? |

### Phase 4: Record Insights
Add to `PENDING_INSIGHTS` section with:
- Motion package identifier
- Document reviewed
- Category (ARC / CASE_LAW / WRITING / STRATEGY)
- Specific insight
- Target instruction file

### Phase 5: Integrate Insights
When insights accumulate (3-5 per category):
- Read the target instruction file
- Add insight in appropriate location
- Mark insight as INTEGRATED

---

## INSTRUCTION FILE STRUCTURE (Per Motion Type)

```
Y:\LCP_v2.0\program_files\brief_drafting\mtd_personal_jurisdiction\
├── motion\
│   ├── mtd_pj_motion_master.md          [TO CREATE]
│   ├── argument_instructions.md          [TO CREATE]
│   └── statement_of_facts_instructions.md [TO CREATE]
├── opposition\
│   ├── mtd_pj_opposition_master.md       [TO CREATE]
│   ├── argument_instructions.md          [CREATED 2026-01-02]
│   └── counter_statement_instructions.md [TO CREATE]
├── reply\
│   └── reply_brief_instructions.md       [TO CREATE]
├── MOTION_ARC.md                         [CREATED 2026-01-02]
├── CASE_LAW_EFFECTIVENESS.md             [CREATED 2026-01-02]
└── STRATEGY_GUIDE.md                     [CREATED 2026-01-02]
```

---

## ACTIVE_MOTION_TYPE

**Current Focus:** Motion to Dismiss for Lack of Personal Jurisdiction

**Directory:** `Y:\LCP_v2.0\program_files\brief_drafting\mtd_personal_jurisdiction\`

**Legal Framework:**
- **NY Long-Arm Statute:** CPLR 301 (general jurisdiction), CPLR 302 (specific jurisdiction)
  - CPLR 302(a)(1): Transaction of business
  - CPLR 302(a)(2): Tortious act within NY
  - CPLR 302(a)(3): Tortious act outside NY causing injury within NY
  - CPLR 302(a)(4): Real property ownership
- **Procedural Basis:** CPLR 3211(a)(8) - lack of jurisdiction over defendant
- **Constitutional Limitation:** Due Process Clause (14th Amendment)
- **Key Concepts:**
  - General jurisdiction: "At home" standard (*Daimler AG v. Bauman*, *Goodyear Dunlop Tires*)
  - Specific jurisdiction: Minimum contacts, purposeful availment, relatedness
  - Consent jurisdiction: Forum selection clauses, registration statutes
  - Transient jurisdiction: Service during physical presence (tag jurisdiction)
- **Burden of Proof:** Plaintiff bears burden of establishing jurisdiction; on motion to dismiss, court may consider affidavits and give plaintiff benefit of all reasonable inferences
- **Discovery:** Jurisdictional discovery may be warranted if plaintiff makes sufficient start

---

## MOTION_PACKAGE_QUEUE

### Motion to Dismiss for Lack of Personal Jurisdiction
| Status | Case | Location | Documents |
|--------|------|----------|-----------|
| **IN REVIEW** | Aybar v. Ford Motor Co. & Goodyear Tire | `Y:\motion_writing_development\motion_packages\personal_jurisdiction\aybar_v_us_tires_and_wheels\` | See inventory below |

---

## CURRENT_PACKAGE_INVENTORY

### Aybar v. Ford Motor Company & The Goodyear Tire & Rubber Co.
**Index No.:** 703632/2017
**Court (Trial):** NY Supreme Court, Queens County
**Appellate Division:** Second Department (2019)
**Court of Appeals:** 37 N.Y.3d 274 (2021)
**Decision Date:** October 7, 2021
**Jurisdiction Issue:** Consent-by-registration - whether foreign corporation consents to general jurisdiction by registering to do business in NY under Business Corporation Law
**Result:**
- **Trial Court:** DENIED (found jurisdiction existed via consent-by-registration under *Bagdon*)
- **Appellate Division:** REVERSED (granted motions to dismiss)
- **Court of Appeals:** AFFIRMED Appellate Division (no consent to general jurisdiction)

**Case Significance:** Landmark decision rejecting 100+ years of *Bagdon v. Philadelphia & Reading Coal & Iron Co.* interpretation; establishes that BCL registration = consent to service only, NOT consent to general jurisdiction.

---

#### LEVEL 1: TRIAL COURT (Seq 017 & 019 - Motion to Dismiss)
**Location:** `seq_017_and_019_lack_of_personal_jurisdiction/`

##### MOVING PAPERS (Ford/Goodyear Motions - Seq 017 & 019)
| # | Document | File | Status |
|---|----------|------|--------|
| 1 | Notice of Motion (Seq 017) | `703632_2017_..._NOTICE_OF_MOTION_88 (1).pdf` | [ ] |
| 2 | Affidavit in Support | `703632_2017_..._AFFIDAVIT_OR_AFFIRM_89.pdf` | [ ] |
| 3 | Exhibit A | `703632_2017_..._EXHIBIT_S__90.pdf` | [ ] |
| 4 | Exhibit B | `703632_2017_..._EXHIBIT_S__91.pdf` | [ ] |
| 5 | Exhibit C | `703632_2017_..._EXHIBIT_S__92.pdf` | [ ] |
| 6 | Notice of Motion (Seq 019) | `703632_2017_..._NOTICE_OF_MOTION__A_93.pdf` | [ ] |
| 7 | Affidavit in Support | `703632_2017_..._AFFIDAVIT_OR_AFFIRM_94.pdf` | [ ] |
| 8 | Exhibits D-J | `703632_2017_..._EXHIBIT_S__95-103.pdf` (9 exhibits) | [ ] |
| 9 | Additional Exhibit | `703632_2017_..._EXHIBIT_S__119.pdf` | [ ] |

##### OPPOSITION PAPERS (Plaintiffs' Opposition)
| # | Document | File | Status |
|---|----------|------|--------|
| 10 | Affidavit in Opposition | `703632_2017_..._AFFIDAVIT_OR_AFFIRM_122.pdf` | [ ] |
| 11 | Affirmation in Opposition | `703632_2017_..._AFFIRMATION_AFFIDAV_123.pdf` | [ ] |
| 12 | Exhibits in Opposition | `703632_2017_..._EXHIBIT_S__124.pdf`, `125.pdf`, `127.pdf` | [ ] |
| 13 | Affidavit | `703632_2017_..._AFFIDAVIT_OR_AFFIRM_129.pdf` | [ ] |

##### CROSS-MOTION / REPLY PAPERS
| # | Document | File | Status |
|---|----------|------|--------|
| 14 | Notice of Cross-Motion | `703632_2017_..._NOTICE_OF_CROSS_MOT_136.pdf` | [ ] |
| 15 | Affidavit in Support of Cross-Motion | `703632_2017_..._AFFIDAVIT_OR_AFFIRM_137.pdf` | [ ] |
| 16 | Cross-Motion Exhibits | `703632_2017_..._EXHIBIT_S__138-145.pdf` (8 exhibits) | [ ] |
| 17 | Additional Affidavit | `703632_2017_..._AFFIDAVIT_OR_AFFIRM_146.pdf` | [ ] |
| 18 | Additional Exhibits | `703632_2017_..._EXHIBIT_S__147.pdf`, `148.pdf` | [ ] |

##### TRIAL COURT DECISIONS
| # | Document | File | Status |
|---|----------|------|--------|
| 19 | Decision & Order on Motion | `703632_2017_..._DECISION___ORDER_ON_202.pdf` | [ ] |
| 20 | Decision & Order (duplicate) | `703632_2017_..._DECISION___ORDER_ON_203.pdf` | [ ] |

##### NOTICES OF APPEAL
| # | Document | File | Status |
|---|----------|------|--------|
| 21 | Notice of Appeal | `703632_2017_..._NOTICE_OF_APPEAL_IN_205.pdf` | [ ] |
| 22 | Notice of Appeal | `703632_2017_..._NOTICE_OF_APPEAL_IN_206.pdf` | [ ] |
| 23 | Notice of Entry | `703632_2017_..._NOTICE_OF_ENTRY_207.pdf` | [ ] |
| 24 | Notice of Appeal | `703632_2017_..._NOTICE_OF_APPEAL_IN_208.pdf` | [ ] |

---

#### LEVEL 2: APPELLATE DIVISION (Second Department)
**Location:** `2nd_dept_appeal/`
**Appeal No.:** 2019-12110
**Decision:** 169 AD3d 137 (2d Dept 2019)

##### APPELLATE NOTICES & PROCEDURAL
| # | Document | File | Status |
|---|----------|------|--------|
| 25 | Copy of Notice of Appeal | `..._COPY_OF_NOTICE_OF_A_1.pdf` | [ ] |
| 26 | Copy of Additional Notice | `..._COPY_OF_ADDITIONAL__2.pdf` | [ ] |
| 27 | Proof of Service | `..._PROOF_OF_SERVICE_OF_3.pdf` | [ ] |
| 28 | Notice of Appearance | `..._NOTICE_OF_APPEARANCE_4.pdf` | [ ] |
| 29 | Notice of Appearance | `..._NOTICE_OF_APPEARANCE_13.pdf` | [ ] |

##### JOINT RECORDS ON APPEAL (REQUIRES CHUNKING)
| # | Document | File | Size | Status | Notes |
|---|----------|------|------|--------|-------|
| 30 | **Joint Record on Appeal Vol. 1** | `..._JOINT_RECORD_ON_APP_6.pdf` | **33 MB** | [ ] | **CHUNKING REQUIRED - 400+ pages** |
| 31 | **Joint Record on Appeal Vol. 2** | `..._JOINT_RECORD_ON_APP_7.pdf` | **65 MB** | [ ] | **CHUNKING REQUIRED - 400+ pages** |

##### APPELLATE BRIEFS
| # | Document | File | Status | Priority |
|---|----------|------|--------|----------|
| 32 | **Appellant's Brief (Ford/Goodyear)** | `..._APPELLANT_S_BRIEF_8.pdf` | [X] REVIEWED | **HIGH - COMPLETE** |
| 33 | **Respondent's Brief (U.S. Tires)** | `..._RESPONDENT_S_BRIEF_11.pdf` | [X] REVIEWED | **HIGH - COMPLETE** |
| 34 | **Respondent's Brief (Gonzales Plaintiffs)** | `..._RESPONDENT_S_BRIEF_15.pdf` | [X] REVIEWED | **HIGH - COMPLETE** |

##### APPELLATE MOTIONS & ORDERS
| # | Document | File | Status |
|---|----------|------|--------|
| 35 | Letter Request | `..._LETTER_REQUEST_FOR__9.pdf` | [ ] |
| 36 | Affirmation | `..._AFFIRMATION_AFFIDAV_10.pdf` | [ ] |
| 37 | Notice of Motion | `..._NOTICE_OF_MOTION_W__5.pdf` | [ ] |
| 38 | Notice of Motion | `..._NOTICE_OF_MOTION_W__12.pdf` | [ ] |
| 39 | Order | `..._ORDER_14.pdf` | [ ] |
| 40 | Letter Request | `..._LETTER_REQUEST_FOR__16.pdf` | [ ] |
| 41 | Order | `..._ORDER_17.pdf` | [ ] |
| 42 | Letter Request | `..._LETTER_REQUEST_FOR__18.pdf` | [ ] |
| 43 | Order | `..._ORDER_19.pdf` | [ ] |
| 44 | Notice of Motion | `..._NOTICE_OF_MOTION_W__21.pdf` | [ ] |
| 45 | Notice of Motion | `..._NOTICE_OF_MOTION_W__25.pdf` | [ ] |
| 46 | Order | `..._ORDER_26.pdf` | [ ] |
| 47 | Order | `..._ORDER_27.pdf` | [ ] |

##### APPELLATE DIVISION DECISIONS
| # | Document | File | Status | Priority | Notes |
|---|----------|------|--------|----------|-------|
| 48 | **Aybar III - Decision and Order (Nov. 2, 2022)** | `..._DECISION_AND_ORDER_30.pdf` | [X] REVIEWED | **HIGH** | **SPECIFIC JURISDICTION FOUND** - Third-party action; CPLR 302(a)(1) analysis |

**IMPORTANT NOTE ON AYBAR DECISIONS:**
This case file contains documents from **three related Aybar actions**:
- **Aybar I** (169 AD3d 137, aff'd 37 NY3d 274): Direct action by plaintiffs vs. Ford/Goodyear. NO jurisdiction (consent-by-registration rejected).
- **Aybar II** (175 AD3d 1373): Aybar vs. Goodyear direct. NO jurisdiction (same holding).
- **Aybar III** (this decision - Nov. 2022): US Tires third-party action vs. Ford/Goodyear. **SPECIFIC JURISDICTION EXISTS** under CPLR 302(a)(1).

##### LEAVE TO APPEAL MOTIONS (to Court of Appeals)
| # | Document | File | Status |
|---|----------|------|--------|
| 49 | Notice of Motion (Leave) | `..._NOTICE_OF_MOTION_W__31.pdf` | [ ] |
| 50 | Notice of Motion (Leave) | `..._NOTICE_OF_MOTION_W__32.pdf` | [ ] |
| 51 | Affidavit | `..._AFFIDAVIT_OR_AFFIRM_33.pdf` | [ ] |
| 52 | Letter Request | `..._LETTER_REQUEST_FOR__34.pdf` | [ ] |
| 53 | Affidavit | `..._AFFIDAVIT_OR_AFFIRM_35.pdf` | [ ] |
| 54 | Affidavit | `..._AFFIDAVIT_OR_AFFIRM_36.pdf` | [ ] |
| 55 | Memorandum of Law | `..._MEMORANDUM_OF_LAW_37.pdf` | [ ] |
| 56 | Memorandum of Law | `..._MEMORANDUM_OF_LAW_38.pdf` | [ ] |
| 57 | Consent to Change Attorney | `..._CONSENT_TO_CHANGE_A_41.pdf` | [ ] |
| 58 | Exhibits | `..._EXHIBIT_S__42.pdf` | [ ] |
| 59 | Affirmation | `..._AFFIRMATION_AFFIDAV_43.pdf` | [ ] |
| 60 | Notice of Motion | `..._NOTICE_OF_MOTION_W__44.pdf` | [ ] |
| 61 | Letter of Withdrawal | `..._LETTER_OF_WITHDRAWAL_45.pdf` | [ ] |
| 62 | Notice of Motion | `..._NOTICE_OF_MOTION_W__46.pdf` | [ ] |
| 63 | Letter of Withdrawal | `..._LETTER_OF_WITHDRAWAL_47.pdf` | [ ] |
| 64 | Notice of Motion (Trial Court) | `703632_2017_..._NOTICE_OF_MOTION_88.pdf` | [ ] |

---

#### LEVEL 3: COURT OF APPEALS
**Decision:** 37 N.Y.3d 274 (2021)
**Location:** `court_of_appeals_decision.txt`

| # | Document | File | Status | Priority |
|---|----------|------|--------|----------|
| 65 | **Court of Appeals Decision** | `court_of_appeals_decision.txt` | [X] REVIEWED | **HIGH - COMPLETE** |

---

---

## DOCUMENT SIZE ASSESSMENT

### Why Size Checking Matters

Before reviewing any document, the system must assess whether the document can be processed in a single pass or requires chunking. Documents exceeding the token limit will fail to process or produce incomplete results.

### Token Estimation Formula

**Formula:** `Estimated Tokens = Character Count ÷ 1.5`

For legal text, the ratio of approximately **1.5 characters per token** provides accurate estimates.

**Examples:**
| Character Count | Estimated Tokens | Needs Chunking? |
|-----------------|------------------|-----------------|
| 30,000 chars | ~20,000 tokens | No |
| 60,000 chars | ~40,000 tokens | No |
| 90,000 chars | ~60,000 tokens | **Borderline** |
| 120,000 chars | ~80,000 tokens | **Yes** |
| 200,000 chars | ~133,000 tokens | **Yes** |

### Chunking Thresholds

| Threshold | Value | Description |
|-----------|-------|-------------|
| **Safe Token Limit** | 60,000 tokens | Documents below this process reliably in single pass |
| **Max Chunk Tokens** | 40,000 tokens | Target size for each chunk when splitting |
| **Character Threshold** | ~90,000 chars | Quick file size check (60,000 × 1.5) |

### File Size Quick Reference (PDF Documents)

PDF file size correlates roughly with content volume:

| File Size | Est. Characters | Est. Tokens | Action |
|-----------|-----------------|-------------|--------|
| < 500 KB | ~50,000 | ~33,000 | **Single pass** |
| 500 KB - 1 MB | ~100,000 | ~66,000 | **May need chunking** |
| 1 - 5 MB | 100,000 - 500,000 | 66,000 - 333,000 | **Requires chunking** |
| 5 - 20 MB | 500,000+ | 333,000+ | **Requires aggressive chunking** |
| > 20 MB | 1,000,000+ | 666,000+ | **Multi-document strategy** |

**Note:** PDF file size varies significantly based on embedded images, formatting, and compression. Text-heavy PDFs are more efficient; image-heavy PDFs may have fewer tokens than their size suggests.

### Pre-Review Size Check Procedure

Before reading any document for review:

1. **Check file size** using `ls -lh` or file properties
2. **Apply quick estimate:**
   - PDF < 500 KB → Proceed with single-pass review
   - PDF 500 KB - 1 MB → Check character count before proceeding
   - PDF > 1 MB → Plan chunking strategy before reading
3. **For borderline cases**, read the first portion and estimate total character count
4. **Document chunking plan** in the session log before beginning

### Chunking Configuration

When chunking is required, use these configurations:

```python
# Default configuration for legal documents
LEGAL_CHUNKING_CONFIG = {
    'enabled': True,
    'safe_token_limit': 60000,
    'max_chunk_tokens': 40000,
    'chars_per_token': 1.5,
    'split_strategy': 'legal_sections',  # Preferred for legal documents
    'merge_strategy': 'structured',
    'overlap_tokens': 200  # Preserve context between chunks
}
```

**Split Strategies (in order of preference for legal documents):**
1. **legal_sections** - Splits on section headers (Point I, Point II, etc.)
2. **paragraphs** - Splits on paragraph boundaries
3. **pages** - Splits on page breaks (if detectable)
4. **characters** - Last resort: splits on character count with overlap

**Merge Strategies:**
1. **structured** - Preserves section structure, best for motion papers
2. **concatenate** - Simple join, good for continuous narrative
3. **deduplicate** - Removes redundant insights across chunks
4. **first_valid** - Returns first successful result (for error handling)

### Chunked Review Workflow

For documents requiring chunking:

1. **Plan chunks** - Identify logical split points (sections, arguments, exhibits)
2. **Process sequentially** - Review each chunk in order
3. **Maintain context** - Reference previous chunk findings when reviewing next
4. **Track progress** - Mark chunk completion in session log
5. **Merge insights** - Consolidate insights after all chunks reviewed
6. **Deduplicate** - Remove redundant insights that appear in multiple chunks

### Programmatic Chunking Utilities

For automated document processing, use the chunking utilities:

**Location:** `Y:\LCP_v2.0\program_files\utils\`

| File | Purpose |
|------|---------|
| `unified_chunker.py` | Core chunking logic - `UnifiedChunker` singleton class |
| `chunking_registry.py` | Configuration registry and default settings |

**Key Functions:**

```python
from utils.unified_chunker import UnifiedChunker
from utils.chunking_registry import ChunkingRegistry

chunker = UnifiedChunker()
registry = ChunkingRegistry()
config = registry.get_config('legal_document')

# Check if document needs chunking
needs_chunking = chunker.needs_chunking(
    text=document_text,
    config=config,
    prompt_overhead=2000,  # Reserve tokens for prompt
    template_text=""
)

# Estimate tokens
estimated_tokens = chunker.estimate_tokens(
    text=document_text,
    chars_per_token=1.5
)

# Split if needed
if needs_chunking:
    result = chunker.split_text(text=document_text, config=config)
    chunks = result.chunks  # List of text chunks

# Merge results from chunked processing
merged = chunker.merge_results(
    results=chunk_results,  # List of results from each chunk
    config=config
)
```

---

### CHUNKING STRATEGY FOR JOINT RECORDS

The two Joint Record on Appeal files are extremely large (33 MB and 65 MB) and contain 400+ pages each. These compile all trial court documents into appellate record format.

**Size Analysis:**
| File | Size | Est. Characters | Est. Tokens | Chunking Required |
|------|------|-----------------|-------------|-------------------|
| Joint Record Vol. 1 | 33 MB | ~5,000,000+ | ~3,333,000+ | **YES - Aggressive** |
| Joint Record Vol. 2 | 65 MB | ~10,000,000+ | ~6,666,000+ | **YES - Aggressive** |

**Recommended Approach:**
1. **Initial Scan:** Use PDF reader to identify table of contents/index if available
2. **Chunking by Document Type:** Extract and review in logical segments:
   - Pleadings (Complaint, Answer)
   - Motion papers (Notices of Motion, Affirmations, Memoranda)
   - Affidavits/Exhibits
   - Transcripts (if any)
   - Orders/Decisions
3. **Priority Documents:** Focus on memoranda of law and court decisions first
4. **Cross-Reference:** Use appellate briefs to identify key record citations
5. **Duplicate Avoidance:** The trial court motion papers in `seq_017_and_019_lack_of_personal_jurisdiction/` may duplicate content in the Joint Records. Review standalone files first to avoid redundancy.

**Chunking Plan for Joint Records:**
```
Volume 1 (33 MB) - Target: 8-10 chunks
├── Chunk 1: Table of Contents + Pleadings
├── Chunk 2: Motion Papers (Notices of Motion)
├── Chunk 3: Affirmations in Support
├── Chunk 4: Affidavits and Declarations
├── Chunk 5: Exhibits A-E
├── Chunk 6: Exhibits F-J
├── Chunk 7: Opposition Papers
├── Chunk 8: Reply Papers
└── Chunk 9: Orders and Decisions

Volume 2 (65 MB) - Target: 15-20 chunks
├── Similar structure, larger segments
└── May contain additional trial court record
```

---

## REVIEW_PROGRESS

### Completed Reviews
| Date | Case | Motion Type | Documents Reviewed | Insights Added |
|------|------|-------------|-------------------|----------------|
| 2026-01-02 | Aybar v. Ford/Goodyear | MTD Personal Jurisdiction | Court of Appeals Decision (37 N.Y.3d 274) | 38 insights |
| 2026-01-02 | Aybar v. Ford/Goodyear | MTD Personal Jurisdiction | Aybar III - AD Decision (Nov. 2022) | 22 insights |
| 2026-01-02 | Aybar v. Ford/Goodyear | MTD Personal Jurisdiction | Appellant's Brief 8 (Ford/Goodyear) | ~87 insights |
| 2026-01-02 | Aybar v. Ford/Goodyear | MTD Personal Jurisdiction | Respondent's Brief 11 (U.S. Tires) | 69 insights |
| 2026-01-02 | Aybar v. Ford/Goodyear | MTD Personal Jurisdiction | Respondent's Brief 15 (Gonzales Plaintiffs) | 14 insights |

### Session Log
| Date | Session Notes |
|------|---------------|
| 2026-01-02 | Protocol created for Motion to Dismiss for Lack of Personal Jurisdiction. Ready to begin motion package review. |
| 2026-01-02 | **Aybar v. Ford Motor Co.** case materials inventoried. Complete case package includes: Trial Court (Seq 017/019), Second Department Appeal, and Court of Appeals decision. Court of Appeals decision reviewed - landmark case on consent-by-registration. Two Joint Record files (33MB, 65MB) require chunking strategy. |
| 2026-01-02 | **Court of Appeals Decision - Full Insight Extraction Complete.** Extracted: 7 Motion Arc insights, 12 Case Law Effectiveness insights, 8 Writing Style insights, 11 Strategy insights. Key holdings: (1) BCL registration = consent to service only, NOT consent to jurisdiction; (2) Bagdon reinterpreted as product of Pennoyer era; (3) Plaintiffs' fatal error was failing to preserve CPLR 302 specific jurisdiction argument. |
| 2026-01-02 | **Aybar III - Appellate Division Decision (Nov. 2022) Reviewed.** CRITICAL COMPANION CASE: Shows what happens when specific jurisdiction IS properly argued. Court found CPLR 302(a)(1) satisfied for third-party indemnification/contribution claims. Key holdings: (1) Two-prong test for 302(a)(1): transaction of business + articulable nexus; (2) "Permissive" standard - no causation required; (3) Third-party claims "tethered" to NY because alleged breach occurred in NY; (4) Due process satisfied - defendants conceded minimum contacts, failed to show unreasonableness. |
| 2026-01-02 | **Second Department Appellate Briefs - Full Review Complete.** Reviewed: (1) Appellant's Brief 8 (Ford/Goodyear - 7 chunks, ~87 insights), (2) Respondent's Brief 11 (U.S. Tires - 5 chunks, 67 pages, 69 insights), (3) Respondent's Brief 15 (Gonzales Plaintiffs - 15 pages, 14 insights). Total ~170 insights extracted across Motion Arc, Case Law, Writing Style, and Strategy categories. Key themes: targeted advertising jurisdiction, used product market theory, CPLR 302(a)(3) alternative, "original injury" theory, multi-jurisdictional Ford losses compilation, "transitory product" doctrine, burden-shifting exploitation. |
| 2026-01-02 | **Insights Integration Complete.** All pending insights integrated into instruction files at `Y:\LCP_v2.0\program_files\brief_drafting\mtd_personal_jurisdiction\`. Created: (1) MOTION_ARC.md - jurisdictional framework, statutory analysis, brief structure; (2) CASE_LAW_EFFECTIVENESS.md - case tables, distinction strategies, citation practices; (3) STRATEGY_GUIDE.md - tactics for plaintiffs and defendants; (4) opposition/argument_instructions.md - writing style, rhetorical techniques, evidence presentation. |

---

## PENDING_INSIGHTS

### Motion Arc
| Source | Insight | Status |
|--------|---------|--------|
| Aybar COA Decision | **Three Bases for Personal Jurisdiction:** (1) General jurisdiction (defendant "at home"), (2) Specific jurisdiction (claim arises from contacts), (3) Consent (forum selection clauses, stipulation, or potentially registration). Court analyzed only consent theory because plaintiffs abandoned general jurisdiction and failed to preserve specific jurisdiction. | PENDING |
| Aybar COA Decision | **Two-Component Constitutional Analysis:** Court of Appeals identifies two components of personal jurisdiction: (1) Service of process (notice and opportunity to be heard), and (2) Power/reach of court over party to enforce decrees. BCL registration satisfies only the first component. | PENDING |
| Aybar COA Decision | **Statutory Text Controls:** Court applied plain meaning analysis to BCL §§ 1301, 1304, 304 - statutes require designation of agent for service of process but do NOT condition right to do business on consent to general jurisdiction. Court refused to "read into a statute a provision which the Legislature did not see fit to enact." | PENDING |
| Aybar COA Decision | **Preservation Requirements:** Plaintiffs' failure to assert specific jurisdiction under CPLR 302 below meant that argument was unpreserved for appeal. Plaintiffs also abandoned "essentially at home" argument. CRITICAL: Always plead alternative jurisdictional bases to preserve appellate options. | PENDING |
| Aybar COA Decision | **Registration ≠ Consent to Jurisdiction:** BCL registration and designation of agent for service = consent to accept service of process in NY. It does NOT = consent to general jurisdiction. This overturns 100+ years of lower court interpretation of *Bagdon*. | PENDING |
| Aybar COA Decision | **Court Declined Constitutional Question:** Because Court resolved case on NY statutory grounds (BCL doesn't provide consent-by-registration), it expressly declined to address whether consent-by-registration, if it existed, would comport with federal due process under *Daimler*. | PENDING |
| Aybar COA Decision | **Motion Structure (from procedural history):** Ford and Goodyear filed separate motions to dismiss under CPLR 3211(a)(8). Plaintiffs opposed. Supreme Court denied motions; Appellate Division reversed; Court of Appeals affirmed Appellate Division. | PENDING |
| Aybar III AD Decision (2022) | **CPLR 302(a)(1) Two-Prong Test:** (1) Defendant must have conducted sufficient activities to have "transacted business" in NY; (2) Claims must "arise from" those transactions. First prong often conceded by major corporations doing substantial NY business. Second prong is where battles are fought. | PENDING |
| Aybar III AD Decision (2022) | **"Articulable Nexus" Standard:** Second prong requires "articulable nexus" or "substantial relationship" between cause of action (or element thereof) and defendant's NY business transactions. This is a "relatively permissive" inquiry - does NOT require causation. | PENDING |
| Aybar III AD Decision (2022) | **Claim Need Not Be "Unmoored":** There must be "a relatedness between the transaction and the legal claim such that the latter is not completely unmoored from the former, regardless of the ultimate merits of the claim." Claims that are "too attenuated" or "merely coincidental" fail. | PENDING |
| Aybar III AD Decision (2022) | **Third-Party Claims Can Establish Nexus:** Third-party indemnification/contribution claims "could not exist but for" the defendant's alleged negligence in NY - this "tethers" the claims to NY and satisfies the articulable nexus requirement even when underlying accident occurred elsewhere. | PENDING |
| Aybar III AD Decision (2022) | **Due Process Two-Part Analysis:** Even if CPLR 302 is satisfied, must separately analyze: (1) "Minimum contacts" - defendant should reasonably anticipate being haled into NY court; (2) "Reasonableness" - five-factor fair play and substantial justice test. | PENDING |
| Aybar III AD Decision (2022) | **Five-Factor Reasonableness Test:** (1) Burden on defendant; (2) Forum state's interest in adjudicating; (3) Plaintiff's interest in convenient/effective relief; (4) Interstate system's efficiency interest; (5) States' shared interest in substantive social policies. | PENDING |
| Aybar III AD Decision (2022) | **Burden Shift on Reasonableness:** "Where minimum contacts exist, the defendant has the burden to present a compelling case that the presence of some other considerations would render jurisdiction unreasonable." Defendants rarely meet this burden. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Counter Questions Presented Format:** When opposing appellant's questions presented, use "Counter Questions Presented" that reframe issues favorably. Example: "Whether there is personal jurisdiction over Ford and Goodyear pursuant to CPLR § 302(a)(1), where they concede that they 'transact business' in New York..." Embeds opponent's concessions into the question itself. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **First Prong Concession Exploitation:** When opponent concedes first prong of CPLR 302(a)(1) (transacting business), structure entire argument around narrowing dispute to second prong only. Opens argument with: "Ford and Goodyear concede... the only issue in dispute is the second prong." | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Statutory Text Inclusion:** Include actual statutory text in argument section. Respondent quotes full CPLR 302(a)(1): "a court may exercise personal jurisdiction over any nondomiciliary... who in person or through an agent: 1. transacts any business within the state or contracts anywhere to supply goods or services in the state." | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **CPLR 302(a)(3) Alternative Argument:** Even when 302(a)(1) appears strong, plead 302(a)(3) as alternative. Requires showing: (1) tortious act outside NY, (2) injury inside NY, (3) defendant derives substantial revenue from interstate commerce. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **"Original Injury" Theory:** For out-of-state accidents involving NY residents who purchased products in NY, argue the "original event" giving rise to injury was the NY purchase of defective product. *Singer v. Walker* doctrine: "the place of the original event which caused the injury rather than the place of the resulting injury." | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Legislative History for 302(a)(3):** Senate Committee reports show NY legislature "intended that tortious conduct without the state causing injury within the state shall be a predicate for long-arm jurisdiction whether or not the defendant had other contacts with the forum." | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Five-Factor Due Process Test Structure:** Organize Point II (Due Process) around the five-factor reasonableness test: (1) burden on defendant, (2) forum state's interest, (3) plaintiff's interest in convenient relief, (4) interstate system's efficiency, (5) shared interest in substantive policies. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Multi-Factor Case Distinction Template:** When distinguishing opponent's cases, attack on multiple independent grounds: (1) plaintiff residency differences, (2) purchase location, (3) basis of claim, (4) type of action (class vs. individual), (5) claims asserted. Each distinction independently undermines applicability. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Burden-Shifting Exploitation:** Once minimum contacts established, shift burden to defendant and note their failure: "Ford and Goodyear, however, have not even attempted to make that showing." Converts silence into argument. | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **Adoption/Incorporation Technique:** Co-respondent brief opens by stating it "adopt[s] and join[s] in the arguments contained in [co-respondent's] brief." Allows comprehensive coverage without duplication, keeps brief focused on unique contributions. | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **Third-Party Action Context:** Argues *Daimler* "and its progeny have not specifically addressed third-party actions, leaving a void which the Court must fill." Where jurisdiction is established among initial parties, different/lower standard may apply for impleaded defendants. | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **"Exceptional Circumstances" Carve-Out:** Proposes courts "characterize cases such as this...as an 'exceptional circumstance', thereby moderating the harsh jurisdictional constraints of Daimler." Creates doctrinal escape valve. | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **Consent Jurisdiction via Registration:** Argues voluntary business registration + appointment of agent for service of process = consent to general jurisdiction. "The act of registering to do business in New York must be held to be consent to be sued in New York courts by New Yorkers." | PENDING |

### Case Law Effectiveness
| Source | Case Cited | Outcome | Why | Status |
|--------|-----------|---------|-----|--------|
| Aybar COA Decision | *Bagdon v. Philadelphia & Reading Coal & Iron Co.*, 217 NY 432 (1916) | **REINTERPRETED/LIMITED** | Majority held Bagdon only addressed effect of service on designated agent, not that registration constitutes consent to general jurisdiction. Bagdon was decided under Pennoyer's territorial approach; its analysis of "effect of service" must be understood in that historical context. | PENDING |
| Aybar COA Decision | *Daimler AG v. Bauman*, 571 US 117 (2014) | **HIGHLY EFFECTIVE - ADOPTED** | Leading SCOTUS case limiting general jurisdiction to where corporation is "at home" (place of incorporation or principal place of business). Court noted Daimler characterized "doing business" standard as "unacceptably grasping." | PENDING |
| Aybar COA Decision | *Goodyear Dunlop Tires v. Brown*, 564 US 915 (2011) | **HIGHLY EFFECTIVE - ADOPTED** | SCOTUS case establishing that general jurisdiction exists only where corporation's "affiliations with the State are so continuous and systematic as to render them essentially at home." | PENDING |
| Aybar COA Decision | *International Shoe Co. v. Washington*, 326 US 310 (1945) | **FOUNDATIONAL - ADOPTED** | "Transformative decision" that replaced Pennoyer's territorial approach with minimum contacts analysis. Court emphasized this was a "momentous departure" that changed the personal jurisdiction framework. | PENDING |
| Aybar COA Decision | *Tauza v. Susquehanna Coal Co.*, 220 NY 259 (1917) | **DISTINGUISHED** | Majority explained Tauza (also by Cardozo) addressed jurisdiction based on corporate presence/doing business, not consent. The "essential thing" in both Bagdon and Tauza was corporate presence in NY. | PENDING |
| Aybar COA Decision | *Pennoyer v. Neff*, 95 US 714 (1878) | **HISTORICAL CONTEXT** | Court explained Bagdon was decided under Pennoyer's territorial approach where in-state service on a present defendant was sufficient for jurisdiction. This historical context is key to reinterpreting Bagdon. | PENDING |
| Aybar COA Decision | *Pennsylvania Fire Ins. Co. v. Gold Issue Mining*, 243 US 93 (1917) | **CITED BY DISSENT** | Dissent cited as SCOTUS case upholding consent-by-registration. Majority did not address. | PENDING |
| Aybar COA Decision | *Neirbo Co. v. Bethlehem Shipbuilding Corp.*, 308 US 165 (1939) | **CITED BY DISSENT** | Dissent cited as SCOTUS case affirming that "consent through corporate registration is a valid and constitutional basis for general jurisdiction." Majority did not address. | PENDING |
| Aybar COA Decision | *Keane v. Kamin*, 94 NY2d 263 (1999) | **SUPPORTING** | Cited for two-component analysis of personal jurisdiction: (1) service of process (notice), (2) power/reach over party. | PENDING |
| Aybar COA Decision | *Flick v. Stewart-Warner Corp.*, 76 NY2d 50 (1990) | **SUPPORTING** | Cited for proposition that service on foreign corporation's designated agent is "equivalent of actual service" - but Court emphasized this addressed service, not jurisdiction. | PENDING |
| Aybar COA Decision | *BNSF R. Co. v. Tyrrell*, 581 US ___ (2017) | **SUPPORTING** | SCOTUS case confirming Daimler's limits on general jurisdiction; Court noted SCOTUS held neither general nor specific jurisdiction existed "absent consent." | PENDING |
| Aybar COA Decision | *Ford Motor Co. v. Montana Eighth Judicial Dist. Court*, 592 US ___ (2021) | **CONTEMPORARY CONTEXT** | 2021 SCOTUS case on specific jurisdiction cited by dissent to note that specific jurisdiction has "rapidly expanded" while general jurisdiction has been limited. | PENDING |
| Aybar III AD (2022) | *Rushaid v. Pictet & Cie*, 28 NY3d 316 (2016) | **KEY - ADOPTED** | Court of Appeals case establishing that CPLR 302(a)(1) inquiry is "relatively permissive" and "does not require causation." Critical for opposing MTD - lower bar than defendants argue. | PENDING |
| Aybar III AD (2022) | *D&R Global Selections v. Bodega Olegario Falcon Pineiro*, 29 NY3d 292 (2017) | **KEY - ADOPTED** | "Articulable nexus" or "substantial relationship" standard. Also confirms two-part due process analysis (minimum contacts + reasonableness). | PENDING |
| Aybar III AD (2022) | *Licci v. Lebanese Can. Bank*, 20 NY3d 327 (2012) | **SUPPORTING** | Claims are "too attenuated" or "merely coincidental" with NY transactions when nexus lacking. Useful for both movants and opponents to frame arguments. | PENDING |
| Aybar III AD (2022) | *Fischbarg v. Doucet*, 9 NY3d 375 (2007) | **SUPPORTING** | "Jurisdiction under CPLR 302(a)(1) is proper even though the defendant never enters New York, so long as the defendant's activities here were purposeful and there is a substantial relationship between the transaction and the claim." | PENDING |
| Aybar III AD (2022) | *LaMarca v. Pak-Mor Mfg. Co.*, 95 NY2d 210 (2000) | **KEY - DUE PROCESS** | Establishes that once minimum contacts shown, defendant bears burden to show jurisdiction is unreasonable. Critical for burden-shifting argument. | PENDING |
| Aybar III AD (2022) | *Williams v. Beemiller, Inc.*, 33 NY3d 523 (2019) | **SUPPORTING** | Minimum contacts require "something more than the fortuitous circumstance that a product sold in another state later makes its way into the forum jurisdiction." | PENDING |
| Aybar III AD (2022) | *Ford Motor Co. v. Montana Eighth Jud. Dist. Ct.*, 141 S Ct 1017 (2021) | **HIGHLY EFFECTIVE** | SCOTUS case on specific jurisdiction - cited extensively by Aybar III. Supports broad specific jurisdiction where defendant "serve[d] a market" in forum state. | PENDING |
| Aybar III AD (2022) | *Fernandez v. DaimlerChrysler, AG*, 143 AD3d 765 (2d Dept 2016) | **DISTINGUISHED** | Case where no nexus found - defendant didn't manufacture subject vehicle or defective parts. Distinguished because here Ford/Goodyear DID manufacture the products. | PENDING |
| Aybar III AD (2022) | *Krajewski v. Osterlund, Inc.*, 111 AD2d 905 (2d Dept 1985) | **DISTINGUISHED** | No nexus where defendant didn't manufacture vehicle in question. Distinguished because here defendants actually made the allegedly defective products. | PENDING |
| Aybar III AD (2022) | *Pichardo v. Zayas*, 122 AD3d 699 (2d Dept 2014) | **DISTINGUISHED** | Court looked to "situs of the cause of action" - contract made in NY but negligence occurred in NJ, so no nexus. Distinguished because here alleged breach (negligent inspection) occurred IN NY. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Licci v. Lebanese Can. Bank*, 20 NY3d 327 (2012) | **KEY - ADOPTED** | Establishes "articulable nexus" standard is "relatively permissive" - does NOT require causation. Opponent cited for restrictive reading but respondent successfully argued Licci supports broad construction. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Singer v. Walker*, 21 AD2d 285 (1st Dept 1964) | **EFFECTIVE FOR CPLR 302(a)(3)** | "Place of the original event which caused the injury rather than the place of the resulting injury" controls situs of injury analysis. Supports argument that NY purchase of defective product = NY injury for 302(a)(3). | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Hamilton v. Accu-Tek*, 935 F.Supp. 1307 (E.D.N.Y. 1996) | **EFFECTIVE - Advertising Jurisdiction** | Gun manufacturers subject to NY jurisdiction based on targeted advertising. "Defendants have directed their sales and advertising toward the New York market, and may therefore be brought into court in New York." Applied to show targeted advertising creates jurisdiction. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *State Farm v. Swizz Style, Inc.*, 2017 WL 1034670 (E.D.N.Y. 2017) | **EFFECTIVE - Hispanic Advertising** | Defendants subject to NY jurisdiction where they "targeted the New York market, specifically its Hispanic population." Key for showing demographic-targeted advertising establishes purposeful availment. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Robins v. Procure Treatment Centers*, 179 Misc.2d 345 (Sup.Ct. Nassau 1998) | **SUPPORTING** | Defendants who invest millions in advertising to NY residents "with the specific purpose of attracting the patronage of forum residents should not be heard to complain when served with process in that jurisdiction." | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Thomas v. Ford Motor Co.*, 2019 WL 4251615 (Ill.App. 2019) | **EFFECTIVE - Ford Lost** | Illinois appellate court found specific jurisdiction over Ford in product liability case. Part of multi-jurisdictional compilation showing Ford's consistent losses on jurisdiction. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Michelin N.A., Inc. v. De Santiago*, 2019 WL 2223410 (Tex.App. 2019) | **KEY - "Tire Hit Its Target"** | Texas court: "The used status of the tire does not disconnect Michelin from this lawsuit... Regardless of whether a 'new' or 'used' product was involved, Michelin's tire hit its target—a Texas consumer." Devastating for "new vs. used" distinction argument. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Bandemer v. Ford Motor Co.*, 931 N.W.2d 744 (Minn. 2019) | **CRITICAL - SCOTUS CERT GRANTED** | Minnesota Supreme Court found specific jurisdiction over Ford. US Supreme Court granted certiorari - signals SCOTUS interest in resolving specific jurisdiction standards. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Ford Motor Co. v. Montana Eighth Judicial Dist.*, SCOTUS No. 19-368 | **SCOTUS CERT GRANTED** | Companion case to Bandemer. SCOTUS consolidated review of specific jurisdiction over vehicle manufacturers. These cases became *Ford v. Montana* (2021). | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Antonini v. Ford Motor Co.*, 2017 WL 3084853 (Pa.Ct.C.P. 2017) | **EFFECTIVE - "Directly Enticed"** | Pennsylvania court found Ford "directly enticed" plaintiff through targeted advertising in forum. Applied to establish advertising-based jurisdiction for used product market. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Griffin v. Ford Motor Co.* (unreported, Fla.) | **EFFECTIVE - Chrysler Canada** | Chrysler Canada subject to Florida jurisdiction because it assembled vehicles for national distribution, invoking World-Wide Volkswagen language about subjecting defendant to suit where "defective merchandise has there been the source of injury." | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Erwin v. Ford Motor Co.*, 2016 WL 7655398 (M.D. Fla. 2016) | **DISTINGUISHED** | Distinguished on three grounds: (1) plaintiff was Ohio resident living part-time in Florida, (2) didn't purchase in forum state, (3) claim didn't arise from forum advertising. Shows how to distinguish adverse authority. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Schmitigal v. Twohig*, 2019 WL 4689228 (D.S.C. 2019) | **VACATED** | Decision "subsequently vacated and dismissed based on lack of subject matter jurisdiction." Demonstrates value of checking case history - opponent's citation was invalid. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *Kommer v. Ford Motor Co.*, 2019 WL 2895384 (N.D.N.Y. 2019) | **DISTINGUISHED** | Distinguished: class action (fundamentally different), no NY state law claims, only 1 of 4 plaintiffs was NY resident, vehicles not sold in NY. Multiple distinguishing factors. | PENDING |
| Respondent's Brief 11 (U.S. Tires) | *D & R Glob. Selections v. Bodega Olegario Falcon Pineiro*, 29 N.Y.3d 292 (2017) | **KEY - Burden Shifting** | Establishes once minimum contacts shown, defendant must "present a compelling case that the presence of some other considerations would render jurisdiction unreasonable." | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | *Daimler A.G. v. Bauman*, 571 U.S. 117 (2014) | **ACKNOWLEDGED BUT DISTINGUISHED** | Brief acknowledges Daimler limits general jurisdiction but argues: (1) creates "two-sided coin" problem, (2) doesn't address third-party actions, (3) consent jurisdiction separate, (4) "exceptional circumstances" possible. | PENDING |

### Writing Style
| Source | Category | Insight | Target File | Status |
|--------|----------|---------|-------------|--------|
| Aybar COA Decision | Opinion Structure (Majority) | **Issue Framing First:** Opens by clarifying exactly what IS and IS NOT before the court. "To begin, we clarify what issues are—and are not—presented here." Then explicitly lists preserved vs. unpreserved/abandoned arguments. | mtd_pj_motion_master.md | PENDING |
| Aybar COA Decision | Statutory Interpretation | **Plain Text Analysis:** "A different reading would improperly amend the statute by adding words that are not there" and "would impermissibly read into a statute a provision which the Legislature did not see fit to enact." Emphasizes what statute DOES say vs. what it DOESN'T say. | argument_instructions.md | PENDING |
| Aybar COA Decision | Historical Context Framing | **Recontextualization Technique:** Rather than overruling Bagdon, Court reinterprets it by placing it in "the context of the controlling jurisprudence of the time." Shows how precedent was decided under different legal framework (Pennoyer) that no longer applies. | argument_instructions.md | PENDING |
| Aybar COA Decision | Analytical Progression | **Step-by-Step Framework:** (1) State the statute's plain terms, (2) Analyze leading precedent in historical context, (3) Apply modern framework, (4) Decline to reach unnecessary constitutional questions. | mtd_pj_motion_master.md | PENDING |
| Aybar COA Decision | Dissent Structure | **Historical Narrative:** Dissent uses extensive historical narrative starting from 1819 (*M'Queen v. Middletown Mfg. Co.*) to show legislative intent. Traces evolution of corporate jurisdiction law through multiple eras. Effective for arguing legislative intent. | argument_instructions.md | PENDING |
| Aybar COA Decision | Dissent Rhetorical Technique | **"Means vs. Ends" Argument:** Dissent argues majority "confused the means for the end" - legislature used "service" as mechanism to achieve "jurisdiction." Powerful reframing technique for statutory interpretation disputes. | argument_instructions.md | PENDING |
| Aybar COA Decision | Citation Practice | **Parenthetical Explanations:** Court uses detailed parentheticals to explain relevance of cited cases, e.g., "Daimler, 571 US at 128, quoting Goodyear, 564 US at 925" with explanation of holding. | argument_instructions.md | PENDING |
| Aybar COA Decision | Limiting Language | **Explicit Non-Holdings:** Court explicitly states what it is NOT deciding: "we have no occasion to address whether consent-by-registration, if it existed in New York, would comport with federal due process under Daimler." | mtd_pj_motion_master.md | PENDING |
| Aybar III AD (2022) | Opinion Structure | **Clear Issue Statement:** Opens with precise framing: "This appeal presents the question of whether specific personal jurisdiction exists over the third-party defendants, two out-of-state corporations, pursuant to New York State's long-arm statute, CPLR 302(a)(1)." Identifies exact statutory basis. | mtd_pj_opposition_master.md | PENDING |
| Aybar III AD (2022) | Procedural History | **Multi-Case Context:** Provides detailed procedural history of all three related Aybar cases, explaining how this case differs. Shows importance of understanding full litigation context. | mtd_pj_opposition_master.md | PENDING |
| Aybar III AD (2022) | Legal Framework Organization | **Statutory → Due Process Structure:** Organizes analysis as: (A) Statutory Framework (CPLR 302 text and two-prong test), then (B) Application of the Law (first CPLR 302, then Due Process). Systematic approach. | argument_instructions.md | PENDING |
| Aybar III AD (2022) | Distinguishing Cases | **Effective Case Distinction:** Distinguishes *Fernandez*, *Krajewski*, and *Pichardo* by identifying specific factual differences (defendant didn't manufacture product vs. did manufacture; breach occurred outside NY vs. in NY). | argument_instructions.md | PENDING |
| Aybar III AD (2022) | Concession Leverage | **Using Opponent's Concessions:** "In this case, Ford and Goodyear concede that the first prong of CPLR 302(a)(1) is satisfied." Court uses defendants' concession to narrow the dispute and focus argument. | argument_instructions.md | PENDING |
| Aybar III AD (2022) | "Tethered" Language | **Nexus Framing:** Uses "tethered" metaphor to describe relationship between claims and NY: "the third-party claims for indemnification and contribution are therefore, tethered." Effective imagery for establishing connection. | argument_instructions.md | PENDING |
| Aybar III AD (2022) | Burden Emphasis | **Shifting Burden Back:** Emphasizes that once minimum contacts exist, defendants bear burden to show unreasonableness - and notes they "failed to present any compelling argument." Effective for opposition briefs. | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Rhetorical Attack | **"Slender Reed" Rhetoric:** Characterizing opponent's best argument as a "slender reed." Effective dismissive metaphor for thin legal arguments. | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Attack Language | **"Brazenly Deny" Attack:** "Their motion papers brazenly deny having any contacts with the forum other than..." Strong language highlighting opponent's overreach in denial. | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Concession Lists | **Bullet Point Concession Lists:** Present opponent's concessions as itemized bullet points for visual impact. Makes admissions undeniable and easy for court to reference. | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Quantification | **Advertising Spend Quantification:** Ford's $2.28 billion annual advertising expenditure, 17% ($372 million) on Hispanic advertising. Concrete numbers demonstrate magnitude of purposeful availment. | statement_of_facts_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Verb Accumulation | **Sophisticated Verb Accumulation:** "created, orchestrated, nurtured and sustained the commercial environment or conditions needed to induce" - building momentum through synonymous verbs. | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Dismissive Phrase | **"Of No Moment" Dismissive:** Classic legal phrase for dismissing opponent's arguments: "That they did not directly sell the products or pull the proverbial trigger themselves, is of no moment given their culpability..." | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Multi-Jurisdictional Survey | **Ford Loss Compilation:** Lists 13+ jurisdictions where Ford lost jurisdiction arguments (Illinois, Florida, Texas, Minnesota, Tennessee, Montana, Pennsylvania, Georgia, Oklahoma, Missouri, Washington, New Mexico, California). Powerful pattern evidence. | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Quote Integration | **"Tire Hit Its Target" Quote:** Adopting vivid language from favorable precedent: "Regardless of whether a 'new' or 'used' product was involved, Michelin's tire hit its target—a Texas consumer." | argument_instructions.md | PENDING |
| Respondent's Brief 11 (U.S. Tires) | Conclusion Format | **Brief Conclusion Format:** Short, direct: "For all the foregoing reasons, as well as those set forth in U.S. Tires' papers below, it is respectfully requested that this Honorable Court affirm..." Incorporates lower court papers by reference. | argument_instructions.md | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | Metaphors | **"Two-Sided Coin" and "Smell Test" Metaphors:** Accessible metaphors for constitutional analysis. Daimler is "a two-sided coin" and opponent's position does "not seem to pass the proverbial smell test for constitutional fairness." | argument_instructions.md | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | Hypothetical | **George Washington Bridge Hypothetical:** "Whether the product failure happens in the westbound lanes or the eastbound lanes of the George Washington Bridge should not be the sole determining factor over jurisdiction." Reduces opponent's position to geographic formalism. | argument_instructions.md | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | Label Agnosticism | **Jurisdictional Label Agnosticism:** "The precise labeling of such jurisdiction should not be determinative. Whether this is labeled general... or specific... or 'modified' general jurisdiction, or an exceptional circumstance..." Invites court to find any doctrinal path. | argument_instructions.md | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | Practical Absurdity | **Multi-Forum Litigation Absurdity:** Argues dismissal would require "separate lawsuits in Ohio (Goodyear's home state) and Michigan (Ford's home state)" plus "Kentucky" where tire was manufactured. "These results are ludicrous, the product of form over substance." | argument_instructions.md | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | Attack Phrase | **"Jurisdictional Crapshoots" Attack:** "Goodyear wishes to turn actions, including third-party actions, into jurisdictional crapshoots, where the situs of original sale only becomes known after suit is commenced." Vivid critique of information asymmetry. | argument_instructions.md | PENDING |

### Strategy
| Source | Insight | Movant/Opponent | Status |
|--------|---------|-----------------|--------|
| Aybar COA Decision | **Plain Text Statutory Argument Prevailed:** Defendants successfully argued BCL's plain text doesn't condition right to do business on consent to jurisdiction. Court applied strict statutory construction - if legislature wanted consent-by-registration, it would have said so. | Movant (Defendant) | PENDING |
| Aybar COA Decision | **Historical Recontextualization Won:** Defendants successfully reframed Bagdon as a product of its time (Pennoyer era) rather than binding precedent on consent-to-jurisdiction. Court adopted this "Bagdon was about service, not jurisdiction" argument. | Movant (Defendant) | PENDING |
| Aybar COA Decision | **CRITICAL FAILURE - Plaintiffs Failed to Preserve Alternatives:** Plaintiffs "concede[d] that they did not assert below that New York courts had specific jurisdiction over Ford and Goodyear under New York's long-arm statute, CPLR 302." Also "abandoned" essentially-at-home argument. Left only consent theory. | Opponent (Plaintiff) - LESSON | PENDING |
| Aybar COA Decision | **Always Plead Multiple Jurisdictional Bases:** When opposing MTD for lack of personal jurisdiction, ALWAYS argue: (1) general jurisdiction (at home), (2) specific jurisdiction under CPLR 302, AND (3) consent theories. Preserve all arguments even if some seem weaker. | Opponent (Plaintiff) - LESSON | PENDING |
| Aybar COA Decision | **Leverage SCOTUS Trends:** Defendants effectively used Daimler/Goodyear trend of limiting general jurisdiction to support narrow reading of consent-by-registration. Even though those cases don't directly address consent, they inform interpretive approach. | Movant (Defendant) | PENDING |
| Aybar COA Decision | **Dissent's Counter-Strategy (Failed Here):** Dissent argued: (1) 150 years of consistent interpretation, (2) legislative acquiescence, (3) reliance interests of litigants, (4) SCOTUS has repeatedly carved out consent from jurisdiction limits. These arguments lost 5-2 but may succeed in other contexts. | Opponent (Plaintiff) | PENDING |
| Aybar COA Decision | **Due Process Escape Hatch:** Court declined to address constitutional question. If legislature amends BCL to expressly provide consent-by-registration, constitutional challenge would still be available. Defendants preserved this fallback. | Movant (Defendant) | PENDING |
| Aybar COA Decision | **Forum Selection as Alternative:** Court noted that parties can consent to jurisdiction through "forum-selection agreements" - suggesting defendants should ensure contracts include forum selection clauses in their favor, and plaintiffs should negotiate for favorable forums. | Both Sides | PENDING |
| Aybar COA Decision | **Post-Aybar Landscape:** After this decision, consent-by-registration is NOT available in NY. Plaintiffs must establish: (1) defendant is "at home" in NY (rare for out-of-state corporations), OR (2) specific jurisdiction under CPLR 302 (claim arises from NY contacts), OR (3) contractual consent. | Both Sides - Framework | PENDING |
| Aybar COA Decision | **Burden Dynamics:** Plaintiff bears burden of establishing jurisdiction. On MTD, court considers affidavits and gives plaintiff benefit of all reasonable inferences - but plaintiff must actually MAKE the arguments to get the benefit. | Both Sides | PENDING |
| Aybar III AD (2022) | **Specific Jurisdiction CAN Work (Aybar III Proves It):** Where plaintiffs in Aybar I failed by not arguing CPLR 302, US Tires in Aybar III succeeded by properly arguing specific jurisdiction. Same defendants, same products, different result because correct argument was made. | Opponent (Plaintiff) - LESSON | PENDING |
| Aybar III AD (2022) | **"Permissive" Standard is Key:** Court emphasized inquiry is "relatively permissive" and "does not require causation." Opposition should hammer this language - it's a lower bar than defendants typically argue. | Opponent (Plaintiff) | PENDING |
| Aybar III AD (2022) | **Concede First Prong if Necessary:** Ford/Goodyear conceded they transacted business in NY (first prong). Major corporations doing substantial NY business may strategically concede this to focus fight on second prong. | Movant (Defendant) | PENDING |
| Aybar III AD (2022) | **"Unmoored" vs. "Tethered" Framing:** Defendants argued claims were "unmoored" from NY activities. Court rejected this, finding claims "tethered" to NY. The metaphor battle matters - opposition should use "tethered," "connected," "linked" language. | Both Sides | PENDING |
| Aybar III AD (2022) | **Situs of Breach Matters:** Court emphasized "the alleged breach occurred in New York" (the negligent tire inspection). Even when injury occurs elsewhere, if breach/conduct occurred in NY, nexus can be established. | Opponent (Plaintiff) | PENDING |
| Aybar III AD (2022) | **Third-Party Claims Analysis:** For indemnification/contribution claims, court found nexus because "third-party causes of action... could not exist but for US Tires' alleged negligence, which occurred in New York." Derivative claims trace back to NY conduct. | Opponent (Plaintiff) | PENDING |
| Aybar III AD (2022) | **Distinguish, Don't Ignore Adverse Cases:** Court carefully distinguished *Fernandez*, *Krajewski*, and *Pichardo* rather than ignoring them. Movants and opponents should directly address unfavorable precedent by identifying distinguishing facts. | Both Sides | PENDING |
| Aybar III AD (2022) | **Market Participation Argument:** Court noted Ford/Goodyear "purposely availed themselves of the New York market" and "would undoubtably benefit from the sale of replacement parts and services from third-party companies." Manufacturers who serve NY market can expect NY jurisdiction. | Opponent (Plaintiff) | PENDING |
| Aybar III AD (2022) | **Due Process Burden Shift is Powerful:** Once minimum contacts are conceded or established, burden shifts to defendant to show jurisdiction is unreasonable. Ford/Goodyear "failed to present any compelling argument" on this - defendants rarely win on reasonableness prong. | Opponent (Plaintiff) | PENDING |
| Aybar III AD (2022) | **NY Interest Argument:** Court noted "New York has an interest in adjudicating the dispute, as it is the residence of both Aybar and the defendant, US Tires, as well as the location of the alleged breach." Forum state interest is a factor in reasonableness analysis. | Opponent (Plaintiff) | PENDING |
| Aybar III AD (2022) | **No Discernible Burden for Major Corps:** Court found "no discernible difference for companies such as Ford or Goodyear whether they defend an action in New York or Virginia." Large corporations can't claim burden of defending in major commercial states. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Targeted Advertising as Jurisdictional Hook:** Ford's $2.28B annual advertising spend (17% targeting Hispanic consumers) + Goodyear's national advertising campaigns establish purposeful availment. "A manufacturer who invests millions of dollars in advertising to forum residents with the specific purpose of attracting the patronage of forum residents should not be heard to complain when served with process." | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Used Product Market Strategy:** Manufacturers who actively promote used product resale market through infrastructure (service centers, parts distribution, warranty transfers) cannot disclaim jurisdiction over used product claims. Market participation creates jurisdiction. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **"Distinction Without Jurisdictional Difference":** New vs. used product distinction is irrelevant for jurisdiction. *Michelin*: "The used status of the tire does not disconnect [manufacturer] from this lawsuit." Manufacturer's contacts don't depend on product's subsequent sales. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Multi-Jurisdictional Ford Losses Compilation:** Document Ford's consistent jurisdiction losses across 13+ states (Illinois, Florida, Texas, Minnesota, Tennessee, Montana, Pennsylvania, Georgia, Oklahoma, Missouri, Washington, New Mexico, California). Shows pattern, not isolated result. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Independent Co-Defendant's Jurisdictional Hook:** U.S. Tires' third-party claims provide independent basis for jurisdiction over Ford/Goodyear because the claims arise from alleged negligence IN New York (the tire inspection), not the out-of-state accident. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Vacated Case Attack:** Always Shepardize/KeyCite opponent's cases. Finding a case was vacated (like *Schmitigal*) is devastating - opponent's authority is simply invalid. | Both Sides | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **CPLR 302(a)(3) as Alternative:** Even when 302(a)(1) is strong, plead 302(a)(3) as fallback. For out-of-state accidents: (1) tortious act (defective design) outside NY, (2) injury inside NY (NY resident injured using NY-purchased product), (3) substantial interstate revenue. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **"Original Injury" Theory:** Argue "original event" causing injury was NY purchase of defective product, not out-of-state accident. *Singer v. Walker* places situs of injury at "original event which caused the injury rather than the place of the resulting injury." | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 11 (U.S. Tires) | **Burden Shift Exploitation:** Once minimum contacts established (or conceded), immediately pivot to burden-shifting: defendant must show "compelling case" that jurisdiction would be unreasonable. Note opponent's failure: "have not even attempted to make that showing." | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **"Transitory Product" Doctrine:** Vehicles and tires are "products designed and manufactured for the purpose of travel" - defendants "cannot be reasonably argued" not to expect products to cross state lines. "When the product is transitory, jurisdiction should appropriately follow." | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **George Washington Bridge Absurdity:** "Whether the product failure happens in the westbound lanes or the eastbound lanes of the George Washington Bridge should not be the sole determining factor over jurisdiction." Reduces opponent's position to arbitrary geographic formalism. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **Forum Shopping Reversal:** Flip the forum shopping concern. *Daimler* addressed Argentine plaintiffs in California (true forum shopping). But NY plaintiffs suing in NY "were not engaged in forum shopping. They are both New York State residents." | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **Due Process Balancing Argument:** "Nowhere is there any definitional requirement that personal jurisdiction be so tightly woven into one classification or the another that in protecting the due process rights of one litigant, it crushes the due process rights of the other." | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **"Chilling Effect" on Third-Party Practice:** Strict jurisdiction limits "raise the likelihood of a chilling effect, discouraging third-party actions, except in the most potentially lucrative of cases." Policy argument for maintaining jurisdiction. | Opponent (Plaintiff) | PENDING |
| Respondent's Brief 15 (Gonzales Plaintiffs) | **80-Year Registration Argument:** Defendants "made the affirmative choice over 80 years ago of duly registering with the Department of State to do business in New York and maintaining that registration." Voluntary, sustained forum participation undercuts burden claims. | Opponent (Plaintiff) | PENDING |

---

## INTEGRATED_INSIGHTS

**Note:** All pending insights from Court of Appeals decision, Aybar III decision, and Appellate Briefs were integrated on 2026-01-02.

### Motion Arc
| Date | Source | Insight Summary |
|------|--------|-----------------|
| 2026-01-02 | Aybar COA + AD + Briefs | Three jurisdictional bases (general, specific, consent); CPLR 302 two-prong test; articulable nexus standard; due process five-factor test; preservation requirements; third-party action considerations; counter questions presented format; first prong concession exploitation |

### Case Law Effectiveness
| Date | Source | Case | Finding |
|------|--------|------|---------|
| 2026-01-02 | Aybar COA + AD + Briefs | *Daimler*, *Goodyear*, *Ford v. Montana* | SCOTUS framework for general/specific jurisdiction |
| 2026-01-02 | Aybar COA + AD + Briefs | *Licci*, *Rushaid*, *D&R Global* | "Relatively permissive" articulable nexus standard |
| 2026-01-02 | Aybar COA + AD + Briefs | *Bagdon* | Reinterpreted - service not consent |
| 2026-01-02 | Respondent's Briefs | *Michelin*, *Antonini*, *Hamilton*, *Thomas*, *Bandemer* | Multi-jurisdictional Ford losses, advertising jurisdiction, "tire hit its target" |

### Writing Style
| Date | Source | Target File | Summary |
|------|--------|-------------|---------|
| 2026-01-02 | Respondent's Briefs | opposition/argument_instructions.md | "Slender reed" rhetoric, verb accumulation, bullet point concessions, George Washington Bridge hypothetical, "jurisdictional crapshoots" attack, Ford loss compilation format |

### Strategy
| Date | Source | Insight Summary |
|------|--------|-----------------|
| 2026-01-02 | Aybar COA + AD + Briefs | Preserve all jurisdictional theories; exploit first prong concessions; targeted advertising as jurisdictional hook; used product market strategy; CPLR 302(a)(3) alternative; burden shift exploitation; multi-jurisdictional loss compilation; transitory product doctrine; forum shopping reversal |

---

## PERSONAL JURISDICTION ANALYSIS FRAMEWORK

### Two-Step Analysis (NY Courts)
1. **Statutory Analysis:** Does the long-arm statute (CPLR 301 or 302) authorize jurisdiction?
2. **Constitutional Analysis:** Does exercising jurisdiction comport with due process?

### General Jurisdiction (CPLR 301)
- **Corporate Defendants:** Must be "at home" in NY (principal place of business or state of incorporation)
- **Post-Daimler Standard:** "Doing business" alone insufficient; must be "essentially at home"
- **Exceptional Cases:** Contacts so substantial that defendant is "essentially at home" even if not incorporated/headquartered there

### Specific Jurisdiction (CPLR 302)
- **302(a)(1) - Transaction of Business:**
  - Defendant must transact business in NY
  - Cause of action must arise from that transaction
  - Single act can suffice if purposeful
  - Contract negotiations, communications, performance in NY

- **302(a)(2) - Tortious Act in NY:**
  - Physical presence requirement (act committed in NY)
  - Applied narrowly

- **302(a)(3) - Tortious Act Outside NY:**
  - Requires: (1) tort outside NY, (2) injury in NY, (3) defendant derives substantial revenue from interstate commerce OR expects/should expect act to have consequences in NY and derives substantial revenue from interstate commerce
  - "Situs of injury" analysis (where original event occurred vs. where consequential damages felt)

### Due Process Requirements
- **Minimum Contacts:** Defendant must have sufficient contacts with forum
- **Purposeful Availment:** Defendant purposefully directed activities at forum
- **Relatedness:** Claims must arise out of or relate to contacts
- **Reasonableness:** Exercising jurisdiction must not offend traditional notions of fair play and substantial justice

---

## CONTEXT MANAGEMENT RULES

To prevent context exhaustion:

1. **One motion package at a time** - Complete full package before starting next
2. **Document-by-document** - Don't try to review all documents at once
3. **Extract, don't transcribe** - Capture insights, not full text
4. **Incremental updates** - Small additions to instruction files
5. **Save progress frequently** - Update this file before session ends
6. **Resume, don't restart** - Check this file first each session

---

## END OF PROTOCOL
