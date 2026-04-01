# data-quality

**Author:** karthick
**Skill Mode:** Live
**Category:** Data Quality / Observability

---

## Overview

Comprehensive data quality monitoring using Snowflake Data Metric Functions (DMFs). Covers schema health, quality scoring, root cause analysis, SLA alerting, table comparison, regression detection, and pipeline circuit breakers.

---

## When to Use

- Monitoring data quality metrics (nulls, duplicates, freshness, schema drift)
- Investigating why a data quality check failed
- Comparing two tables for migration or transformation validation
- Setting up SLA alerts when quality drops below thresholds
- Detecting quality regressions after pipeline changes
- Analyzing dataset popularity and usage patterns
- Setting up custom Data Metric Functions (DMFs)
- Pausing pipelines automatically on quality failures (circuit breaker)

---

## How to Use

Invoke for any data quality task:

```
/data-quality
```

**Or describe your intent:**
> "Check data quality for the orders table"
> "Why did the null check fail for customer_id?"
> "Compare the old and new version of the products table"
> "Set up a daily freshness alert for the inventory table"

### Workflows

| Workflow | Purpose |
|----------|---------|
| `health-scoring` | Calculate overall quality score |
| `root-cause-analysis` | Investigate a quality failure |
| `regression-detection` | Detect quality changes after updates |
| `trend-analysis` | Quality metrics over time |
| `sla-alerting` | Set up threshold-based alerts |
| `compare-tables` | Diff two tables for migration validation |
| `popularity` | Dataset usage and access analysis |
| `adhoc-assessment` | One-time quality check on any table |
| `monitor-recommendations` | DMF setup wizard for a table |
| `coverage-gaps` | Identify tables without monitoring |
| `dq-incident-investigation` | Multi-dimensional root cause analysis |
| `circuit-breaker` | Pause pipelines on quality failures |
| `custom-dmf-patterns` | Create custom quality metrics |
| `expectations-management` | Tune thresholds and expectations |

---

## Testing

- Deploy DMFs to a test schema before applying to production tables
- Validate health score calculations against known good/bad datasets
- Test circuit breaker logic with simulated failures in a dev pipeline
- Verify SLA alert thresholds fire correctly with synthetic bad data

---

## Related Skills

- `lineage` — Trace upstream causes of data quality failures
- `data-governance` — Govern access to quality metrics and DMF results
- `dynamic-tables` — Monitor quality for incrementally refreshed tables
- `cost-intelligence` — Track DMF execution costs
