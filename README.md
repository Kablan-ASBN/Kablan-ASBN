# Kablan Assebian

**Analytics Engineer | Customer-Facing Technical Specialist**
`dbt` `Snowflake` `SQL` `Python` `Power BI` `Demo Delivery` `Customer Discovery` `Data Quality`

MSc Data Science (Distinction) | University of Greenwich (BCS-Accredited) | U.S. Citizen

English & French (native/bilingual) | Atlanta, GA | [![LinkedIn](https://img.shields.io/badge/LinkedIn-gomis--kablan-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/gomis-kablan/) [![Email](https://img.shields.io/badge/Email-gomis.k.assebian@gmail.com-EA4335?style=flat&logo=gmail)](mailto:gomis.k.assebian@gmail.com)

---

I build the data infrastructure layer between raw events and business decisions, and I translate it for the people making those decisions.

I work in dbt and Snowflake, building staging-intermediate-marts architectures with incremental models, snapshots, dbt-expectations, custom macros, and GitHub Actions CI/CD. At Georgia EPD, I designed an automated 15-stage data pipeline processing 35,000+ geospatial permit records at 99.98% accuracy, replacing a manual multi-step workflow. At Seabed.AI, I built data quality frameworks, KPI dashboards, and transformation pipelines that reduced manual reporting by 50%.

My focus is the layer between technical capability and business outcomes: explaining architecture trade-offs to non-technical buyers, running discovery conversations that surface real pain, modeling data so metrics are consistent and explainable, and shipping pipelines that audit cleanly. Open to Analytics Engineer and customer-facing technical roles.

Before analytics, I spent six years at a nonprofit across four regions of Côte d'Ivoire, co-leading fundraising and sponsor development. We secured $100K+ in cumulative funding through B2B corporate sponsors, high-net-worth individual donors, broad-base donor cultivation, and government grants. That work was customer-facing technical communication before I knew the term: discovery conversations with skeptical buyers, technical demos for non-technical audiences, and translating complex impact data into funding decisions.

---

## What I Work On

**Modern Data Stack & Analytics Engineering**
dbt fluency (staging-intermediate-marts, incremental models, snapshots, dbt-expectations, custom macros). Snowflake architecture (micro-partitioning, three-cache model, QUALIFY, TIME_TRAVEL, cost optimization). Modular SQL transformations, metric definitions, KPI documentation, and validation logic that catches reporting discrepancies before they reach stakeholders.

**Data Quality & Reconciliation**
End-to-end reconciliation workflows, root-cause investigation of KPI mismatches (join errors, grain issues, definition drift), completeness and consistency checks, and audit-ready outputs.

**Customer-Facing Technical Communication**
Live demo delivery, discovery question frameworks, technical sales conversations, requirements gathering across competing stakeholders, and translating prospect pain into demonstrable solutions.

**Production Engineering Discipline**
GitHub Actions CI/CD, SQLFluff style enforcement, dbt run logs analysis, observability through alerting, and reproducible workflows built to be testable and maintainable.

---

## Projects

### [SaaS Metrics Pipeline: dbt + Snowflake](https://github.com/Kablan-ASBN/saas_metrics_pipeline)
**The problem:** SaaS companies track revenue at the event level (signups, upgrades, cancellations), but the raw data does not directly answer the financial questions that matter: Is MRR growing? What is driving churn? Which cohorts retain best?

Built an end-to-end dbt project running on Snowflake. Generates synthetic but realistic B2B subscription data (800 customers, 36 months). Executes models across staging, intermediate, and mart layers. Includes incremental models for fact tables, SCD Type 2 snapshots for plan changes, 10+ dbt tests covering not_null, unique, accepted_values, and referential integrity, dbt-expectations for range and pattern validation, and custom macros for surrogate key generation. GitHub Actions CI/CD runs `dbt test` and `SQLFluff` lint on every push. Produces a monthly MRR waterfall, cohort retention curves, customer health segmentation, and LTV estimates.

`dbt` `Snowflake` `SQL` `Python` `GitHub Actions` `Incremental Models` `SCD Type 2` `dbt-expectations`

---

### [Stripe API Integration: Subscription Billing Demo](https://github.com/Kablan-ASBN/stripe-billing-demo)
**The problem:** Customer-facing technical roles at fintech vendors require demonstrating API fluency in live conversation, not just describing it on a resume.

Built a Python application using the Stripe API to programmatically create customers, attach payment methods, generate subscription billing schedules, handle payment webhooks, and reconcile billing events against an internal ledger. Includes error handling for failed payments, dunning logic for retry scenarios, and a small dashboard showing MRR and churn calculated directly from Stripe data.

`Python` `Stripe API` `FastAPI` `Webhooks` `Subscription Billing` `Reconciliation`

---

### [Revenue & KPI Reconciliation: Commerce Analytics Case Study](https://github.com/Kablan-ASBN/revenue-kpi-reconciliation)
**The problem:** Finance, Operations, and Marketing report different revenue numbers from the same source data. This project investigates why and builds the reconciliation logic to resolve it.

Built on the Olist Brazilian E-Commerce dataset. Aggregates item-, freight-, and payment-level data to a consistent order-level grain. Defines and compares four revenue metrics (gross items-only, gross with freight, paid, net non-canceled proxy). Identifies root causes of mismatches including canceled orders with captured payments and multi-item joins at the wrong grain. Produces operational validation checks designed for production monitoring. The pattern (different teams, different definitions, same source data) is one of the most common scenarios in customer-facing analytics work across data vendors.

`Python` `Pandas` `SQL-style aggregation` `Metric documentation` `Data validation`

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

Full ML pipeline for 3,400+ noisy sidescan sonar images. Custom preprocessing, YOLO-to-VOC data conversion, Faster R-CNN baseline with ResNet-50 FPN, and adversarial domain adaptation (DANN + novel DCCAN hybrid) to improve generalization across sonar types. Evaluated with COCO mAP and FROC metrics. Included to demonstrate research-grade ML capability and pipeline construction under real-world constraints.

`Python` `PyTorch` `Faster R-CNN` `Domain Adaptation` `COCO metrics` `Computer Vision`

---

## Skills

| Area | Tools & Concepts |
|---|---|
| Modern Data Stack | dbt (incremental, snapshots, tests, dbt-expectations, macros), Snowflake (architecture, QUALIFY, TIME_TRAVEL, cost optimization), PostgreSQL |
| SQL | Joins, CTEs, window functions, aggregations, reconciliation queries, query optimization, grain control |
| Python | Pandas, NumPy, scikit-learn, LightGBM, FastAPI, Matplotlib, validation pipelines, API integration |
| Customer-Facing | Live demo delivery, discovery question frameworks, technical sales conversations, stakeholder communication |
| Analytics Engineering | Staging-intermediate-marts modeling, metric definitions, KPI documentation, semantic layer fluency |
| Data Quality | Completeness checks, deduplication, grain validation, referential integrity, audit-ready outputs |
| BI & Visualization | Power BI (DAX), Tableau, dashboard design, data storytelling, self-service analytics |
| Production Engineering | GitHub Actions CI/CD, SQLFluff, observability, dbt run logs analysis, alerting |
| ML & Modeling | Classification, class imbalance handling, model evaluation, transfer learning, domain adaptation |
| Cloud & Infrastructure | AWS (S3, IAM), Docker, PostgreSQL, Git/GitHub, Linux |
| Tools & Workflow | Excel, Jupyter, VS Code, Agile, ArcGIS Online, Salesforce |

---

## Currently Building

- Stripe API integration project: subscription billing, webhook handling, and ledger reconciliation, demonstrating fintech-relevant API patterns
- Live demo recordings of dbt + Snowflake architecture walkthroughs on YouTube, designed to translate technical decisions into customer-facing narratives
- Production-style portfolio extensions: incremental model patterns, observability through Slack alerting, dbt run logs analysis
- Active in DataTalks.Club Slack and dbt Community Slack, occasional LinkedIn writing on SaaS metrics layering and incremental model patterns

---

*Open to Analytics Engineer and customer-facing technical roles. U.S. Citizen. Based in Atlanta, GA. Open to relocation: Chicago, NYC, Baltimore, Philadelphia.*
