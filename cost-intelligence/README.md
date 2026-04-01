# cost-intelligence

**Author:** karthick
**Skill Mode:** Live
**Category:** Cost & Billing / FinOps

---

## Overview

Handles ALL Snowflake cost and billing questions. Provides SQL-driven analysis of spend by user, warehouse, service, and time period. Supports anomaly detection, budget creation, trend analysis, and serverless cost breakdowns.

---

## When to Use

- Investigating unexpected Snowflake credit consumption
- Identifying top spenders (users, warehouses, queries)
- Analyzing week-over-week or month-over-month cost trends
- Setting up Snowflake budgets and alerts
- Breaking down costs by service (warehouse, Cortex AI, SPCS, Snowpipe, storage)
- Detecting cost anomalies or spikes

---

## How to Use

Invoke for any Snowflake cost question:

```
/cost-intelligence
```

**Or ask directly:**
> "Who is spending the most credits this month?"
> "Show me cost trends for the last 30 days"
> "Create a budget alert for our analytics warehouse"
> "Why did our Snowflake bill spike last Tuesday?"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `anomaly-insights` | Detect and explain spending anomalies |
| `budget` | Create and manage Snowflake budgets |

### Reference Query Categories

| Category | What It Answers |
|----------|----------------|
| `users-queries` | Top spenders, most expensive queries |
| `overview` | Cost breakdown by service type |
| `warehouse` | Per-warehouse credit usage |
| `trends` | Week/month-over-month analysis |
| `serverless` | Tasks, Snowpipe, search optimization costs |
| `storage` | Database and stage storage sizes |
| `cortex-ai` | AI function and agent token costs |
| `containers` | SPCS compute pool costs |
| `budgets` | Budget utilization and status |

---

## Testing

- Run reference queries against `SNOWFLAKE.ACCOUNT_USAGE` views
- Use `SHOW BUDGETS` to verify budget creation
- Test anomaly detection against historical billing data in a dev account
- Validate trends queries with known billing periods

---

## Related Skills

- `workload-performance-analysis` — Optimize expensive queries to reduce costs
- `organization-management` — Org-wide cost visibility across accounts
- `cortex-agent` — Monitor agent token usage costs
