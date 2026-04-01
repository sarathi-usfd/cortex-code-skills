# data-governance

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Data Governance / Compliance

---

## Overview

Comprehensive data governance skill covering catalog management, access control, data classification, policy management, and governance maturity assessment. Handles PII detection, role auditing, masking policies, and health scoring.

---

## When to Use

- Auditing who has access to sensitive tables or columns
- Applying data masking or row-level access policies
- Automatically classifying PII and sensitive data
- Reviewing role hierarchies and grant chains
- Assessing your organization's governance maturity
- Tracking data access history and lineage for compliance
- Creating governance maturity or observability health scores

---

## How to Use

Invoke for any governance, access control, or compliance task:

```
/data-governance
```

**Or describe your intent:**
> "Who has access to our customer PII tables?"
> "Apply a masking policy to the email column"
> "Classify sensitive columns automatically"
> "Generate a governance maturity score for our account"

### Workflows

| Workflow | Purpose |
|----------|---------|
| `horizon-catalog` | Catalog browsing, access history, permissions, audit |
| `data-policy` | Masking, row access, and projection policies |
| `sensitive-data-classification` | PII detection and auto-classification |
| `governance-maturity-score` | Overall governance health assessment |
| `observability-maturity-score` | Data observability health score |

---

## Testing

- Run access history queries against `SNOWFLAKE.ACCOUNT_USAGE.ACCESS_HISTORY`
- Validate masking policies on test columns before applying to production
- Test role hierarchies with `SHOW GRANTS TO ROLE` chains
- Verify PII classification results on a sample of known-sensitive columns

---

## Related Skills

- `data-quality` — Ensure data quality as part of governance
- `lineage` — Understand data flow for governance impact analysis
- `trust-center` — Security findings and compliance posture
- `network-security` — Network-level access governance
