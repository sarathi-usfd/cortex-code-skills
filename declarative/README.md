# declarative

**Author:** karthick
**Skill Mode:** Live
**Category:** Data Sharing / Application Packages

---

## Overview

Declarative data sharing with versioning and application roles. Creates versioned application packages for cross-account data sharing — NOT full native Snowflake apps. Supports sharing agents, semantic views, notebooks, and datasets with automatic consumer updates on version changes.

---

## When to Use

- Sharing versioned data assets across Snowflake accounts
- Creating application packages with role-based consumer access
- Publishing datasets, semantic views, or AI agents for external consumers
- Managing data sharing with automatic version rollout
- Setting up app roles to control what consumers can access

---

## How to Use

Invoke for versioned data sharing tasks:

```
/declarative
```

**Or describe your intent:**
> "Create a versioned data sharing package for our revenue models"
> "Share our Cortex Agent with partner accounts"
> "Set up app roles for consumer access to the analytics package"

### Workflow Steps

1. Define the application package scope (objects to share)
2. Set up app roles with appropriate privilege grants
3. Create an initial version with the shared objects
4. Publish the version to make it available to consumers
5. Manage version upgrades with automatic consumer updates

### Supported Shared Assets

- Tables and views
- Semantic views (for Cortex Analyst)
- Cortex Agents
- Notebooks
- Custom datasets

---

## Testing

- Test in a consumer sandbox account before sharing externally
- Validate app role grants let consumers access intended objects only
- Test version upgrade by installing a new version in a test consumer account
- Verify automatic consumer update behavior on version change

---

## Related Skills

- `data-cleanrooms` — Multi-party collaboration without raw data exposure
- `data-products` — Governed internal data product packaging
- `data-governance` — Apply governance before sharing
- `cortex-agent` — Include AI agents in declarative packages
