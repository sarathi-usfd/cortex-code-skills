# data-cleanrooms

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Data Sharing / Collaboration

---

## Overview

Manages Snowflake Data Clean Rooms (DCR) using the Collaboration API. Enables multi-party data collaboration (audience overlap, activation analysis) without exposing raw data between parties.

---

## When to Use

- Setting up a new data clean room collaboration with a partner
- Registering your data as an offering or template for sharing
- Joining an existing collaboration as a data provider
- Running overlap or activation analysis on shared datasets
- Browsing available collaborations, offerings, and templates
- Managing roles across clean room participants (owner, provider, runner)

---

## How to Use

Invoke for any clean room collaboration task:

```
/data-cleanrooms
```

**Or describe your intent:**
> "Create a clean room collaboration with Acme Corp for audience overlap"
> "Register my customer table as a data offering"
> "Run the activation template on the shared collaboration"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `browse` | View available collaborations, offerings, templates |
| `review-join` | Join an existing collaboration |
| `register` | Register data offerings and templates |
| `run` | Execute analysis or activation templates |
| `create` | Create a new collaboration |

---

## Testing

- Test collaboration setup in a sandbox account pair before production
- Validate data offering schemas are accessible to partner accounts
- Run overlap analysis on synthetic datasets before using real PII
- Verify role grants across all participant accounts

---

## Related Skills

- `data-governance` — Govern access to data before sharing in clean rooms
- `declarative` — Alternative for versioned cross-account data sharing
- `integrations` — Configure storage and security integrations needed for collaboration
