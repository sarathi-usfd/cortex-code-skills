# workload-performance-analysis

**Author:** karthick
**Skill Mode:** Live
**Category:** Performance / Query Optimization

---

## Overview

Comprehensive SQL query and workload performance analysis for Snowflake. Analyzes spilling, pruning efficiency, caching, clustering, Query Acceleration Service (QAS), and warehouse utilization. Follows a three-phase approach: summary → detection → recommendation.

---

## When to Use

- Investigating slow SQL queries in Snowflake
- Diagnosing warehouse credit consumption and inefficiency
- Analyzing table pruning and partition scan efficiency
- Detecting and fixing disk spilling in queries
- Evaluating cache hit rates for warehouse optimization
- Assessing Query Acceleration Service (QAS) candidates
- Reviewing table clustering effectiveness
- Getting performance improvement recommendations for a workload

---

## How to Use

Invoke for any performance analysis task:

```
/workload-performance-analysis
```

**Or describe your intent:**
> "Why is this query taking so long?"
> "Analyze the performance of our analytics warehouse"
> "How can I reduce the cost of the top 10 most expensive queries?"
> "Why is my table scan reading too many partitions?"

### Analysis Entities

| Entity | Focus |
|--------|-------|
| `query` | Single query performance diagnosis |
| `query-pattern` | Patterns across similar queries |
| `warehouse` | Warehouse-level utilization and efficiency |
| `table` | Table scan performance, clustering |
| `spilling` | Disk and memory spilling diagnosis |
| `pruning` | Partition pruning effectiveness |
| `cache` | Cache hit rate analysis |
| `qas` | Query Acceleration Service candidates |
| `account` | Account-wide workload patterns |

### Three-Phase Analysis

1. **Summary** — High-level metrics and overview
2. **Detection** — Identify specific performance bottlenecks
3. **Recommendation** — Actionable optimization steps

---

## Testing

- Run analysis queries against `SNOWFLAKE.ACCOUNT_USAGE.QUERY_HISTORY` 
- Test recommendations on a copy of the problematic query with `EXPLAIN`
- Validate clustering improvements with `SYSTEM$CLUSTERING_INFORMATION`
- Compare before/after credits using `QUERY_HISTORY.CREDITS_USED_CLOUD_SERVICES`

---

## Related Skills

- `cost-intelligence` — Connect performance improvements to cost savings
- `data-quality` — Check if bad data is causing slow scans
- `lineage` — Understand query data paths for optimization
- `dynamic-tables` — Replace slow queries with incremental DT refreshes
