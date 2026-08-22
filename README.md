# Anomaly Detection in Cybersecurity

## Overview

This project investigates machine-learning approaches for detecting anomalous and potentially malicious behavior in cybersecurity event logs.

The project uses the **BETH Cybersecurity Dataset**, which contains system-level event information such as process activity and event types.

The main objective is:

> **Learn the normal behavior of a system and identify previously unseen anomalous or malicious activity.**

The project compares three machine-learning approaches:

1. **Isolation Forest**
2. **Local Outlier Factor (LOF)**
3. **Random Forest — Supervised Baseline**

The key finding is that the BETH dataset is designed around a **normal-only training setup**, making unsupervised anomaly-detection algorithms more appropriate than a conventional supervised classifier.

---

# Problem Statement

Cybersecurity systems continuously generate large volumes of system-event data.

Manually inspecting these events is difficult, especially when malicious activity is rare or previously unseen.

The goal of this project is to develop a machine-learning pipeline that can:

- Learn patterns of normal system behavior.
- Identify observations that deviate from normal behavior.
- Detect previously unseen anomalous activity.
- Compare supervised and unsupervised machine-learning approaches.
- Evaluate the models using appropriate cybersecurity metrics.

---

# Dataset

## BETH Cybersecurity Dataset

The project uses the **BETH dataset**, a cybersecurity benchmark designed for anomaly detection.

The dataset is divided into separate training, validation, and testing partitions.

A key characteristic of the dataset is that the **training and validation partitions contain only normal observations**, while the test set contains both normal and anomalous observations.

### Dataset distribution

| Split | Normal | Anomaly |
|---|---:|---:|
| Training | 763,144 | 0 |
| Validation | 188,967 | 0 |
| Testing | 30,535 | 158,432 |

This creates an anomaly-detection scenario:

```text
                BETH Dataset
                     │
          ┌──────────┴──────────┐
          │                     │
       Normal                Anomaly
          │                     │
          ▼                     ▼
    Train + Validation         Test
