# dynamic-tables

**Author:** karthick
**Skill Mode:** Live
**Category:** Data Engineering / Incremental Processing

---

## Overview

Create and manage Snowflake Dynamic Table pipelines with incremental refresh. Handles creation, monitoring, optimization, troubleshooting, alerting, permissions, and migration from Streams+Tasks.

---

## When to Use

- Building an incrementally refreshed data transformation pipeline
- Replacing a complex Streams+Tasks pipeline with Dynamic Tables
- Debugging a Dynamic Table that stopped refreshing or has stale data
- Optimizing a Dynamic Table for cost or refresh performance
- Setting up refresh lag monitoring and alerts
- Managing access permissions for Dynamic Tables
- Breaking down a large Dynamic Table into smaller dependencies

---

## How to Use

Invoke for any Dynamic Table task:

```
/dynamic-tables
```

**Or describe your intent:**
> "Create a dynamic table that aggregates orders by day with a 1-hour lag"
> "Why is my dynamic table not refreshing?"
> "Migrate our Streams+Tasks pipeline to Dynamic Tables"
> "Set up an alert when the DT refresh lag exceeds 2 hours"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `create` | Create new dynamic tables with SQL |
| `monitor` | Health monitoring, lag tracking, refresh status |
| `optimize` | Performance tuning, cost reduction |
| `troubleshoot` | Debug refresh failures and stale data |
| `permissions` | Role-based access control for DTs |
| `dt-alerting` | Set up lag and failure alerts |
| `task-to-dt` | Migrate Streams+Tasks to Dynamic Tables |

### Key References

| File | Content |
|------|---------|
| `references/sql-syntax.md` | CREATE/ALTER DYNAMIC TABLE syntax |
| `references/monitoring-functions.md` | Monitoring queries and functions |

---

## Testing

- Create Dynamic Tables in a `DEV` schema first with short target lag
- Use `SHOW DYNAMIC TABLES` and `DYNAMIC_TABLE_REFRESH_HISTORY` to verify refreshes
- Test with `ALTER DYNAMIC TABLE ... REFRESH` to force a manual refresh
- Validate output matches expected results vs the source tables

---

## Related Skills

- `dbt-projects-on-snowflake` — Alternative transformation orchestration
- `data-quality` — Monitor Dynamic Table output quality
- `lineage` — Trace Dynamic Table dependencies
- `cost-intelligence` — Monitor Dynamic Table credit costs
