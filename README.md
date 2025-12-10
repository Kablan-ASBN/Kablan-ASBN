# Hi, I’m Kablan Assebian (Legal Name: Gomis Kablan Assebian)

**Data Scientist & Data Analyst** | SQL • Python • Machine Learning • Power BI  
MSc Data Science (Distinction, University of Greenwich)

I design **ETL pipelines, machine learning models, and analytics dashboards** that turn messy real-world data into decision-ready insights for **risk, finance, and operations teams**.

I started in **neuroscience**, working with noisy behavioral and biological data, then pivoted into **data science and engineering** — so I’m used to complex systems, imperfect data, and tight constraints.

---

## Most Recent Role

**Machine Learning Engineer (Professional Placement) — Seabed.AI (London, UK)**  
AI startup building sonar and computer vision solutions for offshore operations.

- Developed a **domain-adaptation model (DCCAN)** that boosted object detection performance in noisy sonar environments by ~25% vs the internal baseline.
- Engineered **SQL/Python ETL pipelines with automated QC**, cutting manual data prep time by roughly 50%.
- Designed **Power BI dashboards** for executives and engineers, giving real-time visibility into pipeline health, detection accuracy, and data coverage.
- Partnered with engineers on **AWS + Databricks** workflows, aligning research pipelines with production deployment patterns.

---

## Selected Projects

### 🔹 **[Bank Loan Risk Analysis](https://github.com/Kablan-ASBN/bank-loan-risk-analysis)**:
Analyzed **1.2M+ Lending Club loans**; balanced logistic regression improved recall from **5% → 67%**; delivered actionable borrower-risk insights.  

- Cleaned and transformed a large, messy loan dataset (missing data, categorical encoding, heavy class imbalance).
- Built **logistic regression models** and compared performance on **imbalanced vs balanced** data.
- Improved recall on defaulted loans from **~5% to ~67%** using downsampling, while maintaining similar AUC (~0.71).
- Produced **stakeholder-style reporting** focused on business impact, trade-offs, and model limitations.

**Tech:** Python, Pandas, scikit-learn, class imbalance handling, AUC/ROC, F1, confusion matrices.

---

### 🔹 **[Sonar Object Detection](https://github.com/Kablan-ASBN/sonar-object-detection)** — **(Research done during Seabed.AI Placement)**:
Built a **domain-adaptation deep learning model** (PyTorch + SQL) for 3,400+ sonar images, improving detection under domain shift.

- Converted **3,400+ YOLO-annotated sonar images** into Pascal VOC format, handled class remapping, and created stratified train/val/test splits.
- Fine-tuned **Faster R-CNN (ResNet-50 FPN, COCO-pretrained)** on sonar data with multiple preprocessing variants (raw, denoised, CLAHE).
- Implemented **adversarial domain adaptation** (DANN + a novel DCCAN hybrid) to improve robustness under domain shift between training and deployment data.
- Evaluated using **COCO metrics (AP@0.5, mAP@[.5:.95]) and FROC curves**, showing DCCAN recovered more true targets at higher FP rates and delivered the best precision–recall balance.

**Tech:** PyTorch, TorchVision detection API, adversarial domain adaptation, COCO metrics, FROC, NVIDIA A100 (Colab).

---

## Skills Snapshot

**Data Engineering**
- SQL (MySQL, T-SQL), Python, ETL Pipelines  
- Databricks, basic Spark, data cleaning & transformation

**ML & Analytics**
- Classification, risk modeling, credit/fraud analytics  
- scikit-learn, PyTorch, LightGBM  
- Model evaluation (ROC/AUC, F1, PR curves), class imbalance

**Visualization & BI**
- Power BI (DAX, Power Query)  
- Tableau, Excel (advanced)

**Workflow & Tools**
- Git, Jupyter, VS Code  
- AWS basics (S3, Glue, Redshift)  
- Experiment tracking & reproducible notebooks

---

## Currently Exploring

- Cloud-native data pipelines with **AWS & Databricks**  
- **Orchestration & automation** with Airflow / Prefect  
- **Model interpretability & fairness** (SHAP, LIME, bias considerations)

---

## Let’s Connect
[LinkedIn](https://www.linkedin.com/in/gomis-kablan/) · [GitHub](https://github.com/Kablan-ASBN) · **gomis.k.assebian@gmail.com**
