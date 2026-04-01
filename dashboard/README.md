# dashboard

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Visualization / BI

---

## Overview

Creates interactive dashboards using the DashboardSpec JSON format. Supports charts (Vega-Lite), tables, scorecards, markdown widgets, interactive variables and filters, all arranged in a 12-column grid layout.

---

## When to Use

- Building a Snowflake dashboard with charts, tables, and KPI scorecards
- Adding interactive filters or dropdown variables to a dashboard
- Creating a visualization without writing a full React/Next.js app
- Sharing a data view with stakeholders inside Snowflake

---

## How to Use

Invoke for dashboard creation tasks:

```
/dashboard
```

**Or describe your intent:**
> "Build a dashboard showing daily active users and revenue by region"
> "Create a scorecard for key business metrics"
> "Add a date filter to the sales dashboard"

### Widget Types

| Widget | Purpose |
|--------|---------|
| `markdown` | Text, headers, descriptions |
| `chart` | Vega-Lite charts (bar, line, pie, scatter) |
| `table` | Tabular SQL results |
| `scorecard` | Single KPI metric with trend indicator |

### Key References

- `references/variables-and-filters.md` — Interactive filtering and dropdown variables
- `references/complete-example.md` — Full DashboardSpec JSON example

---

## Testing

- Validate DashboardSpec JSON against the schema before deployment
- Test SQL data sources independently in a Snowflake worksheet
- Preview chart Vega-Lite specs at `vega.github.io/editor`
- Verify interactive variables render correctly with test filter values

---

## Related Skills

- `build-react-app` — For more complex web apps needing custom logic
- `developing-with-streamlit` — Python-based interactive apps
- `semantic-view` — Power dashboards with semantic model data sources
