# trust-center

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Security / Trust Center

---

## Overview

Analyze and remediate security findings from the Snowflake Trust Center. Covers severity distribution analysis, scanner inventory, scanner management (enable/disable), finding remediation guidance, and CIS Benchmarks tracking.

---

## When to Use

- Reviewing security findings from the Snowflake Trust Center dashboard
- Getting remediation guidance for specific security issues
- Analyzing finding severity trends over time
- Managing security scanners (enable/disable specific checks)
- Tracking CIS Benchmark compliance status
- Prioritizing security fixes by risk severity

---

## How to Use

Invoke for any Trust Center security task:

```
/trust-center
```

**Or describe your intent:**
> "Show me the critical Trust Center findings I need to fix"
> "How do I remediate the MFA not enforced finding?"
> "What scanners are enabled in Trust Center?"
> "Track our progress on CIS Benchmarks compliance"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `findings-analysis` | Severity distribution, trends, priority ranking |
| `scanner-analysis` | Scanner inventory and coverage gaps |
| `api-management` | Enable or disable specific scanners via API |
| `finding-remediation` | Step-by-step fixes for specific findings |

---

## Testing

- Query Trust Center findings via SQL: `SELECT * FROM SNOWFLAKE.TRUST_CENTER_SCHEMA.FINDINGS`
- Test scanner enable/disable operations in a non-production account first
- Validate remediation steps by re-running scanners after applying fixes
- Compare finding counts before/after remediation to measure progress

---

## Related Skills

- `data-governance` — Governance policies that address access-related findings
- `network-security` — Network policies for network access findings
- `organization-management` — Org-wide security posture via org-hub
