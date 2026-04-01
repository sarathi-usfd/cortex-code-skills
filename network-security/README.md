# network-security

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Security / Network Policies

---

## Overview

Manage Snowflake network policies and rules to control which IP addresses and networks can access your Snowflake account or specific users. Includes policy advisor for recommendations, IP allowlist configuration, SaaS coverage analysis, and hybrid policy setup.

---

## When to Use

- Restricting Snowflake access to specific IP ranges or VPCs
- Creating or modifying network policies for user-level or account-level access control
- Getting recommendations for network policy settings (policy advisor)
- Checking which SaaS integrations are covered by existing policies
- Setting up hybrid (allow + block) network policies

---

## How to Use

Invoke for any network security task:

```
/network-security
```

**Or describe your intent:**
> "Create a network policy that only allows our office IP ranges"
> "What network policy settings would you recommend for our account?"
> "Block all access except from our VPC CIDR range"
> "Check if our Tableau SaaS IPs are covered in the current policy"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `network-policy-advisor` | Get intelligent policy recommendations |

### Operations Covered

- `CREATE NETWORK POLICY` — New policies with IP allowlists/blocklists
- `ALTER NETWORK POLICY` — Modify existing policies
- `SHOW NETWORK POLICIES` — List all policies
- `DESCRIBE NETWORK POLICY` — View policy details
- Assigning policies to users and account-wide

---

## Testing

- Test network policies in a dev account before applying account-wide
- Use a separate session to verify the policy allows/blocks as expected
- Test from both allowed and blocked IP addresses to confirm behavior
- Use `SHOW PARAMETERS LIKE 'NETWORK_POLICY' IN ACCOUNT` to verify assignment

---

## Related Skills

- `data-governance` — Combine network policies with user access governance
- `trust-center` — Check security posture including network access findings
- `integrations` — External access integrations that may need network policy exceptions
