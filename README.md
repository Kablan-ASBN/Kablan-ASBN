# Hi, I’m Kablan Assebian  
*(Legal name: Gomis Kablan Assebian)*

**Data Scientist (Applied Analytics & Risk Modeling)**  
SQL • Python • Analytics Engineering • Machine Learning • Power BI  
MSc Data Science (Distinction) — University of Greenwich

I build **reliable analytics pipelines and decision-ready metrics** that help
**risk, finance, and operations teams** trust their numbers and act on them.

My work focuses on:
- turning messy transactional data into **clean, reconciled KPIs**
- designing **ETL pipelines with validation and monitoring**
- explaining *why* metrics differ across teams, not just computing them

I began my career in **neuroscience**, working with noisy experimental data,
then transitioned into **data science and analytics engineering**.
That background trained me to think carefully about **data quality, assumptions,
and real-world constraints** — the same issues that drive most business reporting problems.

---

## Most Recent Role

### **Analytics Engineer (AI/ML) — Seabed.AI (London, UK)**  
AI startup building analytics and computer vision systems for offshore operations.

- Designed and maintained **SQL + Python ETL pipelines** with automated data-quality checks, reducing manual data preparation by ~50%.
- Aggregated **multi-source operational data** into consistent, order- and job-level metrics used by engineering and leadership teams.
- Built **Power BI dashboards** to monitor pipeline health, data coverage, and model performance.
- Partnered with data scientists and engineers on **AWS + Databricks** workflows, aligning exploratory analysis with production reporting.
- Applied transfer learning and domain adaptation techniques to improve model robustness and reduce performance degradation under real-world data shifts.

This role emphasized **analytics engineering, metric consistency, and stakeholder-facing reporting**, alongside applied ML.

---

## Selected Projects

### 🔹 **Revenue & KPI Reconciliation (Commerce Analytics)**  
**Order-Level Revenue Reconciliation Case Study**  
*(Olist Brazilian E-Commerce Dataset)*

Finance, Operations, and Marketing teams often report different revenue numbers
from the same data. This project investigates **why those discrepancies occur**
and demonstrates how to resolve them through **clear definitions, correct grain,
and validation checks**.

**What I did:**
- Aggregated item-, freight-, and payment-level data to a **single order-level grain**
- Defined and compared multiple revenue metrics:
  - Gross (items only)
  - Gross (items + freight)
  - Paid revenue
  - Net revenue (non-canceled proxy)
- Identified root causes of mismatches:
  - canceled orders with captured payments
  - multi-item and multi-payment orders
  - joins performed at the wrong grain
- Designed **operational validation checks** suitable for production monitoring

**Key findings:**
- Item-only revenue understates customer-paid value by ~15%
- Item + freight revenue aligns closely with paid revenue (≈1% delta)
- Most discrepancies are caused by **implicit assumptions**, not bad data

**Deliverables:**
- Order-level reconciliation table
- Validation checks for ongoing monitoring
- Fully reproducible analysis notebook

**Tech:** Python, Pandas, SQL-style aggregation logic, data validation, business metrics  
📁 Repo: `revenue-kpi-reconciliation`

---

### 🔹 **Bank Loan Risk Analysis**  
Analyzed **1.2M+ Lending Club loans** to understand borrower default risk.

- Cleaned and transformed a large, messy dataset with missing values and heavy class imbalance
- Built **logistic regression models** on imbalanced vs balanced data
- Improved recall on defaulted loans from **~5% to ~67%** using downsampling
- Focused reporting on **business trade-offs**, not just model accuracy

**Tech:** Python, Pandas, scikit-learn, AUC/ROC, F1, confusion matrices  
📁 Repo: `bank-loan-risk-analysis`

---

### 🔹 **Sonar Object Detection (Applied ML)**  
Research project completed during Seabed.AI placement.

Included here to demonstrate experience with:
- complex data pipelines
- model evaluation
- production constraints under noisy conditions

Primary focus of my portfolio is **analytics and decision support**, not research modeling.

---

## Skills Snapshot

### Data & Analytics Engineering
- SQL (MySQL, T-SQL)
- Python (Pandas, NumPy)
- ETL pipelines, data validation, reconciliation logic
- Databricks, basic Spark

### Analytics & ML
- Classification, risk modeling, operational analytics
- scikit-learn, LightGBM, PyTorch (applied)
- Model evaluation: ROC/AUC, PR curves, F1

### Visualization & Reporting
- Power BI (DAX, Power Query)
- Tableau
- Excel (advanced)

### Tools & Workflow
- Git, Jupyter, VS Code
- AWS basics (S3, Glue, Redshift)
- Reproducible notebooks and documentation

---

## What I’m Focused On Now

- Production-grade analytics pipelines
- Metric governance and data quality monitoring
- Cloud-based analytics workflows
- Translating technical results into **clear business narratives**

---

## Let’s Connect

- **GitHub:** https://github.com/Kablan-ASBN  
- **LinkedIn:** https://www.linkedin.com/in/gomis-kablan/  
- **Email:** gomis.k.assebian@gmail.com
