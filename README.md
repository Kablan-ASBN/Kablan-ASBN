# Gomis Kablan Assebian

**Data Scientist & Analytics Engineer**
`Python` `PyTorch` `scikit-learn` `LightGBM` `SQL` `Statistics` `FastAPI` `Docker` `Power BI` `Tableau`

MSc Data Science (Distinction) | University of Greenwich (BCS-Accredited) | U.S. Citizen

English & French (native/bilingual) | Metro Atlanta, GA | [![LinkedIn](https://img.shields.io/badge/LinkedIn-gomis--kablan-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/gomis-kablan/) [![Email](https://img.shields.io/badge/Email-gomis.k.assebian@gmail.com-EA4335?style=flat&logo=gmail)](mailto:gomis.k.assebian@gmail.com)

---

I build and ship machine learning and analytics that turn messy data into decisions, making the results clear to the people who act on them.

My strongest work is in applied ML and credit risk: an end-to-end scorecard and model risk management system on 307K real loan applications, where a Weight of Evidence scorecard champion runs against a calibrated LightGBM challenger (AUC 0.7497 vs 0.7732 on a held-out set of 61,503 applications), with Regulation B adverse action reason codes, a fair lending test, PSI/CSI drift monitoring, and a FastAPI scoring service with 35 tests in CI. Alongside that sits my MSc research: a domain-adversarial object detection architecture I proposed and built in PyTorch for sidescan sonar.

At the Georgia Environmental Protection Division (EPD), I consolidate permit data from three source systems, including the agency's Salesforce/Clarity database, into one validated geospatial dataset of 35,000+ records using SQL and Python, automate the recurring T-SQL and GIS steps, and scoped a migration of the legacy Access database to SQL Server covering 39 views, 5 staging tables, 2 stored procedures, and a 22-check QA framework.

My focus is the layer between technical capability and business outcomes: choosing the right metric, evaluating models honestly including where they fail, modeling data so numbers are consistent and explainable, and translating all of it for non-technical stakeholders. Open to Data Analyst, Data Scientist, Analytics Engineer, and customer-facing technical roles.

Before analytics, I spent six years at a nonprofit across four regions of Côte d'Ivoire, leading reporting and co-leading sponsor and donor development, where we secured $100K+ in cumulative funding. Most of that was customer-facing technical communication before I had the term for it: explaining complex impact data to non-technical decision-makers, gathering requirements across competing stakeholders, and turning analysis into decisions people could act on.

---

## What I Work On

**Machine Learning and Applied ML**
Supervised classification, deep learning, and class-imbalance handling, with a focus on decision-relevant evaluation (ROC-AUC, precision-recall, Brier, COCO/FROC) rather than headline accuracy. Credit risk modeling (WOE/IV, PDO points scaling, probability calibration, fairness analysis), model serving via FastAPI, transfer learning, and domain adaptation. PyTorch, scikit-learn, LightGBM.

**Analytics Engineering**
Layered SQL modeling in the staging, intermediate, and marts pattern, with dependency-ordered runs and data quality checks built into the pipeline. Grain control and one-to-one join validation, explicit metric definitions, and reconciliation logic that catches reporting discrepancies before they reach stakeholders. SQL Server (T-SQL), PostgreSQL, SQLite.

**Data Quality and Reconciliation**
End-to-end reconciliation workflows, root cause investigation of KPI mismatches (join errors, grain issues, definition drift), completeness and referential integrity checks, and severity-rated validation suites designed to run in production.

**Communication and Stakeholder Translation**
Explaining architecture and model trade-offs to non-technical audiences, requirements gathering across competing stakeholders, and turning analysis into decisions. Comfortable being the person who diagnoses a problem to root cause and then explains the fix plainly.

**Engineering Discipline**
Typed validation modules shared between training and serving, pytest unit and integration tests, GitHub Actions CI with lint and a smoke run, Docker, and configuration files that put every threshold a reviewer would challenge in one place.

---

## Projects

### [Credit Risk Scorecard & Model Risk Management System](https://github.com/Kablan-ASBN/credit-risk-engine)
**The problem:** most default-prediction projects stop at "trained a model, got a good AUC." A bank cannot deploy that. It needs decisions it can explain to a declined applicant (Regulation B), probabilities honest enough to price risk with, outcomes tested for disparate impact, and drift monitoring after launch.

Built on 307K real Home Credit applications, structured the way bank model development teams work under SR 11-7 and ECOA. A Weight of Evidence scorecard champion with PDO points scaling (base 650 at 20:1 odds) runs against a calibrated LightGBM challenger: AUC 0.7497 vs 0.7732 on 61,503 held-out applications, and that 2.4-point gap is the measured price of interpretability. TreeSHAP adverse action reason codes translate declines into the plain language the law requires. Fair lending analysis passed gender against the four-fifths rule (0.867) and flagged age group at 0.670 with a 0.249 equal opportunity gap. Isotonic calibration is reported as a null result (Brier 0.0667 to 0.0669) rather than hidden. Expected loss on the approved book runs 1.78% of exposure at baseline and 3.39% under a severe stress scenario. 35 tests, including a train-then-serve integration test, run in CI on every push.

`Python` `LightGBM` `scikit-learn` `WOE/IV` `Probability calibration` `SHAP` `Fair lending` `PSI/CSI monitoring` `FastAPI` `Docker` `CI/CD`

---

### [Sonar Object Detection with Domain Adaptation](https://github.com/Kablan-ASBN/sonar-object-detection)
**Context:** MSc Data Science dissertation, University of Greenwich, from a professional placement at Seabed.AI.

Full detection pipeline over 3,465 annotated sidescan sonar images: YOLO to Pascal VOC conversion, class remapping, an 80/10/10 stratified split, and a Faster R-CNN (ResNet-50 FPN) baseline. DCCAN is a domain adaptation architecture I proposed and built, combining global (DANN-style), class-conditional (CDAN-style), and proposal-level adversarial alignment, each through a gradient reversal layer. On the raw target domain it led every variant tested: AP50 0.163 against 0.152 for the best no-adaptation baseline and 0.091 for DANN, mAR@100 0.155 against 0.104, and FROC recall rising to about 0.47 at higher false-positive allowances. Also diagnosed and fixed a numerical stability failure that broke CDAN-style alignment under automatic mixed precision, which is what made the model trainable on a single A100.

`Python` `PyTorch` `Faster R-CNN` `Domain adaptation` `COCO metrics` `FROC` `Mixed precision`

---

### [Revenue & KPI Reconciliation](https://github.com/Kablan-ASBN/revenue-kpi-reconciliation)
**The problem:** Finance, Operations, and Marketing report different revenue numbers from the same source data. The instinct is to assume bad data. Usually it is a definition difference nobody wrote down.

Built on the Olist Brazilian E-Commerce dataset. Aggregated items and payments to order grain before joining, with `validate="one_to_one"` asserting grain integrity at every step, which prevents the fan-out that inflates most revenue reporting. Defined and compared four revenue metrics: the $2.4M gap between items-only revenue ($13.6M) and paid revenue ($16.0M) turned out to be freight and cancellation scope, not error, and all four definitions converged within $0.2M once freight was included. Classified every order into one of five mismatch buckets and added seven severity-rated validation checks. The `payment_no_items` bucket is under 1% of orders but drives about $130K of unexplained delta, which is the escalation worth making.

`Python` `pandas` `Grain control` `Metric definition` `Data validation`

---

### [SaaS Metrics Pipeline](https://github.com/Kablan-ASBN/saas_metrics_pipeline)
**The problem:** SaaS revenue is tracked at the event level, but the raw event log does not answer the questions that matter: is MRR growing, where is the growth coming from, and which cohorts retain?

Nine SQL models in dbt-style layers (4 staging, 2 intermediate, 3 marts) executed in dependency order by a Python runner script on SQLite, over synthetic B2B subscription data covering 800 customers, 853 subscriptions, and 1,682 lifecycle events across 36 months. The interesting part is the intermediate layer: a monthly subscription spine that carries MRR forward through months with no events, which is what makes the MRR waterfall, cohort retention, and LTV marts possible. Five data quality assertions run after every execution. I built the orchestration by hand rather than reaching for the tool, so I can explain every step of the DAG, and the SQL lifts into a dbt project with minimal changes. Known limits are stated in the README, including full rebuilds with no incremental materialization.

`SQL` `Python` `SQLite` `Layered modeling` `Data quality checks`

---

### [Bank Loan Risk Analysis](https://github.com/Kablan-ASBN/bank-loan-risk-analysis)
**The problem:** default models trained on imbalanced data produce misleadingly high accuracy while missing the cases that matter most.

1,265,976 resolved Lending Club loans out of 2.26M raw rows, cleaned to 16 features. A logistic baseline hits 80.7% accuracy by predicting "fully paid" for nearly everything and catches 5.4% of defaults. Class balancing takes accuracy down to 65.2% and default recall up to 67.1%, with F1 moving from 0.098 to 0.658 at flat AUC (0.710 to 0.7105), which is the point: the discriminatory power did not change, the decision behavior did. The README states the limitation plainly, that both models were evaluated in-sample without a held-out split, because a portfolio piece that hides its own caveats is worth less than one that names them.

`Python` `pandas` `scikit-learn` `Class imbalance` `ROC-AUC` `Precision-Recall`

---

### [NGO Donor & Impact Dashboard (Côte d'Ivoire)](https://github.com/Kablan-ASBN/NGO-Donor-Impact-Dashboard-C-te-d-Ivoire-)
Reporting workflow built for a foundation operating across four regions of Côte d'Ivoire from 2018 to 2024. Four regional teams submitted data in different formats, consolidation was manual and slow, and leadership had no single trusted view. I standardized collection with locked-KPI Excel templates, automated calculation and validation with VBA macros, consolidated to a structured CSV, and built a Tableau dashboard covering donor retention against a 75% target, funds by donor origin, and students supported by region, refreshed from a central SharePoint folder. On-time reporting reached about 95%.

`Excel` `VBA` `Tableau` `KPI definition` `Process standardization`

---

### [S&P 500 Time-Series Forecasting (ARIMA, R)](https://github.com/Kablan-ASBN/sp500-arima-forecasting)
Classical time-series work done properly: S&P 500 adjusted prices from 2000 to 2023 converted to log returns, stationarity tested with ADF and ACF/PACF inspection, a manually specified ARIMA(1,0,1) compared against `auto.arima` on MSE, RMSE, MAE, AIC, and BIC, and residual diagnostics run to validate the assumptions. The manual specification won on the balance of fit, stability, and interpretability. The point is not to forecast markets, it is to show how a forecasting model is specified, tested, and defended.

`R` `quantmod` `forecast` `tseries` `ARIMA` `Residual diagnostics`

---

## Skills

| Area | Tools & Concepts |
|---|---|
| Machine Learning & Modeling | classification, deep learning, class-imbalance handling, model evaluation (ROC-AUC, precision-recall, Brier, COCO/FROC), probability calibration, transfer learning, domain adaptation; PyTorch, scikit-learn, LightGBM |
| Credit Risk & Model Risk | WOE/IV scorecards, PDO points scaling, champion/challenger, adverse action reason codes (SHAP), fair lending analysis (disparate impact, equal opportunity), PSI/CSI monitoring, expected loss and stress scenarios, SR 11-7-style model documentation |
| Statistics & Experimentation | exploratory data analysis, hypothesis testing, experimental design, ablation studies, regression, ARIMA forecasting |
| Python | pandas, NumPy, scikit-learn, LightGBM, FastAPI, Matplotlib, validation pipelines |
| SQL | joins, CTEs, window functions, aggregations, reconciliation queries, grain control; SQL Server (T-SQL), PostgreSQL, SQLite |
| Analytics Engineering | layered modeling (staging, intermediate, marts), dependency-ordered pipeline runs, metric definitions, data quality assertions |
| Data Quality | completeness checks, deduplication, grain validation, referential integrity, severity-rated validation suites |
| BI & Visualization | Power BI (DAX), Tableau, Excel (advanced, VBA), dashboard design, self-service reporting |
| Engineering | GitHub Actions CI/CD, pytest, Docker, Git/GitHub, Linux, reproducible workflows |
| Communication | translating technical for non-technical audiences, stakeholder communication, requirements gathering, root cause investigation |
| Cloud | Google Cloud Platform (training-data pipelines), Microsoft Azure |
| Tools & Workflow | Excel, Jupyter, VS Code, Agile, ArcGIS Online, Salesforce, R |

---

## Currently

- Extending the credit risk system: out-of-time validation, reject inference, and a fairness-constrained retrain of the age-group flag
- Rebuilding the SQL and Python foundations from blank, daily, ahead of a PostgreSQL and dbt platform build

---

*Open to Data Analyst, Analytics Engineer, Data Engineer, Solutions/Implementation Engineer, and credit risk roles. U.S. Citizen. Based in Metro Atlanta, GA. Open to remote or relocation (Chicago, Philadelphia, Dallas, New York City).*
