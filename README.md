# Full Legal Name: Gomis Kablan Assebian
# Professional Name: Kablan Assebian
 
**Data Scientist & Analytics Engineer**
`Python` `Machine Learning` `PyTorch` `SQL` `Statistics` `dbt` `Snowflake` `Power BI`
 
MSc Data Science (Distinction) | University of Greenwich (BCS-Accredited) | U.S. Citizen
 
English & French (native/bilingual) | Atlanta, GA | [![LinkedIn](https://img.shields.io/badge/LinkedIn-gomis--kablan-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/gomis-kablan/) [![Email](https://img.shields.io/badge/Email-gomis.k.assebian@gmail.com-EA4335?style=flat&logo=gmail)](mailto:gomis.k.assebian@gmail.com)
 
---
 
I build and ship machine learning and analytics that turn messy data into decisions, and I make the results clear to the people who act on them.
 
My strongest work is in applied ML: an end-to-end credit risk scorecard and model risk management system (WOE scorecard champion vs calibrated LightGBM challenger, AUC 0.77 on 307K real applications, with ECOA adverse action reason codes, fair lending analysis, and PSI drift monitoring behind a FastAPI scoring service), a novel domain-adversarial object-detection architecture from my MSc research (Faster R-CNN, PyTorch), and a default-risk pipeline over 1.2M+ loan records. At Georgia EPD I designed an automated 15-stage pipeline processing 35,000+ geospatial permit records at 99.98% accuracy, replacing a manual multi-step workflow. I also work in dbt and Snowflake, building staging-intermediate-marts models that are tested, documented, and CI/CD-backed.
 
My focus is the layer between technical capability and business outcomes: choosing the right metric, evaluating models honestly including where they fail, modeling data so numbers are consistent and explainable, and translating all of it for non-technical stakeholders. Open to Data Scientist, Analytics Engineer, and customer-facing technical roles.
 
Before analytics, I spent six years at a nonprofit across four regions of Côte d'Ivoire, leading reporting and co-leading sponsor and donor development, where we secured $100K+ in cumulative funding. Most of that was customer-facing technical communication before I had the term for it: explaining complex impact data to non-technical decision-makers, gathering requirements across competing stakeholders, and turning analysis into decisions people could act on.
 
---
 
## What I Work On
 
**Machine Learning & Applied ML**
Supervised classification, deep learning, and class-imbalance handling, with a focus on decision-relevant evaluation (ROC-AUC, precision-recall, COCO/FROC) rather than headline accuracy. Credit risk modeling (WOE/IV, PDO scorecards, probability calibration, fairness analysis), model deployment via FastAPI, transfer learning, and domain adaptation. PyTorch, scikit-learn, LightGBM.
 
**Analytics Engineering & Modern Data Stack**
dbt fluency (staging-intermediate-marts, incremental models, snapshots, dbt-expectations, custom macros). Snowflake architecture (micro-partitioning, three-cache model, QUALIFY, TIME_TRAVEL, cost optimization). Modular SQL, metric definitions, and validation logic that catches reporting discrepancies before they reach stakeholders.
 
**Data Quality & Reconciliation**
End-to-end reconciliation workflows, root-cause investigation of KPI mismatches (join errors, grain issues, definition drift), completeness and consistency checks, and audit-ready outputs.
 
**Communication & Stakeholder Translation**
Explaining architecture and model trade-offs to non-technical audiences, requirements gathering across competing stakeholders, and turning analysis into decisions. Comfortable being the person who diagnoses a problem to root cause and then explains the fix plainly.
 
**Production Engineering Discipline**
GitHub Actions CI/CD, SQLFluff style enforcement, dbt run logs analysis, observability through alerting, and reproducible workflows built to be testable and maintainable.
 
---
 
## Projects
 
### [Credit Risk Scorecard & Model Risk Management System](https://github.com/Kablan-ASBN/credit-risk-engine)
**The problem:** Most default-prediction projects stop at "trained a model, got a good AUC." A bank cannot deploy that. It needs decisions it can explain to a declined applicant (Regulation B), probabilities honest enough to price risk with, outcomes tested for disparate impact, and drift monitoring after launch.
 
Built the full system on 307K real Home Credit applications, structured the way bank model development teams work under SR 11-7 and ECOA. A Weight of Evidence scorecard champion with PDO points scaling sits next to a calibrated LightGBM challenger (AUC 0.7732 vs 0.7497; the 2.4-point gap is the measured price of interpretability). SHAP-based adverse action reason codes translate declines into the plain language the law requires. Fair lending analysis surfaced a real age-group disparate impact (0.67 ratio against the four-fifths rule). Includes PSI/CSI drift monitoring, expected loss with CCAR-style stress scenarios, a data quality gate shared between training and serving, a FastAPI scoring service, and an SR 11-7-style model card. 35 tests, including a train-then-serve integration test, run in CI on every push.
 
`Python` `LightGBM` `scikit-learn` `WOE/IV` `Probability calibration` `SHAP` `Fair lending` `PSI monitoring` `FastAPI` `Docker` `CI/CD`
 
---
 
### [Sonar Object Detection: Deep Learning Research](https://github.com/Kablan-ASBN/sonar-object-detection)
**Context:** MSc Data Science research project, University of Greenwich.
 
Full ML pipeline for 3,400+ noisy sidescan sonar images. Custom preprocessing, YOLO-to-VOC conversion, a Faster R-CNN baseline with ResNet-50 FPN, and adversarial domain adaptation (DANN plus a novel DCCAN hybrid) to improve generalization across sonar types, lifting detection accuracy about 80% over the standard domain-adaptation baseline. Diagnosed and fixed a numerical-stability failure under mixed-precision training. Evaluated with COCO mAP and FROC metrics.
 
`Python` `PyTorch` `Faster R-CNN` `Domain Adaptation` `COCO metrics` `Computer Vision`
 
---
 
### [Bank Loan Risk Analysis](https://github.com/Kablan-ASBN/bank-loan-risk-analysis)
**The problem:** Default-risk models trained on imbalanced data produce misleadingly high accuracy while missing the cases that matter most.
 
Analyzed 1.2M+ Lending Club loan records. Built an end-to-end pipeline covering ingestion, cleaning, validation, and feature engineering. Improved default recall from 5.4% to 67.1% through class-imbalance handling and downsampling. Framed results around lending-risk decisions (ROC-AUC, precision-recall curves, confusion matrices), not raw model accuracy.
 
`Python` `Pandas` `scikit-learn` `ROC-AUC` `Precision-Recall` `Class imbalance`
 
---
 
### [Revenue & KPI Reconciliation: Commerce Analytics Case Study](https://github.com/Kablan-ASBN/revenue-kpi-reconciliation)
**The problem:** Finance, Operations, and Marketing report different revenue numbers from the same source data. This project investigates why and builds the reconciliation logic to resolve it.
 
Built on the Olist Brazilian E-Commerce dataset. Aggregates item-, freight-, and payment-level data to a consistent order-level grain. Defines and compares four revenue metrics. Identifies root causes of mismatches including canceled orders with captured payments and multi-item joins at the wrong grain. Produces operational validation checks designed for production monitoring.
 
`Python` `Pandas` `SQL-style aggregation` `Metric documentation` `Data validation`
 
---
 
### [SaaS Metrics Pipeline: dbt + Snowflake](https://github.com/Kablan-ASBN/saas_metrics_pipeline)
**The problem:** SaaS revenue is tracked at the event level, but the raw data does not directly answer the financial questions that matter: Is MRR growing? What drives churn? Which cohorts retain best?
 
End-to-end dbt project on Snowflake over synthetic but realistic B2B subscription data (800 customers, 36 months). Models across staging, intermediate, and mart layers, with incremental fact tables, SCD Type 2 snapshots, 10+ dbt tests, dbt-expectations validation, and custom macros for surrogate keys. GitHub Actions runs `dbt test` and `SQLFluff` lint on every push. Produces a monthly MRR waterfall, cohort retention curves, health segmentation, and LTV estimates.
 
`dbt` `Snowflake` `SQL` `Python` `GitHub Actions` `Incremental Models` `SCD Type 2` `dbt-expectations`
 
---
 
## Skills
 
| Area | Tools & Concepts |
|---|---|
| Machine Learning & Modeling | classification, deep learning, class-imbalance handling, model evaluation (ROC-AUC, precision-recall, Brier, COCO/FROC), probability calibration, transfer learning, domain adaptation; PyTorch, scikit-learn, LightGBM |
| Credit Risk & Model Risk | WOE/IV scorecards, PDO scaling, champion/challenger, adverse action reason codes (SHAP), fair lending analysis (disparate impact, equal opportunity), PSI/CSI monitoring, expected loss and stress scenarios, SR 11-7-style documentation |
| Statistics & Experimentation | exploratory data analysis, hypothesis testing, experimental design, ablation studies, regression |
| Python | Pandas, NumPy, scikit-learn, LightGBM, FastAPI, Matplotlib, validation pipelines, API integration |
| SQL | joins, CTEs, window functions, aggregations, reconciliation queries, query optimization, grain control |
| Modern Data Stack | dbt (incremental, snapshots, tests, dbt-expectations, macros), Snowflake (architecture, QUALIFY, TIME_TRAVEL, cost optimization), PostgreSQL |
| LLM & Cloud AI | Azure OpenAI (LLM-assisted workflows), large language model concepts |
| Data Quality | completeness checks, deduplication, grain validation, referential integrity, audit-ready outputs |
| BI & Visualization | Power BI (DAX), Tableau, dashboard design, data storytelling, self-service analytics |
| Production Engineering | GitHub Actions CI/CD, SQLFluff, observability, dbt run logs analysis, alerting |
| Communication | translating technical for non-technical audiences, stakeholder communication, requirements gathering, root-cause investigation |
| Cloud & Infrastructure | Microsoft Azure, AWS (S3, IAM), Docker, Git/GitHub, Linux |
| Tools & Workflow | Excel, Jupyter, VS Code, Agile, ArcGIS Online, Salesforce |
 
---
 
## Currently Building
 
- Deepening the credit risk system: out-of-time validation patterns, reject inference, and fairness-constrained retraining
- Production-style portfolio extensions: incremental model patterns, observability through Slack alerting, dbt run logs analysis
- Exploring LLM evaluation and Azure OpenAI workflows
- Active in DataTalks.Club Slack and dbt Community Slack, with occasional LinkedIn writing on SaaS metrics layering and incremental model patterns
---
 
*Open to Data Analyst, Data Scientist, Analytics Engineer, and customer-facing technical roles. U.S. Citizen. I am currently based in Atlanta, GA. Open to relocation.*
 





















