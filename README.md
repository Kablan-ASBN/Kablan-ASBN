# Kablan Assebian
*(Legal name: Gomis Kablan Assebian)*

**Analytics Engineer · Technical Data Analyst**
`SQL` `Python` `dbt` `ETL` `Data Quality` `KPI Modeling`

MSc Data Science — Distinction · University of Greenwich (BCS-Accredited) · U.S. Citizen

🌐 English & French (native/bilingual) &nbsp;|&nbsp; 📍 Atlanta, GA &nbsp;|&nbsp; [![LinkedIn](https://img.shields.io/badge/LinkedIn-gomis--kablan-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/gomis-kablan/) [![Email](https://img.shields.io/badge/Email-gomis.k.assebian@gmail.com-EA4335?style=flat&logo=gmail)](mailto:gomis.k.assebian@gmail.com)

---

I build analytics systems where the numbers are consistent, explainable, and audit-ready.

My focus is the layer between raw data and business decisions: transformation logic, metric definitions, validation pipelines, and documentation that makes outputs trustworthy and reproducible. Currently open to Analytics Engineer, Technical Data Analyst, and related roles.

Before analytics engineering, I spent six years co-founding and scaling a nonprofit across four regions of Côte d'Ivoire. I built the team from the ground up, managed cross-regional operations, and coordinated stakeholders with competing priorities on a limited budget. That experience showed me what happens when data systems are absent or unreliable. It shapes how I work today: data quality is a prerequisite for organizational trust, not just a technical checkbox. It also means I bring project leadership, stakeholder communication, and the ability to move initiatives from ambiguity to execution.

---

## What I Work On

**Analytics Engineering**
Modular SQL transformations, staging and mart layers, dbt-style modeling, metric grain standardization, and validation logic that catches reporting discrepancies before they reach stakeholders.

**Data Quality & Reconciliation**
End-to-end reconciliation workflows, root-cause investigation of KPI mismatches (join errors, grain issues, definition drift), completeness and consistency checks, and audit-ready outputs.

**ETL & Python Pipelines**
Reproducible Python workflows for data ingestion, cleaning, transformation, and automated validation. Built to be readable, testable, and maintainable.

---

## Projects

### [Revenue & KPI Reconciliation: Commerce Analytics Case Study](https://github.com/Kablan-ASBN/revenue-kpi-reconciliation)
**The problem:** Finance, Operations, and Marketing report different revenue numbers from the same source data. This project investigates why — and builds the reconciliation logic to resolve it.

Built on the Olist Brazilian E-Commerce dataset. Aggregates item-, freight-, and payment-level data to a consistent order-level grain. Defines and compares four revenue metrics (gross items-only, gross with freight, paid, net non-canceled proxy). Identifies root causes of mismatches including canceled orders with captured payments and multi-item joins at the wrong grain. Produces operational validation checks designed for production monitoring.

`Python` `Pandas` `SQL-style aggregation` `Metric documentation` `Data validation`

---

### [Bank Loan Risk Analysis](https://github.com/Kablan-ASBN/bank-loan-risk-analysis)
**The problem:** Default risk models trained on imbalanced data produce misleadingly high accuracy while failing to identify the cases that matter most.

Analyzed 1.2M+ Lending Club loan records. Built an end-to-end pipeline covering ingestion, cleaning, validation, and feature engineering. Improved default recall from 5.4% to 67.1% through class imbalance handling and downsampling. Emphasis on business trade-offs and decision-relevant reporting — ROC-AUC, precision-recall curves, and confusion matrices framed around lending risk decisions, not raw model accuracy.

`Python` `Pandas` `scikit-learn` `ROC-AUC` `Precision-Recall` `Class imbalance`

---

### [Fraud Detection System: Real-Time ML Pipeline](https://github.com/Kablan-ASBN/fraud-detection-system)
**The problem:** Credit card fraud detection requires handling extreme class imbalance (577:1) while maintaining low false negatives and real-time throughput.

Built a production-oriented ML pipeline using Dask-based ETL that scales with transaction volume. Trained a LightGBM classifier achieving 0.905 ROC-AUC and 87% fraud recall. Deployed via FastAPI as a REST endpoint for real-time inference. Applied threshold tuning and scale_pos_weight adjustment to minimize false negatives. Modularized codebase with separate training, evaluation, and deployment modules.

`Python` `LightGBM` `Dask` `FastAPI` `ETL pipeline` `Class imbalance` `Model deployment`

---

### [Sonar Object Detection: Applied ML (MSc Placement at Seabed.AI)](https://github.com/Kablan-ASBN/sonar-object-detection)
**Context:** Research project completed during Analytics Engineer placement at Seabed.AI (London, UK).

Full ML pipeline for 3,400+ noisy sidescan sonar images. Custom preprocessing, YOLO→VOC data conversion, Faster R-CNN baseline with ResNet-50 FPN, and adversarial domain adaptation (DANN + novel DCCAN hybrid) to improve generalization across sonar types. Evaluated with COCO mAP and FROC metrics. Included to demonstrate complex pipeline construction and model evaluation under real-world constraints — not a primary portfolio focus.

`Python` `PyTorch` `Faster R-CNN` `Domain Adaptation` `COCO metrics` `Computer Vision`

---

## Skills

| Area | Tools & Concepts |
|---|---|
| SQL | Joins, CTEs, window functions, aggregations, reconciliation queries, PostgreSQL |
| Python | Pandas, NumPy, scikit-learn, LightGBM, data cleaning, validation pipelines |
| Analytics Engineering | dbt (foundational), metric definitions, staging/mart modeling, KPI documentation |
| Data Quality | Completeness checks, deduplication, grain validation, audit-ready outputs |
| Visualization | Tableau, Power BI (supporting role — dashboard enablement) |
| ML & Modeling | Classification, class imbalance, model evaluation, transfer learning |
| Deployment & Tools | FastAPI, Git/GitHub, Jupyter, VS Code |
| Cloud & Infrastructure | AWS basics (S3), Azure OpenAI, Databricks (exposure), Linux (basic) |

---

## Currently Building

Building toward a production-grade dbt + Prefect + PostgreSQL pipeline project — publishing in April 2026.

---

*Open to Analytics Engineer, Technical Data Analyst, and related roles. U.S. Citizen. Eligible for public sector and government positions.*
