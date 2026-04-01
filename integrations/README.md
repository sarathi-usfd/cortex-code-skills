# integrations

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Infrastructure / Integrations

---

## Overview

Create, alter, drop, describe, and show Snowflake integrations of all types. Covers API integrations, catalog integrations, external access integrations, notification integrations, security integrations (SAML2, OAuth, SCIM), and storage integrations (S3, GCS, Azure).

---

## When to Use

- Setting up cloud storage access from Snowflake (S3, GCS, Azure Blob)
- Configuring external API access from UDFs or stored procedures
- Creating notification integrations for email, webhooks, or cloud messaging
- Setting up SAML2 SSO or OAuth authentication
- Configuring catalog integrations for Iceberg (AWS Glue, OpenCatalog)
- Managing SCIM provisioning for user sync
- Any `CREATE/ALTER/DROP INTEGRATION` operation

---

## How to Use

Invoke for any Snowflake integration task:

```
/integrations
```

**Or describe your intent:**
> "Create a storage integration for our S3 bucket"
> "Set up an external access integration for calling an external REST API"
> "Configure SAML2 SSO with Okta"
> "Create an email notification integration"

### Integration Types Covered

| Type | Examples |
|------|---------|
| **API** | REST API calls from UDFs/procedures |
| **Catalog** | AWS Glue, Databricks UC, OpenCatalog (for Iceberg) |
| **External Access** | Outbound network access from Snowpark/UDFs |
| **Notification** | Email, webhooks, SNS/SQS/Pub-Sub |
| **Security** | SAML2 SSO, OAuth (Snowflake/Custom), SCIM |
| **Storage** | S3, GCS, Azure Blob for external stages |

### Operations

- `CREATE` — Create a new integration
- `ALTER` — Modify integration properties
- `DROP` — Remove an integration
- `DESCRIBE` — Show integration details and IAM trust policies
- `SHOW` — List all integrations of a type

---

## Testing

- Use `DESCRIBE INTEGRATION <name>` to get IAM ARNs/trust policies after creation
- Test storage integrations with `LIST @<stage>` after granting S3 permissions
- Validate external access integrations by calling the target API from a test UDF
- Test notification integrations with `SYSTEM$SEND_EMAIL` or a test webhook payload

---

## Related Skills

- `iceberg` — Uses catalog and storage integrations
- `deploy-to-spcs` — Uses external access integrations
- `data-governance` — Uses security integrations for authentication
- `network-security` — Complements integrations with network policies
