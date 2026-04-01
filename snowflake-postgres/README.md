# snowflake-postgres

**Author:** karthick
**Skill Mode:** Live
**Category:** Database / Snowflake Postgres

---

## Overview

Manage Snowflake Postgres instances and configure `pg_lake` for exporting Postgres data to S3 as Apache Iceberg tables. Covers instance lifecycle management, network connectivity, health diagnostics, and data lake integration.

---

## When to Use

- Creating, suspending, resuming, or resetting a Snowflake Postgres instance
- Configuring network policies for Postgres connectivity
- Diagnosing Postgres performance issues (cache hit, bloat, locks, slow queries)
- Setting up `pg_lake` to export Postgres tables to S3 as Iceberg
- Connecting to a Postgres instance with auto-resume capability
- Troubleshooting Postgres connection or access issues

---

## How to Use

Invoke for any Snowflake Postgres task:

```
/snowflake-postgres
```

**Or describe your intent:**
> "Create a new Snowflake Postgres instance"
> "Why is my Postgres instance running slowly?"
> "Set up pg_lake to export tables to S3 as Iceberg"
> "Configure the network policy for Postgres access"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `manage` | Create, suspend, resume, reset Postgres instances |
| `connect` | Network policy and connection setup |
| `diagnose` | Health checks, cache, bloat, locks, slow queries |
| `pg-lake` | Export Postgres data to S3 as Iceberg tables |

### Key Scripts

| Script | Purpose |
|--------|---------|
| `pg_connect.py` | Connection management with auto-resume |
| `pg_lake_setup.py` | Data lake integration configuration |
| `pg_lake_storage.py` | Storage integration for pg_lake |

---

## Testing

- Test instance creation with `SHOW POSTGRES INSTANCES`
- Run diagnostic queries against `pg_catalog` views after connecting
- Test `pg_lake` export with a small table before bulk export
- Validate Iceberg table availability in Snowflake after pg_lake sync

---

## Related Skills

- `iceberg` — Query pg_lake exported Iceberg tables in Snowflake
- `network-security` — Configure network policies for Postgres access
- `integrations` — Storage integrations needed for pg_lake
