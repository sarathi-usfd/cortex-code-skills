# build-react-app

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Claude Code CLI, Codex CLI
**Category:** Application Development

---

## Overview

Build data-intensive Next.js (React) applications connected to Snowflake. Creates dashboards, analytics tools, and data apps with a professional UI using shadcn/ui components.

---

## When to Use

- You need to build a web application that queries Snowflake data
- You want to create an interactive dashboard or data visualization tool
- You need a full-stack app with API routes connected to Snowflake
- You are deploying a containerized app to Snowpark Container Services (SPCS)

---

## How to Use

Invoke this skill when a user asks to build or create a React/Next.js app with Snowflake:

```
/build-react-app
```

**Or describe the intent:**
> "Build a Next.js dashboard that shows revenue trends from Snowflake"

### Workflow Steps

1. **Prerequisites validation** — Checks Node.js v20+ and Docker are installed
2. **Project scaffolding** — Creates Next.js project with shadcn/ui
3. **Snowflake connection** — Sets up connection config (EXTERNALBROWSER for local, OAuth for SPCS)
4. **API routes** — Generates `/api` routes with real Snowflake SQL queries
5. **UI components** — Builds charts, tables, scorecards using shadcn/ui
6. **Local testing** — Validates the dev server and build
7. **Deployment** — Optionally deploys to SPCS via the `deploy-to-spcs` skill

---

## Testing

- Run `npm run dev` to test locally on `localhost:3000`
- Run `npm run build` to validate production build
- Verify Snowflake connectivity with EXTERNALBROWSER authentication locally
- For SPCS deployment, test OAuth token flow before deploying

---

## Related Skills

- `deploy-to-spcs` — Deploy the built app as a containerized service
- `cortex-agent` — Add AI-powered query capabilities to the app
- `dashboard` — Alternative for non-React interactive dashboards
