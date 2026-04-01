# snowpark

**Author:** karthick
**Skill Mode:** Live
**Category:** Data Engineering / Snowpark Python

---

## Overview

Snowpark Python reference and workflow skill. Covers Snowpark Session setup, DataFrame operations, data ingestion, and transformation — enabling Python-based data processing that runs natively inside Snowflake.

---

## When to Use

- Writing Python code that runs directly on Snowflake compute using Snowpark
- Setting up a Snowpark Session for local or Snowflake-native execution
- Building DataFrame pipelines for data transformation in Python
- Ingesting data into Snowflake tables using Snowpark DataFrames
- Learning Snowpark Python API patterns and best practices

---

## How to Use

Invoke for any Snowpark Python task:

```
/snowpark
```

**Or describe your intent:**
> "Set up a Snowpark session to connect to Snowflake"
> "Write a Snowpark DataFrame transformation to aggregate sales by region"
> "Ingest a CSV file into a Snowflake table using Snowpark"

### Core Topics

| Topic | Description |
|-------|-------------|
| Session setup | `Session.builder.configs().create()` |
| DataFrame creation | From tables, SQL, or in-memory data |
| Transformations | `filter()`, `select()`, `groupBy()`, `join()` |
| Data ingestion | `write.mode().saveAsTable()` |
| UDFs | Python functions pushed to Snowflake compute |
| Stored procedures | Python procedures with `@sproc` decorator |

---

## Testing

- Test Snowpark sessions locally with `snowflake-snowpark-python` package
- Validate DataFrame transformations with `.show()` before writing to tables
- Compare output with direct SQL queries to verify correctness
- Run Snowpark code in Snowflake Notebooks for integrated testing

---

## Related Skills

- `snowflake-notebooks` — Run Snowpark in interactive notebooks
- `machine-learning` — Snowpark ML for model training
- `developing-with-streamlit` — Use Snowpark inside Streamlit apps
- `dynamic-tables` — SQL-based alternative for incremental transformations
