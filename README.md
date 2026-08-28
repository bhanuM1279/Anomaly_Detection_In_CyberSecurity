# Anomaly Detection in Cybersecurity

## Overview

This project applies machine learning to detect anomalous and potentially malicious behavior in cybersecurity event logs using the **BETH Cybersecurity Dataset**.

The main goal is to learn patterns of normal system behavior and identify previously unseen anomalies.

### Models Used

- **Isolation Forest** — Unsupervised anomaly detection
- **Local Outlier Factor (LOF)** — Unsupervised anomaly detection
- **Random Forest** — Supervised baseline

The BETH dataset uses a **normal-only training setup**, making unsupervised anomaly-detection methods particularly suitable for this task.

---

## Problem Statement

Cybersecurity systems generate a large number of system events, making manual identification of malicious behavior difficult.

This project aims to:

- Learn normal system behavior.
- Detect deviations from normal behavior.
- Identify previously unseen anomalies.
- Compare unsupervised anomaly detection with a supervised baseline.
- Evaluate the models using precision, recall, F1-score, and AUROC.

---

## Workflow

```text
              BETH Dataset
                   │
                   ▼
              Data Loading
                   │
                   ▼
             Data Inspection
                   │
                   ▼
           Data Preprocessing
                   │
                   ▼
          Feature Engineering
                   │
          ┌────────┴────────┐
          ▼                 ▼
   Isolation Forest         LOF
          │                 │
          └────────┬────────┘
                   ▼
             Test Evaluation
                   │
                   ▼
            Model Comparison
                   │
                   ▼
             Random Forest Supervised Baseline
                   │
                   ▼
             Final Analysis
    
  


