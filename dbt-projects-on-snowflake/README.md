# dbt-projects-on-snowflake

**Author:** karthick
**Skill Mode:** Live
**Category:** Data Engineering / dbt

---

## Overview

Deploy and run dbt projects as Snowflake-native objects using the `snow dbt` CLI and `EXECUTE DBT PROJECT` SQL command. This is NOT standard dbt CLI — it manages dbt as a first-class Snowflake object with scheduling, monitoring, and documentation generation.

---

## When to Use

- Deploying a dbt project to Snowflake without managing external orchestration
- Running dbt models via SQL (`EXECUTE DBT PROJECT`)
- Scheduling dbt project runs with Snowflake Tasks
- Monitoring dbt run history and model artifacts inside Snowflake
- Migrating an existing local dbt project to Snowflake-native deployment
- Managing multiple deployed dbt projects (list, describe, alter, drop)

> **Note:** Use this skill only for Snowflake-native dbt deployment. For standard local `dbt run` workflows, use the dbt CLI directly.

---

## How to Use

Invoke for Snowflake-native dbt operations:

```
/dbt-projects-on-snowflake
```

**Or describe your intent:**
> "Deploy my dbt project to Snowflake"
> "Schedule the finance dbt project to run daily at 6am"
> "Show the run history for the analytics dbt project"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `deploy` | Deploy a dbt project via `snow dbt deploy` |
| `execute` | Run deployed projects with `EXECUTE DBT PROJECT` |
| `manage` | List, describe, alter, drop deployed projects |
| `schedule` | Schedule runs with `CREATE TASK` |
| `monitoring` | Track execution history and model artifacts |
| `migrate` | Migrate a local dbt project to Snowflake-native |

---

## Testing

- Deploy to a `DEV` target first before promoting to `PROD`
- Run `EXECUTE DBT PROJECT` with `--select` to test individual models
- Use `--full-refresh` for incremental model testing after schema changes
- Check `SHOW DBT PROJECTS` to verify successful deployment

---

## Related Skills

- `dynamic-tables` — Alternative incremental refresh pattern
- `dcm` — Infrastructure-as-code for Snowflake objects
- `data-quality` — Monitor dbt model output quality
- `lineage` — Trace dbt model dependencies
