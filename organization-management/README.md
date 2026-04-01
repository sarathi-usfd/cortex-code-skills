# organization-management

**Author:** karthick
**Skill Mode:** Live
**Category:** Organization / Admin / FinOps

---

## Overview

Org-wide management of Snowflake accounts, users, spending, security posture, and reliability. Provides executive-level insights across all accounts in the organization using org-hub views, ORGANIZATION_USAGE, and global admin capabilities.

---

## When to Use

- Getting an overview of all Snowflake accounts in your organization
- Managing organization-level users and groups (create, import, troubleshoot)
- Analyzing org-wide spending trends across accounts
- Reviewing security posture, MFA readiness, and authentication across accounts
- Understanding reliability patterns, failure rates, and capacity across accounts
- Using Global Org Admin role for cross-account governance actions

---

## How to Use

Invoke for any org-level management task:

```
/organization-management
```

**Or describe your intent:**
> "Show me all Snowflake accounts in our organization"
> "What is our total Snowflake spend this quarter across all accounts?"
> "Create an organization-level user group for analysts"
> "Which accounts have low MFA adoption?"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `accounts` | Account inventory, editions, regions |
| `organization-users/create` | Create org users and groups |
| `organization-users/import` | Import user groups from external sources |
| `organization-users/troubleshoot` | Fix import conflicts |
| `org-hub` | Executive insights (spend, security, auth, reliability) |
| `org-usage-view` | ORGANIZATION_USAGE view mapping and queries |
| `globalorgadmin` | Global org admin role operations |

---

## Testing

- Test org-level queries against `SNOWFLAKE.ORGANIZATION_USAGE` views
- Validate user group creation in a test org before production
- Test global admin operations in a non-production account first
- Verify `SHOW ORGANIZATION ACCOUNTS` returns all expected accounts

---

## Related Skills

- `cost-intelligence` — Deep-dive cost analysis within a single account
- `data-governance` — Governance within individual accounts
- `trust-center` — Security findings across accounts
- `network-security` — Org-wide network policy management
