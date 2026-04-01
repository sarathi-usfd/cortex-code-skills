# snowconvert-assessment

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Claude Code CLI, Codex CLI
**Category:** Migration / SnowConvert

---

## Overview

Analyze SnowConvert migration assessment reports to plan Snowflake migrations. Covers ETL/SSIS assessment, object exclusion detection, dynamic SQL pattern analysis, and migration wave planning for phased deployment.

---

## When to Use

- Analyzing a SnowConvert assessment report output
- Planning a phased migration from legacy platforms (SQL Server, Teradata, etc.)
- Identifying objects that can be excluded or deprecated before migration
- Analyzing dynamic SQL patterns that need manual conversion
- Generating migration wave plans with dependency ordering
- Assessing SSIS package complexity for ETL migration

---

## How to Use

Invoke for any SnowConvert migration assessment task:

```
/snowconvert-assessment
```

**Or describe your intent:**
> "Analyze the SnowConvert assessment report for our data warehouse migration"
> "Generate migration waves from our assessment results"
> "Which objects can we exclude from the migration?"
> "Analyze dynamic SQL patterns in the assessment"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `etl-assessment` | Analyze SSIS package complexity and migration effort |
| `object_exclusion_detection` | Identify deprecated or excludable objects |
| `analyzing-sql-dynamic-patterns` | Detect and categorize dynamic SQL patterns |
| `waves-generator` | Create phased deployment waves from assessment data |

---

## Testing

- Test with sample SnowConvert assessment report files from a non-production migration
- Validate wave dependencies are correctly ordered before scheduling migration
- Test object exclusion recommendations against actual usage data
- Verify SSIS complexity scores match manual review estimates

---

## Related Skills

- `dcm` — Manage Snowflake infrastructure after migration
- `dbt-projects-on-snowflake` — Replace migrated ETL with dbt-native pipelines
- `data-quality` — Validate migrated data quality post-migration
- `lineage` — Trace migrated object dependencies
