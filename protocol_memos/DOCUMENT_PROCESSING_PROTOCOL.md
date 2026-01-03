# LCP v2.0 DOCUMENT PROCESSING PROTOCOL

**Version:** 1.2
**Date:** December 5, 2025
**Purpose:** Establish uniform procedures for manual document processing sessions
**Last Verified:** December 5, 2025

---

## OVERVIEW

This protocol governs the manual processing of documents through the LCP v2.0 pipeline when working interactively with Claude Code. It ensures consistent handling, quality verification, and proper template/extractor validation before each document is processed.

---

## CORE PRINCIPLES

### 1. User-Directed Processing
- **Only process documents explicitly provided by the user**
- Do not automatically select or batch-process documents from directories
- Wait for explicit file path or document reference before proceeding

### 2. One Document at a Time
- Process each document individually through the complete pipeline
- Confirm successful completion before accepting the next document
- This approach enables:
  - Immediate identification of failures
  - Quality verification at each step
  - Troubleshooting without affecting other documents

### 3. Template/Extractor Verification First
- Before processing any document, verify required resources exist
- Check for missing standardization templates or extractors
- Create any missing resources before attempting to process

---

## PROCESSING WORKFLOW

This workflow combines the interactive steps with the 8-phase LCP pipeline. Steps 1-4 are preparation, Steps 5-12 execute the 8-phase pipeline, and Steps 13-14 complete the interaction.

### Step 1: Receive Document
- User provides document path
- Read and examine the document content

### Step 2: Initial Classification
- Determine document type from the **118 supported categories** (as of December 2025)
- Note confidence level of classification
- Reference: `document_processing/document_types.py` (812 lines, v2.2.1)

### Step 3: Verify Resources
Check for existence of required files:

**Standardization Template:**
```
Y:\LCP_v2.0\program_files\instructions\standardization_templates\{type}_standardization_template.md
```

**Extractor (if applicable for structured extraction):**
```
Y:\LCP_v2.0\program_files\document_processing\{type}_extractor.py
```

**Extraction Instructions (if applicable):**
```
Y:\LCP_v2.0\program_files\instructions\extraction\{type}_extraction_instructions.md
```

### Step 4: Create Missing Resources
If any required template or extractor is missing:
1. Notify user of the gap
2. Create the missing resource following LCP v2.0 patterns
3. Confirm creation before proceeding

### Step 5: Phase 1 - Document Intake
- Validate file exists and is accessible
- Verify file type is supported (PDF, DOCX, DOC, TXT, RTF, images)
- Check file size within limits
- Module: `services/document_intake_service.py` (546 lines)

### Step 6: Phase 2 - Text Extraction
- Extract text using pdfplumber (primary)
- Apply fallbacks if needed (PyPDF2 → Docling → OCR)
- Assess extraction quality (0.0-1.0 score)
- Flag if quality below threshold
- Module: `document_processing/text_extractor.py` (599 lines)

### Step 7: Phase 3 - Classification
- Confirm document type via AI classification
- Verify confidence meets threshold (≥0.70)
- Apply pattern matching fallback if needed
- Request user confirmation if confidence low
- Module: `document_processing/document_classifier.py` (476 lines)

### Step 8: Phase 4 - Metadata Extraction
Extract 6-component schema:
- **DATE** - Filing/document date (YYYY-MM-DD)
- **CLASSIFICATION** - Document type from Phase 3
- **PARTY_ROLE** - Filing party (plaintiff, defendant, etc.)
- **TITLE** - Descriptive document name
- **MOTION_SEQUENCE** - Motion sequence number (seq_no_X or NA)
- **DOC_NUMBER** - Court filing number (NYSCEF-XXX, ECF-XXX, or NA)

Module: `document_processing/metadata_extractor.py` (422 lines)

### Step 9: Phase 5 - Document Standardization
- Load appropriate standardization template (105 templates available)
- Send document text + template to Claude API
- Generate structured markdown output
- Handle large documents via chunked processing
- Module: `document_processing/document_standardizer.py` (2,132 lines)

### Step 10: Phase 6 - Structured Extraction
Apply document-type-specific extractors (if applicable):

| Extractor | Lines | Purpose |
|-----------|-------|---------|
| `causes_of_action_extractor.py` | 408 | Complaint claims |
| `jurisdiction_venue_extractor.py` | 392 | Complaint jurisdiction |
| `contract_extractor.py` | 520 | Contract provisions (18 types) |
| `lp_agreement_extractor.py` | 1,777 | LP agreement terms |
| `llc_operating_agreement_extractor.py` | 1,323 | LLC operating agreement |
| `summary_judgment_memo_extractor.py` | 586 | SJ memo arguments/citations |

Store structured data for downstream analysis.

### Step 11: Phase 7 - Storage and Organization
- Generate standardized 6-component filename
- Route to appropriate folder structure
- Save processed files to output directory:
  - Standardized markdown to `{output_dir}/standardized/`
  - Extraction JSON to `{output_dir}/extractions/`
- **Store to database** using `LCPDatabase`:
  - Document record with 6-component metadata
  - Case and party records (if new)
  - Structured extraction data (claims, provisions, etc.)
  - Processing log entry

### Step 12: Phase 8 - Post-Processing
- Log extraction details to CSV via `utils/extraction_csv_logger.py`
- **Generate vector embeddings** using `legal_research/document_embedder.py`:
  - Chunk document text (configurable size/overlap)
  - Generate embeddings via sentence-transformers (all-MiniLM-L6-v2)
  - Store in Pinecone index (case-specific namespace for confidentiality)
- Trigger litigation analysis (if applicable):
  - Phase 2: Factual allegations extraction
  - Phase 4: Comparative analysis
  - Phase 5: Examination builder

### Step 13: Confirm Success
Report to user:
- Classification result and confidence
- Metadata extracted (all 6 components)
- Output file location(s)
- Database record IDs created
- Pinecone embedding status (chunks stored)
- Any warnings or issues encountered

### Step 14: Await Next Document
- Do not proceed until user provides next document
- Do not assume additional documents should be processed

---

## OUTPUT SPECIFICATIONS

### Default Output Location
Unless otherwise specified by user, outputs go to the case folder structure:
```
Y:\LCP Casework\{case_name}\
├── Processed Documents\
│   ├── Pleadings\
│   ├── Motions\
│   ├── Discovery\
│   └── ...
├── Standardized\
└── Extractions\
```

### Output Files Generated

**1. Standardized Document (Markdown)**
```
{case_folder}/Standardized/{standardized_filename}.md
```

**2. Extraction Data (JSON)**
```
{case_folder}/Extractions/{document_id}_extraction.json
```

**3. Processing Log Entry**
```
{case_folder}/extraction_log.csv
```

### Standardized Filename Format
```
DATE_TYPE_ROLE_TITLE_MOTION-SEQ_DOCNUM.ext

Example: 2024-03-15_COMPLAINT_PL_Verified Complaint_NA_NYSCEF-001.pdf
```

---

## DATABASE CONFIGURATION

### Database Location
LCP v2.0 uses a dual-database architecture:

**Main Database (case and document data):**
```
Y:\LCP_v2.0\data\databases\lcp_data.db
```

**Legal Research Database:**
```
Y:\LCP_v2.0\data\databases\legal_research.db
```

### Database Access Module
```
Y:\LCP_v2.0\program_files\core\lcp_database.py (1,309 lines)
```

This module provides the central interface, composing 10 specialized operation classes:

| Operation Class | Purpose |
|----------------|---------|
| `lcp_database_case.py` | Case CRUD, party queries |
| `lcp_database_document.py` | Document CRUD, type validation |
| `lcp_database_factual_allegations.py` | Phase 2 allegation storage |
| `lcp_database_comparative_analysis.py` | Phase 4 analysis chains |
| `lcp_database_examination.py` | Phase 5 examination outlines |
| `lcp_database_causes_of_action.py` | Complaint claim tracking |
| `lcp_database_contract_provisions.py` | Contract provision storage |
| `lcp_database_jurisdiction_venue.py` | Jurisdiction/venue data |
| `lcp_database_summary_judgment.py` | SJ memo analysis |
| `legal_authorities_database.py` | Legal research storage |

### Key Database Tables

**Case Management:**
- `cases` - Case/matter information
- `entities` - People and organizations
- `case_parties` - Entity-case relationships
- `documents` - Processed documents with 6-component metadata

**Litigation Analysis:**
- `factual_allegations` - Individual allegations (Phase 2)
- `allegation_relationships` - Cross-document relationships
- `analysis_chains` - Comparative analysis chains (Phase 4)
- `analysis_layers` - Layer-by-layer analysis
- `inconsistencies` - Detected inconsistencies
- `examination_outlines` - Trial examination outlines (Phase 5)
- `examination_sections` - Outline sections
- `examination_questions` - Individual questions

**Structured Extraction:**
- `complaint_causes_of_action` - Legal claims
- `complaint_jurisdiction_venue` - Jurisdiction data
- `contract_metadata` - Contract information
- `contract_provisions` - Contract provisions (18 types)
- `summary_judgment_memos` - SJ memo data
- `sj_arguments` - SJ arguments
- `sj_citations` - Legal citations
- `sj_undisputed_facts` - Undisputed facts

### Storing Processed Documents

```python
from core.lcp_database import LCPDatabase

db = LCPDatabase()

# Store document with metadata
doc_id = db.insert_document(
    case_id='case_001',
    filepath='/path/to/document.pdf',
    document_type='COMPLAINT',
    title='Verified Complaint',
    party_role='plaintiff',
    doc_date='2024-03-15',
    motion_seq='NA',
    filing_number='NYSCEF-001'
)

# Store structured extraction data
db.insert_causes_of_action(doc_id, causes_data)
db.insert_contract_provisions(doc_id, provisions_data)
```

---

## PINECONE VECTOR DATABASE CONFIGURATION

### Data Isolation Policy
**Each case uses a dedicated namespace within the Pinecone index for confidentiality.**

This ensures:
- Complete data isolation between cases
- No accidental cross-case search results
- Clean deletion when case closes

### Index Configuration
```
Index Name: lcp-documents (default, configurable via PINECONE_INDEX_NAME)
Namespace: {case_id} (one namespace per case)
```

### Environment Configuration
API keys are stored in environment variables (NEVER in code or chat):

```
Y:\LCP_v2.0\.env
```

Required variables:
- `PINECONE_API_KEY` - Your Pinecone API key
- `PINECONE_INDEX_NAME` - Index name (optional, defaults to "lcp-documents")
- `ANTHROPIC_API_KEY` - Claude API key

### Embedding Documents
```python
from legal_research.document_embedder import DocumentEmbedder

embedder = DocumentEmbedder()

# Embed single document
embedder.embed_document(doc_id, case_id)

# Search within case
results = embedder.search(
    query="general partner equity interests",
    case_id="case_001",
    top_k=5
)
```

---

## DOCUMENT GENERATION (Optional Post-Processing)

After processing, documents can be used to generate reports:

### Case Reports
```python
from document_generators.case_report_generator import ClaudeReportGenerator

generator = ClaudeReportGenerator(case_id="case_001")
report_path = generator.generate_report(output_dir="/path/to/output")
```

### Legal Analysis Reports (Summary Judgment Stage)
```python
from document_generators.legal_analysis_generator import generate_legal_analysis_report

output_files = generate_legal_analysis_report(
    case_id="case_001",
    output_dir="/path/to/output",
    output_formats=['markdown', 'word']
)
```

This generates a comprehensive 9-section analysis including:
- Executive Summary
- Procedural History
- Statement of Facts (undisputed/disputed)
- Legal Issues
- Applicable Law
- Analysis
- Outcome Prediction
- Responsive Brief Recommendations
- Appendices

---

## RESOURCE CREATION GUIDELINES

### When Creating Standardization Templates

1. Follow existing template patterns in `instructions/standardization_templates/`
2. Include all relevant sections for the document type
3. Use consistent markdown structure
4. Reference the `TEMPLATE_CREATION_GUIDE.md` for formatting standards
5. Name file: `{document_type_lowercase}_standardization_template.md`

### When Creating Extractors

1. Follow existing extractor patterns in `document_processing/`
2. Implement tiered extraction if appropriate (Tier 1/2/3 priority)
3. Include confidence scoring
4. Integrate with appropriate database tables in `core/lcp_database_*.py`
5. Name file: `{document_type_lowercase}_extractor.py`

### When Creating Extraction Instructions

1. Follow existing instruction patterns in `instructions/extraction/`
2. Provide clear field definitions
3. Include examples where helpful
4. Name file: `{document_type_lowercase}_extraction_instructions.md`

---

## ERROR HANDLING

### If Text Extraction Fails
- Report failure to user
- Suggest alternatives (OCR, manual text input, Vision API for handwriting)
- Do not proceed without user direction

### If Classification Confidence is Low (<0.70)
- Report classification with confidence score
- Ask user to confirm or override classification
- Do not proceed without confirmation

### If Standardization Fails
- Save extraction data regardless
- Report the failure with error details
- Ask user whether to retry or proceed to next document

### If API Connection Fails
- Report the connection issue
- Wait for user direction (retry, skip phase, abort)
- Do not automatically retry indefinitely

### If Database Insert Fails
- Save files to filesystem regardless
- Report the database error
- Provide SQL or manual insert instructions if needed

---

## SESSION DOCUMENTATION

### At Session Start
- Confirm output directory
- Verify API connectivity (Claude API)
- **Verify database connectivity** (check `lcp_data.db` exists and is accessible)
- Note any standing instructions from user

### During Session
- Track documents processed
- Note any issues encountered
- Record any new templates/extractors created

### At Session End
- Summarize documents processed
- List any failures or pending items
- Note any resources created
- Create handoff memo if session is incomplete

---

## CHECKLIST FOR EACH DOCUMENT

```
PREPARATION (Steps 1-4)
[ ] Step 1:  Document path received from user
[ ] Step 2:  Document read and initial classification determined
[ ] Step 3:  Required resources verified (templates, extractors)
[ ] Step 4:  Missing resources created (if needed)

8-PHASE PIPELINE (Steps 5-12)
[ ] Step 5:  Phase 1 - Document intake validated
[ ] Step 6:  Phase 2 - Text extraction successful (quality score acceptable)
[ ] Step 7:  Phase 3 - Classification confirmed (≥0.70 confidence or user-confirmed)
[ ] Step 8:  Phase 4 - Metadata extraction complete (all 6 components)
[ ] Step 9:  Phase 5 - Standardization to markdown complete
[ ] Step 10: Phase 6 - Structured extraction complete (if applicable)
[ ] Step 11: Phase 7 - Files saved AND database records created
[ ] Step 12: Phase 8 - Post-processing complete (CSV logging, Pinecone embeddings)

COMPLETION (Steps 13-14)
[ ] Step 13: Success confirmed with user
[ ] Step 14: Awaiting next document (user-initiated)
```

---

## QUICK REFERENCE: KEY FILES

| Purpose | File Location | Lines |
|---------|---------------|-------|
| Document Types (118) | `document_processing/document_types.py` | 812 |
| Classification | `document_processing/document_classifier.py` | 476 |
| Standardization | `document_processing/document_standardizer.py` | 2,132 |
| Metadata Extraction | `document_processing/metadata_extractor.py` | 422 |
| Text Extraction | `document_processing/text_extractor.py` | 599 |
| Database Interface | `core/lcp_database.py` | 1,309 |
| Vector Embeddings | `legal_research/document_embedder.py` | 435 |
| Case Reports | `document_generators/case_report_generator.py` | 737 |
| Legal Analysis | `document_generators/legal_analysis_generator.py` | 1,135 |
| Prompt Loading | `utils/prompt_loader.py` | 348 |

---

**END OF PROTOCOL**

*Prepared by: Claude Code*
*Version: 1.2*
*Date: December 5, 2025*
*Verified against LCP v2.0 codebase: December 5, 2025*
