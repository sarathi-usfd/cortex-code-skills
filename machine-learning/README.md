# machine-learning

**Author:** karthick
**Skill Mode:** Live
**Category:** Machine Learning / Data Science

---

## Overview

End-to-end ML and data science workflows on Snowflake. Covers model training, batch inference, real-time inference via SPCS, experiment tracking, model registry management, model monitoring, and distributed training.

---

## When to Use

- Training ML models using Snowpark ML or scikit-learn on Snowflake compute
- Registering trained models in the Snowflake Model Registry
- Running batch inference jobs on registered models
- Deploying models as real-time REST endpoints via SPCS
- Setting up experiment tracking to compare model versions
- Monitoring deployed model performance (drift, accuracy, latency)
- Running distributed training (PyTorch, XGBoost, LightGBM) on large datasets
- Orchestrating multi-step ML pipelines (DAGs)

---

## How to Use

Invoke for any ML/data science task on Snowflake:

```
/machine-learning
```

**Or describe your intent:**
> "Train a churn prediction model using Snowpark ML"
> "Deploy the fraud detection model as a REST API"
> "Run batch inference on the registered price prediction model"
> "Set up experiment tracking for model comparison"

### Sub-skills

| Sub-skill | Purpose |
|-----------|---------|
| `ml-development` | Model training and feature engineering |
| `batch-inference-jobs` | Run batch scoring on registered models |
| `spcs-inference` | Real-time inference REST endpoints via SPCS |
| `debug-inference` | Troubleshoot inference errors |
| `ml-jobs` | Run custom Python scripts on Snowflake compute |
| `ml-pipeline-orchestration` | Multi-step ML DAG pipelines |
| `distributed-training` | Distributed PyTorch, XGBoost, LightGBM |
| `experiment-tracking` | Log and compare model runs |
| `model-registry` | Register, version, and manage models |
| `model-monitor` | Monitor deployed model performance |
| `inference-logs` | Analyze inference request/response logs |

---

## Testing

- Train and test models in Snowflake Notebooks (Snowsight environment)
- Register model versions with `registry.log_model()` and verify with `SHOW MODELS`
- Test batch inference on a hold-out dataset before production
- Validate REST endpoints with `curl` test calls against SPCS service URL
- Monitor model drift with the `model-monitor` sub-skill after deployment

---

## Related Skills

- `deploy-to-spcs` — Deploy ML inference services to SPCS
- `snowflake-notebooks` — Interactive ML development in notebooks
- `data-quality` — Validate training data quality before model training
- `cost-intelligence` — Track ML compute costs
