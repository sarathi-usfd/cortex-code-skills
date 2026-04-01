# dcm

**Author:** karthick
**Skill Mode:** Live
**Category:** Infrastructure as Code / Database Change Management

---

## Overview

Database Change Management (DCM) — infrastructure as code for Snowflake using `manifest.yml`. Manages Snowflake objects (databases, schemas, tables, views, tasks, dynamic tables) declaratively with version control, dependency tracking, and role-based access control.

---

## When to Use

- Managing Snowflake infrastructure as code with `manifest.yml`
- Creating new databases, schemas, or tables in a repeatable, version-controlled way
- Deploying infrastructure changes across DEV, STAGING, and PROD targets
- Setting up the three-tier role pattern (admin, analyst, consumer)
- Modifying existing DCM projects (add tables, change schemas)
- Tracking and auditing Snowflake object changes over time

---

## How to Use

Invoke for any DCM infrastructure task:

```
/dcm
```

**Or describe your intent:**
> "Create a new DCM project for the analytics database"
> "Add a new table to the existing DCM manifest"
> "Deploy the DCM changes to production"
> "Set up roles for the data warehouse project"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `create-project` | Scaffold a new DCM project with `manifest.yml` |
| `deploy-project` | Deploy infrastructure changes with `snow dcm deploy` |
| `modify-project` | Update an existing manifest (add/change objects) |
| `roles-and-grants` | Set up three-tier role pattern |

### Key References

| File | Content |
|------|---------|
| `reference/syntax_overview.md` | DCM syntax and DEFINE statement patterns |
| `reference/project_structure.md` | Manifest file structure |
| `reference/cli_reference.md` | `snow dcm` CLI commands |
| `reference/primitives/` | Per-object-type syntax (tables, schemas, tasks, etc.) |

---

## Testing

- Deploy to a `DEV` target and validate objects are created correctly
- Run `snow dcm plan` (dry-run) before applying changes to production
- Validate role grants with `SHOW GRANTS TO ROLE <role>` after deployment
- Test multi-target deployments with separate `manifest.yml` target sections

---

## Related Skills

- `dbt-projects-on-snowflake` — Manage dbt projects alongside DCM-managed infrastructure
- `data-governance` — Apply governance policies after DCM deployment
- `dynamic-tables` — Define dynamic tables within DCM projects
- `integrations` — Set up integrations referenced in DCM manifests
