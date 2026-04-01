# Kablan Assebian

**Data Analyst | Analytics Engineer**
`SQL` `Python` `Power BI` `Tableau` `dbt-Style Modeling` `ETL` `Data Quality`

MSc Data Science (Distinction) | University of Greenwich (BCS-Accredited) | U.S. Citizen

English & French (native/bilingual) | Atlanta, GA | [![LinkedIn](https://img.shields.io/badge/LinkedIn-gomis--kablan-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/gomis-kablan/) [![Email](https://img.shields.io/badge/Email-gomis.k.assebian@gmail.com-EA4335?style=flat&logo=gmail)](mailto:gomis.k.assebian@gmail.com)

---

I build analytics systems where the numbers are consistent, explainable, and audit-ready.

Currently at Georgia EPD, I designed an automated data pipeline processing 35,000+ geospatial permit records at 99.98% accuracy, replacing a manual multi-step workflow. Previously at Seabed.AI, I built data quality frameworks, KPI dashboards, and transformation pipelines that reduced manual reporting by 50%.

My focus is the layer between raw data and business decisions: transformation logic, metric definitions, validation pipelines, and documentation that makes outputs trustworthy and reproducible. Open to Data Analyst, Analytics Engineer, and related roles.

Before analytics, I spent six years co-founding and scaling a nonprofit across four regions of Cote d'Ivoire. I built the team from the ground up, managed cross-regional operations, and coordinated stakeholders with competing priorities on a limited budget. That experience showed me what happens when data systems are absent or unreliable. It shapes how I work today: data quality is a prerequisite for organizational trust, not just a technical checkbox. It also means I bring project leadership, stakeholder communication, and the ability to move initiatives from ambiguity to execution.

---

## What I Work On

**Data Analysis & Reporting**
SQL-driven analysis, KPI dashboards (Power BI, Tableau), stakeholder-ready reporting, root cause investigation, trend and variance analysis, and translating complex data into actionable business recommendations.

**Analytics Engineering**
Modular SQL transformations, staging and mart layers, dbt-style modeling, metric grain standardization, and validation logic that catches reporting discrepancies before they reach stakeholders.

**Data Quality & Reconciliation**
End-to-end reconciliation workflows, root-cause investigation of KPI mismatches (join errors, grain issues, definition drift), completeness and consistency checks, and audit-ready outputs.

**ETL & Python Pipelines**
Reproducible Python workflows for data ingestion, cleaning, transformation, and automated validation. Built to be readable, testable, and maintainable.

---

## Projects

### [Revenue & KPI Reconciliation: Commerce Analytics Case Study](https://github.com/Kablan-ASBN/revenue-kpi-reconciliation)
**The problem:** Finance, Operations, and Marketing report different revenue numbers from the same source data. This project investigates why and builds the reconciliation logic to resolve it.

Built on the Olist Brazilian E-Commerce dataset. Aggregates item-, freight-, and payment-level data to a consistent order-level grain. Defines and compares four revenue metrics (gross items-only, gross with freight, paid, net non-canceled proxy). Identifies root causes of mismatches including canceled orders with captured payments and multi-item joins at the wrong grain. Produces operational validation checks designed for production monitoring.

`Python` `Pandas` `SQL-style aggregation` `Metric documentation` `Data validation`

---

### [SaaS Metrics Pipeline](https://github.com/Kablan-ASBN/saas_metrics_pipeline)
**The problem:** SaaS companies track revenue at the event level (signups, upgrades, cancellations), but the raw data does not directly answer the financial questions that matter: Is MRR growing? What is driving churn? Which cohorts retain best?

Built an end-to-end pipeline that transforms subscription lifecycle events into core SaaS financial metrics. Generates synthetic but realistic B2B subscription data (800 customers, 36 months). Executes dbt-style SQL models across staging, intermediate, and mart layers. Produces a monthly MRR waterfall, cohort retention curves, customer health segmentation, and LTV estimates. Includes 5 automated data quality checks that run on every pipeline execution.

`Python` `SQL` `Pandas` `dbt-style modeling` `Data quality` `SaaS metrics`

---

### [Bank Loan Risk Analysis](https://github.com/Kablan-ASBN/bank-loan-risk-analysis)
**The problem:** Default risk models trained on imbalanced data produce misleadingly high accuracy while failing to identify the cases that matter most.

Analyzed 1.2M+ Lending Club loan records. Built an end-to-end pipeline covering ingestion, cleaning, validation, and feature engineering. Improved default recall from 5.4% to 67.1% through class imbalance handling and downsampling. Emphasis on business trade-offs and decision-relevant reporting: ROC-AUC, precision-recall curves, and confusion matrices framed around lending risk decisions, not raw model accuracy.

`Python` `Pandas` `scikit-learn` `ROC-AUC` `Precision-Recall` `Class imbalance`

---

### [Fraud Detection System: Real-Time ML Pipeline](https://github.com/Kablan-ASBN/fraud-detection-system)
**The problem:** Credit card fraud detection requires handling extreme class imbalance (577:1) while maintaining low false negatives and real-time throughput.

Built a production-oriented ML pipeline using Dask-based ETL that scales with transaction volume. Trained a LightGBM classifier achieving 0.905 ROC-AUC and 87% fraud recall. Deployed via FastAPI as a REST endpoint for real-time inference. Applied threshold tuning and scale_pos_weight adjustment to minimize false negatives. Modularized codebase with separate training, evaluation, and deployment modules.

`Python` `LightGBM` `Dask` `FastAPI` `ETL pipeline` `Class imbalance` `Model deployment`

---

### [Sonar Object Detection: Deep Learning Research](https://github.com/Kablan-ASBN/sonar-object-detection)
**Context:** MSc Data Science research project, University of Greenwich.

Full ML pipeline for 3,400+ noisy sidescan sonar images. Custom preprocessing, YOLO-to-VOC data conversion, Faster R-CNN baseline with ResNet-50 FPN, and adversarial domain adaptation (DANN + novel DCCAN hybrid) to improve generalization across sonar types. Evaluated with COCO mAP and FROC metrics. Included to demonstrate complex pipeline construction and model evaluation under real-world constraints.

`Python` `PyTorch` `Faster R-CNN` `Domain Adaptation` `COCO metrics` `Computer Vision`

---

## Skills

| Area | Tools & Concepts |
|---|---|
| SQL | Joins, CTEs, window functions, aggregations, reconciliation queries, PostgreSQL, SQLite |
| Python | Pandas, NumPy, scikit-learn, LightGBM, Matplotlib, data cleaning, validation pipelines |
| Analytics Engineering | dbt-style modeling, metric definitions, staging/intermediate/mart layers, KPI documentation |
| Data Quality | Completeness checks, deduplication, grain validation, referential integrity, audit-ready outputs |
| BI & Visualization | Power BI (DAX), Tableau, dashboard design, data storytelling, self-service analytics |
| ML & Modeling | Classification, class imbalance handling, model evaluation, transfer learning, domain adaptation |
| Cloud & Infrastructure | AWS (S3, IAM), Docker, PostgreSQL, Git/GitHub, Linux |
| Tools & Workflow | Excel, Jupyter, VS Code, Agile, ArcGIS Online, Salesforce |

---

## Currently Building

- Automated geospatial data pipeline at Georgia EPD (15 processing stages, 35K+ records, 99.98% validation accuracy)
- End-to-end dbt + Airflow + PostgreSQL portfolio project (targeting July 2026)

---

*Open to Data Analyst, Analytics Engineer, and related roles. U.S. Citizen. Based in Atlanta, GA.*
