# lineage

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Data Observability / Lineage

---

## Overview

Data lineage analysis for Snowflake — impact analysis, root cause debugging, data discovery, and column-level tracing. Uses Snowflake's built-in lineage functions to map upstream dependencies and downstream consumers of any object.

---

## When to Use

- Assessing the downstream impact before modifying or dropping a table/view
- Tracing the root cause of bad data upstream through a pipeline
- Discovering where a dataset originates (data provenance)
- Tracing column-level lineage to understand transformations
- Verifying data flow for compliance or audit purposes
- Supporting data quality root cause analysis

---

## How to Use

Invoke for any lineage investigation:

```
/lineage
```

**Or describe your intent:**
> "What downstream objects will be affected if I change the orders table?"
> "Trace where the revenue column in the dashboard comes from"
> "Why does the monthly_sales view have incorrect data?"
> "Show me all tables that feed into the customer_360 model"

### Workflows

| Workflow | Purpose |
|----------|---------|
| `impact-analysis` | Discover downstream dependencies before making changes |
| `root-cause-analysis` | Trace upstream path of a data problem |
| `data-discovery` | Verify data provenance and origins |
| `column-lineage` | Column-level transformation tracing |

### Templates

25 SQL templates covering different lineage analysis scenarios including trust scoring and cross-skill integration with data-quality.

---

## Testing

- Run lineage queries against `SNOWFLAKE.ACCOUNT_USAGE.OBJECT_DEPENDENCIES`
- Validate column lineage using `SYSTEM$GET_COLUMN_LINEAGE` function
- Test impact analysis on a known dependency chain before production changes
- Cross-reference lineage results with actual pipeline documentation

---

## Related Skills

- `data-quality` — Use lineage to find root cause of quality failures
- `data-governance` — Combine lineage with access history for compliance
- `dynamic-tables` — Visualize Dynamic Table dependency chains
- `workload-performance-analysis` — Understand query data paths
