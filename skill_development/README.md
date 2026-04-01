# skill_development

**Author:** karthick
**Skill Mode:** Development
**Category:** Meta / Skill Authoring

---

## Overview

Create, document, and audit Cortex Code / Claude Code skills. Provides a workflow for building new skills from scratch, capturing existing workflows as skills, and reviewing/improving existing skills for quality and correctness.

---

## When to Use

- Building a new skill for a Snowflake workflow
- Capturing an existing conversation workflow as a reusable skill
- Auditing an existing skill for quality, completeness, and best practices
- Learning how the skill system works and how to structure SKILL.md files
- Following best practices for skill authoring (frontmatter, stopping points, routing)

---

## How to Use

Invoke for any skill creation or improvement task:

```
/skill_development
```

**Or describe your intent:**
> "Create a new skill for managing Snowflake Tasks"
> "Turn this workflow we just did into a reusable skill"
> "Audit the data-quality skill for completeness"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `create-from-scratch` | Build a new skill with proper structure and frontmatter |
| `summarize-session` | Capture the current session workflow as a skill |
| `audit-skill` | Review an existing skill against best practices |

### Key References

| File | Content |
|------|---------|
| `SKILL_BEST_PRACTICES.md` | Comprehensive skill authoring guidelines (29KB) |
| `SKILL.md` | Routing guide for the sub-skills |

---

## Skill Mode Note

This skill is marked as **Development** because it is a meta-skill used to build other skills. It is not typically invoked for end-user Snowflake operations.

---

## Testing

- After creating a skill, test it by invoking it with representative user prompts
- Run `audit-skill` on newly created skills before publishing
- Validate SKILL.md frontmatter has `name` and `description` fields
- Confirm stopping points (⚠️) are placed before irreversible operations
- Test sub-skill routing by trying different intent phrasings

---

## Related Skills

- `cortex-code-guide` — Understand the skill system before building new skills
- All other skills — Use as examples of well-structured skill implementations
