# cortex-agent

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** AI / Cortex Agents

---

## Overview

Master skill for ALL Cortex Agent operations. Routes to specialized sub-skills for creating, editing, testing, evaluating, optimizing, debugging, and deleting Cortex Agents on Snowflake.

---

## When to Use

- Creating a new Cortex Agent (AI assistant with tools and semantic models)
- Editing or updating an existing agent's configuration
- Testing an agent interactively with ad-hoc questions
- Running formal benchmarks and evaluating agent quality
- Debugging why an agent returned a wrong or unexpected answer
- Optimizing agent performance and accuracy
- Managing the agent lifecycle (list, delete, track)

---

## How to Use

Invoke this skill for any Cortex Agent task:

```
/cortex-agent
```

**Or describe your intent:**
> "Create a new Cortex Agent for our sales data"
> "Why is my agent returning wrong results for revenue questions?"
> "Run an evaluation on the finance agent"

### Sub-skills Available

| Sub-skill | Purpose |
|-----------|---------|
| `create-cortex-agent` | Create a new agent with tools, semantic models, and system prompt |
| `edit-cortex-agent` | Modify an existing agent's config |
| `adhoc-testing-for-cortex-agent` | Ask test questions interactively |
| `evaluate-cortex-agent` | Run formal benchmarks with accuracy metrics |
| `dataset-curation` | Build evaluation datasets from conversation history |
| `debug-single-query-for-cortex-agent` | Debug a specific failing question |
| `investigate-cortex-agent-evals` | Investigate evaluation failures |
| `optimize-cortex-agent` | Improve accuracy and response quality |
| `delete-cortex-agent` | Safely delete an agent with backup |
| `list-cortex-agents` | Discover and list all agents |
| `agent-system-of-record` | Track agent configuration changes |
| `best-practices` | Development guidelines and patterns |

---

## Testing

- Use `adhoc-testing-for-cortex-agent` for interactive question testing
- Use `evaluate-cortex-agent` for batch evaluation with metrics (precision, recall, accuracy)
- Use `debug-single-query-for-cortex-agent` to trace a single query step-by-step
- Evaluation datasets are managed via `dataset-curation`

---

## Related Skills

- `semantic-view` — Build semantic views used as agent tools
- `cost-intelligence` — Monitor agent token usage and costs
- `data-quality` — Validate data quality before exposing via agents
