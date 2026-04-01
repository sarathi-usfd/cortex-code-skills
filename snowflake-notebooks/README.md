# snowflake-notebooks

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Development / Notebooks

---

## Overview

Create and edit Snowflake Workspace notebooks (`.ipynb` format) with SQL and Python cells. Supports Jinja templating, cell referencing, visualization libraries, and upload to Snowflake Workspace with deeplink generation.

---

## When to Use

- Creating a new Snowflake Workspace notebook for data exploration or analysis
- Adding Python or SQL cells to an existing notebook
- Using Jinja templates for parameterized SQL queries in notebooks
- Building visualizations with matplotlib, altair, or plotly in notebooks
- Uploading notebooks to Snowflake Workspace
- Creating notebooks with Snowpark Python data processing

---

## How to Use

Invoke for any Snowflake notebook task:

```
/snowflake-notebooks
```

**Or describe your intent:**
> "Create a notebook that explores the orders table with charts"
> "Add a parameterized SQL cell using Jinja templates"
> "Build a matplotlib visualization cell for revenue trends"

### Notebook Modes

| Mode | Description |
|------|-------------|
| **Workspace (default)** | Notebooks that run entirely in Snowflake — session is automatic |
| **Dual-mode (optional)** | Notebooks that work both locally and in Snowflake |

### Key Features

- SQL cells with `cell_type: sql` and `%%sql` magic
- Python cells with Snowpark session (auto-created in Workspace)
- Cell referencing: reference previous cell results in Python
- Jinja templating: `{{ variable }}` in SQL cells for parameterization
- Visualization: matplotlib, altair, plotly (all supported in Workspace)
- nbformat 4.5+ compliance for compatibility

---

## Testing

- Validate notebook JSON structure with `nbformat.validate()` locally
- Test SQL cells in a Snowflake worksheet before adding to notebook
- Verify Jinja template variables render correctly with test values
- Upload to Snowflake Workspace and run all cells to verify execution

---

## Related Skills

- `machine-learning` — Use notebooks for ML model development
- `developing-with-streamlit` — Convert notebook analyses into interactive Streamlit apps
- `snowpark` — Snowpark Python operations within notebooks
- `data-quality` — Run quality checks inside notebooks
