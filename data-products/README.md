# data-products

**Author:** karthick
**Skill Mode:** Live
**Compatibility:** Cortex Code CLI, Cortex UI
**Category:** Data Products / Data Sharing

---

## Overview

Build, publish, and govern data products with versioning, access control, and discoverability. Enables teams to package datasets, semantic models, and analytics as reusable, governed products for internal or external consumers.

---

## When to Use

- Packaging a dataset or analytics asset as a shareable data product
- Adding governance (access roles, versioning) to shared data
- Publishing a data product for internal teams or external partners to discover
- Managing the lifecycle of a data product (create, version, deprecate)
- Searching or cataloging available data products in your organization

---

## How to Use

Invoke for any data product creation or management task:

```
/data-products
```

**Or describe your intent:**
> "Create a versioned data product for our revenue metrics"
> "Publish the customer 360 dataset as a data product"
> "Show all available data products in the catalog"

### Workflow

1. Define the data product scope (tables, views, semantic models)
2. Set up access roles and consumer permissions
3. Apply versioning and change management
4. Publish and register in the data catalog
5. Monitor consumption and usage metrics

---

## Testing

- Validate consumer role access grants in a test account
- Verify versioned references resolve correctly after publish
- Test discoverability by searching the catalog as a consumer role
- Check access controls block unauthorized consumers

---

## Related Skills

- `declarative` — Versioned data sharing via application packages
- `data-governance` — Apply governance policies to data products
- `semantic-view` — Include semantic models in data products
- `lineage` — Trace data product dependencies and downstream impact
