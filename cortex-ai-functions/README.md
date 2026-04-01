# cortex-ai-functions

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** AI / Cortex AI Functions

---

## Overview

Snowflake Cortex AI Functions skills bundle for text, image, & document analytics.

## Taxonomy

The `cortex-ai-functions` skills exosystem consists of a main problem-to-solution router for intention detections (either atomic function(s) or custom workflow(s)), elevated high-level refs/ with curated functions docs, and nested purpose-built workflows with their own decomposed refs/ for clarifying nuances.

```
cortex-ai-functions/
├── SKILL.md                          # Main routing skill
├── README.md                         # For humans.. ;)
└── references/                       # AI Functions docs & tips
|   ├── ai-classify.md
|   ├── ai-complete.md
|   ├── ai-extract.md
|   ├── ai-filter.md
|   ├── ai-parse-doc.md
|   └── ai-summ-agg.md
└── document-intelligence/            # "Document intelligence" wofklows -- extraction, parsing, vis-analytics
```

### Functions (atomic)

| Function | Category | Input | Output | Use Case |
|----------|----------|-------|--------|----------|
| **AI_CLASSIFY** | Classification | text/image | label(s) | Categorize, tag, route tickets, sentiment |
| **AI_FILTER** | Filtering | text/image | boolean | Yes/no conditions, semantic joins |
| **AI_EXTRACT** | Extraction | text/file | JSON object | Structured fields from documents |
| **AI_PARSE_DOCUMENT** | Parsing | file | markdown/text | Full document OCR, layout preservation |
| **AI_AGG** | Aggregation | text column | summary | Custom multi-row aggregation |
| **AI_SUMMARIZE_AGG** | Aggregation | text column | summary | General-purpose summarization |
| **AI_COMPLETE** | Generation | prompt/image | text/JSON | Custom LLM tasks, vision analysis |

### Workflows -- nested sub-skills

| Workflow | Description | Route |
|----------|-------------|-------|
| Document Intelligence | End-to-end document processing pipelines | `document-intelligence/SKILL.md` |

---

## When to Use

- Classifying text or images into categories using AI (AI_CLASSIFY)
- Extracting structured fields from documents, invoices, or free-text (AI_EXTRACT)
- Filtering rows with natural language conditions (AI_FILTER)
- Parsing full documents with layout preservation (AI_PARSE_DOCUMENT)
- Summarizing or aggregating multiple text rows (AI_AGG, AI_SUMMARIZE_AGG)
- Running custom LLM completions or vision tasks in SQL (AI_COMPLETE)
- End-to-end document intelligence pipelines (PDFs, images, scanned docs)

---

## How to Use

Invoke this skill for any Cortex AI function task:

```
/cortex-ai-functions
```

**Or describe your intent:**
> "Classify customer feedback into Positive/Negative/Neutral"
> "Extract invoice fields from uploaded PDFs"
> "Filter emails that mention pricing issues"

The skill routes your intent to the appropriate atomic function or the `document-intelligence` workflow sub-skill.

---

## Testing

- Test AI functions in a Snowflake worksheet with a sample `LIMIT 10` query
- Validate AI_EXTRACT schemas match expected output fields
- Check `SHOW CORTEX AI FUNCTIONS` to confirm function availability in your region
- Monitor token consumption in ACCOUNT_USAGE.CORTEX_FUNCTIONS_USAGE_HISTORY

---

## Related Skills

- `cortex-agent` — Build full AI assistants on top of these AI functions
- `cost-intelligence` — Monitor Cortex AI token usage and costs
- `data-quality` — Validate AI function output accuracy
