# snowpark-connect

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Claude Code CLI, Codex CLI
**Category:** Migration / Spark to Snowpark

---

## Overview

Migrate and validate PySpark code to Snowpark Connect for Spark (SCOS). Converts PySpark import statements, APIs, and patterns to their SCOS equivalents, and validates migrations for correctness and compatibility.

---

## When to Use

- Migrating existing PySpark code to run on Snowflake via Snowpark Connect (SCOS)
- Validating that a migrated PySpark-to-SCOS conversion is complete and correct
- Checking PySpark code for SCOS compatibility before migration
- Converting specific PySpark patterns (import statements, DataFrame APIs) to SCOS

---

## How to Use

Invoke for PySpark-to-SCOS migration tasks:

```
/snowpark-connect
```

**Or describe your intent:**
> "Migrate this PySpark script to Snowpark Connect"
> "Validate my PySpark to SCOS migration is complete"
> "Check if this PySpark code is compatible with SCOS"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `migrate-pyspark-to-snowpark-connect` | Convert PySpark code to SCOS equivalents |
| `validate-pyspark-to-snowpark-connect` | Verify migration completeness and correctness |

### Migration Covers

- Import statement conversion (`pyspark` → SCOS equivalents)
- SparkSession initialization patterns
- DataFrame API compatibility
- PySpark SQL function replacements
- Streaming and structured streaming patterns

---

## Testing

- Run the migrated SCOS code on a small dataset subset first
- Use the `validate` sub-skill to check for unconverted PySpark patterns
- Compare outputs between original PySpark and migrated SCOS on test data
- Run `scripts/` validation tools to generate a compatibility report

---

## Related Skills

- `snowpark` — Native Snowpark Python (non-Spark) alternative
- `machine-learning` — ML workflows after migrating from Spark ML
- `dynamic-tables` — SQL-native alternative for Spark batch transformations
- `dcm` — Manage Snowflake infrastructure for migrated workloads
