# iceberg

**Author:** karthick
**Skill Mode:** Live
**Category:** Data Engineering / Iceberg / Open Table Format

---

## Overview

Manage Apache Iceberg tables on Snowflake. Covers catalog integrations (AWS Glue, Databricks Unity Catalog, OpenCatalog), catalog-linked databases, external volumes, auto-refresh troubleshooting, and Snowflake Intelligence querying of Iceberg data.

---

## When to Use

- Connecting Snowflake to an external Iceberg catalog (AWS Glue, Databricks, Polaris/OpenCatalog)
- Creating a catalog-linked database to auto-discover Iceberg tables
- Setting up external volumes for Iceberg table storage (S3, GCS, Azure)
- Debugging stale or not-refreshing Iceberg data
- Querying Iceberg tables via Snowflake Intelligence (AI-powered)

---

## How to Use

Invoke for any Iceberg table management task:

```
/iceberg
```

**Or describe your intent:**
> "Connect Snowflake to our AWS Glue Iceberg catalog"
> "Create a catalog-linked database for our lakehouse"
> "Why are my Iceberg tables showing stale data?"
> "Set up an external volume for Iceberg on S3"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `catalog-integration` | Connect to external catalogs (Glue, Databricks, OpenCatalog) |
| `catalog-linked-database` | Auto-discover tables from catalog |
| `external-volume` | Configure S3/GCS/Azure storage for Iceberg |
| `auto-refresh` | Troubleshoot stale Iceberg data |
| `cld-snowflake-intelligence` | Query catalog-linked database tables with AI |

---

## Testing

- Test catalog integration with `SHOW CATALOG INTEGRATIONS`
- Verify external volume connectivity with `VALIDATE STORAGE INTEGRATION`
- Test table discovery with `SHOW TABLES IN DATABASE <catalog_linked_db>`
- Validate auto-refresh is working by checking `SHOW ICEBERG TABLES` metadata timestamps
- Query a sample of Iceberg table rows to confirm data freshness

---

## Related Skills

- `integrations` — Set up storage and catalog integrations
- `data-quality` — Monitor Iceberg table data quality
- `lineage` — Trace lineage for Iceberg-backed tables
- `snowflake-postgres` — Use `pg_lake` to export to Iceberg on S3
