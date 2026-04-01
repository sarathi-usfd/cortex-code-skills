# deploy-to-spcs

**Author:** karthick
**Skill Mode:** Live
**Category:** Infrastructure / Snowpark Container Services

---

## Overview

Deploy containerized applications to Snowpark Container Services (SPCS). Handles Docker image building, image registry setup, compute pool configuration, service creation, and consumer role access management.

---

## When to Use

- Deploying a Docker-based application to Snowflake's managed container infrastructure
- Setting up a REST API or web service inside Snowflake
- Deploying the output of `build-react-app` to SPCS
- Managing SPCS compute pools and image repositories
- Granting consumers access to a deployed SPCS service

---

## How to Use

Invoke when ready to containerize and deploy an application:

```
/deploy-to-spcs
```

**Or describe your intent:**
> "Deploy my Next.js app to SPCS"
> "Set up a compute pool for the analytics service"
> "Grant the analyst role access to the deployed service"

### Deployment Workflow

1. **Validate Docker image** — Build and test the container locally
2. **Set up image repository** — Create or use existing Snowflake image repo
3. **Login to registry** — Authenticate Docker with Snowflake image registry
4. **Push image** — Upload container image to Snowflake registry
5. **Create compute pool** — Configure SPCS compute pool (instance type, size)
6. **Create service** — Deploy the container as an SPCS service
7. **Grant access** — Configure consumer role permissions
8. **Monitor service** — Check service health and logs

---

## Testing

- Test the Docker image locally with `docker run` before pushing
- Use `SHOW SERVICES` to verify the service is running
- Check `SYSTEM$GET_SERVICE_STATUS` for health diagnostics
- Test consumer access with a test role before granting production access
- Validate OAuth token flow for apps using Snowflake authentication

---

## Related Skills

- `build-react-app` — Build the app that this skill deploys
- `machine-learning` — Deploy ML inference endpoints to SPCS
- `integrations` — Set up external access integrations for SPCS services
