# developing-with-streamlit

**Author:** karthick
**Skill Mode:** Live
**Category:** Application Development / Streamlit

---

## Overview

Create, edit, style, optimize, and deploy Streamlit applications on Snowflake. Covers widget creation, theming, custom HTML/JS/CSS components, performance optimization, and deployment to Streamlit in Snowflake (SiS).

---

## When to Use

- Building a Python-based interactive data app with Streamlit
- Creating visualizations, forms, or dashboards using Streamlit widgets
- Styling or theming an existing Streamlit app
- Adding custom HTML, JavaScript, or CSS components to Streamlit
- Optimizing Streamlit app performance (caching, session state)
- Deploying a Streamlit app to Snowflake (Streamlit in Snowflake)

---

## How to Use

Invoke for any Streamlit app development task:

```
/developing-with-streamlit
```

**Or describe your intent:**
> "Create a Streamlit app that shows sales by region with a date filter"
> "Add a custom styled button to my Streamlit app"
> "Optimize the performance of my Streamlit data app"
> "Deploy my Streamlit app to Snowflake"

### Skill Routes To

- **Create** a new Streamlit app from scratch
- **Edit** an existing app (add widgets, fix bugs, change layout)
- **Style** the app with themes, CSS, and branding
- **Optimize** for performance (caching, lazy loading, session state)
- **Deploy** to Streamlit in Snowflake (SiS)

### Reference Coverage (24 topics)

Includes references for: charts, data tables, forms, authentication, session state, caching, theming, custom components, file uploads, multi-page apps, Snowflake connectivity, and more.

---

## Testing

- Test locally with `streamlit run app.py` before deploying to Snowflake
- Use `st.cache_data` and `st.cache_resource` to validate caching behavior
- Test Snowflake connectivity with `snowflake.connector` or `snowpark` session
- After SiS deployment, verify app loads correctly in Snowsight

---

## Related Skills

- `build-react-app` — For complex apps needing Next.js/TypeScript
- `dashboard` — For simpler chart/table dashboards without custom Python
- `deploy-to-spcs` — Deploy as a containerized app (alternative to SiS)
- `snowpark` — Snowpark Python for data transformation inside Streamlit
