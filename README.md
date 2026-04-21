# 🧠 DS-AttritionScope-PredictiveWorkforceAnalytics

<div align="center">

### 🏢 Employee Management System (EMS) — End-to-End Data Science Project
> *Predict. Analyze. Retain. — A complete Data Science lifecycle for HR Attrition Intelligence*

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-RandomForest-orange?logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?logo=sqlite&logoColor=white)](https://sqlite.org)
[![SMOTE](https://img.shields.io/badge/Imbalance-SMOTE-red)](https://imbalanced-learn.org)
[![GridSearchCV](https://img.shields.io/badge/Tuning-GridSearchCV-green)](https://scikit-learn.org)
[![Colab](https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com)
[![License](https://img.shields.io/badge/License-MIT-brightgreen)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Complete-success)](https://github.com)

</div>

---

## 📖 What is DS-AttritionScope-PredictiveWorkforceAnalytics?

**DS-AttritionScope-PredictiveWorkforceAnalytics** is a full-stack **Data Science project** built on top of an **Employee Management System (EMS)**. It transforms raw HR data into actionable workforce intelligence by combining:

- 🗄️ **Structured database management** (SQLite)
- 🔍 **Deep Exploratory Data Analysis** (EDA)
- 🤖 **Predictive Machine Learning** (Random Forest + SMOTE + GridSearchCV)
- 📊 **Automated Visual Dashboards** (Matplotlib + Seaborn)
- 📤 **Business-Ready Excel Reports** (openpyxl)

> **Core Goal:** Identify *which employees are at risk of leaving* — and *why* — so HR teams can take proactive retention action.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Why This Project?](#-why-this-project)
- [Tech Stack](#-tech-stack)
- [Data Science Lifecycle](#-data-science-lifecycle)
- [EMS Modules Breakdown](#-ems-modules-breakdown)
- [ML Architecture](#-ml-architecture)
- [Dataset Schema](#-dataset-schema)
- [How to Run](#-how-to-run)
- [Results & Metrics](#-results--metrics)
- [Visual Outputs](#-visual-outputs)
- [Business Insights](#-business-insights)
- [Project Structure](#-project-structure)
- [Author](#-author)

---

## 🎯 Project Overview

| Property | Details |
|---|---|
| **Project Name** | DS-AttritionScope-PredictiveWorkforceAnalytics |
| **Domain** | Human Resources / Workforce Analytics |
| **Problem Type** | Binary Classification (Stay=0 / Leave=1) |
| **ML Model** | Random Forest Classifier |
| **Optimization** | GridSearchCV (Hyperparameter Tuning) |
| **Class Balancing** | SMOTE (Synthetic Minority Over-sampling) |
| **Database** | SQLite (`ems_uploaded.db`) |
| **Platform** | Google Colab |
| **Output** | Excel Report (5 sheets) + PNG Dashboard |
| **Accuracy** | ~78% (Balanced Model) |

---

## ❓ Why This Project?

Employee attrition is one of the **most costly HR challenges** for any organization:

```
💸  Replacing one employee costs 50%–200% of their annual salary
📉  High attrition damages team morale and productivity
🔮  Most companies react AFTER the employee resigns — too late!
```

**DS-AttritionScope** flips this by using **predictive analytics** to flag at-risk employees *before* they leave — giving HR teams time to intervene with targeted retention strategies.

---

## 🛠️ Tech Stack

```
╔══════════════════════════════════════════════════════════════╗
║  LAYER              │  TOOLS                                 ║
╠══════════════════════════════════════════════════════════════╣
║  Language           │  Python 3.10+                          ║
║  Platform           │  Google Colab                          ║
║  Database           │  SQLite (sqlite3)                      ║
║  Data Processing    │  Pandas, NumPy                         ║
║  Machine Learning   │  scikit-learn                          ║
║  Class Balancing    │  imbalanced-learn (SMOTE)              ║
║  Visualization      │  Matplotlib, Seaborn                   ║
║  Reporting          │  openpyxl (Excel), Matplotlib (PNG)    ║
╚══════════════════════════════════════════════════════════════╝
```

---

## 🔄 Data Science Lifecycle

This project implements a **complete 7-stage Data Science workflow:**

```
┌────────────────────────────────────────────────────────────┐
│                                                            │
│   📂 RAW CSV                                               │
│       │                                                    │
│       ▼                                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 1 → Data Ingestion                        │     │
│   │  CSV uploaded → Cleaned → Stored in SQLite DB    │     │
│   └───────────────────┬──────────────────────────────┘     │
│                       ▼                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 2 → EDA (Exploratory Data Analysis)       │     │
│   │  City | Education | Gender | Attrition stats     │     │
│   └───────────────────┬──────────────────────────────┘     │
│                       ▼                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 3 → Preprocessing                         │     │
│   │  Label Encoding + SMOTE (Class Balancing)        │     │
│   └───────────────────┬──────────────────────────────┘     │
│                       ▼                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 4 → Model Training                        │     │
│   │  Random Forest + GridSearchCV Tuning             │     │
│   └───────────────────┬──────────────────────────────┘     │
│                       ▼                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 5 → Evaluation                            │     │
│   │  Accuracy | Precision | Recall | F1-Score        │     │
│   └───────────────────┬──────────────────────────────┘     │
│                       ▼                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 6 → Prediction                            │     │
│   │  Single Employee + Batch CSV Prediction          │     │
│   └───────────────────┬──────────────────────────────┘     │
│                       ▼                                    │
│   ┌──────────────────────────────────────────────────┐     │
│   │  STAGE 7 → Reporting & Export                    │     │
│   │  Excel (5 Sheets) + PNG Dashboard                │     │
│   └──────────────────────────────────────────────────┘     │
│                       │                                    │
│                       ▼                                    │
│           📊 BUSINESS INSIGHTS                             │
└────────────────────────────────────────────────────────────┘
```

---

## 🏗️ EMS Modules Breakdown

| Cell | Module | Purpose | Details |
|:---|:---|:---|:---|
| **1–2** | ⚙️ Environment Setup | Library Installation & Imports | Loads `pandas`, `sklearn`, `sqlite3`, `seaborn`. Configures visual themes & color palette |
| **3–4** | 📂 Data Ingestion | CSV Upload & SQL Integration | Converts raw CSV → SQLite database (`ems_uploaded.db`) for efficient querying |
| **5** | 🗃️ CRUD Operations | Database Management | `add_record()`, `search_employee()`, `filter_employees()`, `update_record()`, `delete_record()` |
| **6–9** | 🔍 EDA & Analytics | Exploratory Analysis | Headcount, education levels, gender diversity across cities with descriptive statistics |
| **10** | ⚠️ Risk Profiling | Attrition Risk Analysis | Identifies high-risk segments — Tier 2 Payment, Pune city, EverBenched employees |
| **11** | 🌲 Base ML Model | Random Forest Classifier | Predicts `LeaveOrNot` with feature importance ranking |
| **GridSearch** | 🎛️ Optimization | Hyperparameter Tuning | `GridSearchCV` — tunes `n_estimators` and `max_depth` |
| **SMOTE** | ⚖️ Class Balancing | Synthetic Over-sampling | Fixes class imbalance to improve minority class (Leavers) detection |
| **12–16** | 📊 Visual Dashboard | Data Visualization | Heatmaps, Pie charts, Boxplots, Bar charts, Correlation matrix |
| **17** | 📁 Custom CSV | Any CSV Analysis | Auto-analyzes any uploaded CSV with instant stats + charts |
| **18–19** | 📤 Export System | Report Generation | Excel (5 sheets) + PNG dashboard auto-download |

---

## 🌲 ML Architecture

### 🔹 A. Random Forest Classifier
```python
RandomForestClassifier(
    n_estimators = [100, 200, 300],    # Tuned via GridSearchCV
    max_depth    = [None, 5, 10, 15],  # Tuned via GridSearchCV
    random_state = 42
)
```
- ✅ Handles non-linear relationships
- ✅ Resistant to overfitting
- ✅ Provides Feature Importance scores
- ✅ Works well with mixed data types

### 🔹 B. GridSearchCV — Hyperparameter Tuning
```python
param_grid = {
    'n_estimators': [100, 200, 300],
    'max_depth':    [None, 5, 10, 15]
}
GridSearchCV(rf_model, param_grid, cv=5, scoring='accuracy')
```

### 🔹 C. SMOTE — Class Balancing
```python
from imblearn.over_sampling import SMOTE
sm = SMOTE(random_state=42)
X_train_sm, y_train_sm = sm.fit_resample(X_train, y_train)
```
- ❌ Without SMOTE → model predicts "Stay" for everyone (biased)
- ✅ With SMOTE → model correctly identifies at-risk Leavers

### 🔹 D. Feature Importance Ranking
```
1st  →  JoiningYear                ████████████████████  (Highest)
2nd  →  Age                        ███████████████
3rd  →  PaymentTier                ████████████
4th  →  ExperienceInCurrentDomain  ████████
5th  →  EverBenched                █████
```

---

## 📋 Dataset Schema

Your CSV must contain these columns:

| Column | Type | Description |
|---|---|---|
| `Education` | String | Degree level (Bachelors / Masters / PHD) |
| `JoiningYear` | Integer | Year the employee joined the company |
| `City` | String | Work location (Bangalore / Pune / New Delhi) |
| `PaymentTier` | Integer | Salary tier (1 = Low, 2 = Mid, 3 = High) |
| `Age` | Integer | Employee age in years |
| `Gender` | String | Male / Female |
| `EverBenched` | String | Ever put on bench? (Yes / No) |
| `ExperienceInCurrentDomain` | Integer | Years of experience in current role |
| `LeaveOrNot` | Integer | 🎯 **Target** → 0 = Stay, 1 = Leave |

---

## 🚀 How to Run

### Step 1 — Open in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com)

### Step 2 — Install Dependencies
```python
# Cell 1 auto-installs everything
!pip install pandas matplotlib seaborn scikit-learn openpyxl imbalanced-learn -q
```

### Step 3 — Run Cells in Order
```
📦 Cells 1–2   →  Setup environment & import libraries
📂 Cells 3–4   →  Upload CSV → Create SQLite DB
🗃️ Cell  5     →  Initialize CRUD functions
🔍 Cells 6–9   →  EDA + Statistical analysis
⚠️ Cell  10    →  Attrition risk profiling
🌲 Cell  11    →  Train ML model (RF + SMOTE + GridSearch)
📊 Cells 12–16 →  Generate all visualizations
📁 Cell  17    →  (Optional) Analyze any custom CSV
📤 Cells 18–19 →  Export Excel report + Dashboard PNG
```

### Step 4 — Single Employee Prediction
```python
# Configure these variables in the prediction cell:
EDUCATION    = "Masters"
JOINING_YEAR = 2017
CITY         = "Pune"
PAYMENT_TIER = 2
AGE          = 30
GENDER       = "Male"
EVER_BENCHED = "Yes"
EXPERIENCE   = 3

# ── Sample Output ─────────────────────────────────
#   🎯 ATTRITION PREDICTION RESULT
#   ──────────────────────────────────────────
#   Prediction  : 🔴 LIKELY TO LEAVE
#   Stay Prob   : 32.4%
#   Leave Prob  : 67.6%
```

### Step 5 — Batch Prediction
Upload a new CSV (without `LeaveOrNot` column) → auto-generates `Attrition_Risk_Predictions.csv` with risk labels for every employee.

---

## 📊 Results & Metrics

```
╔══════════════════════════════════════════════╗
║         MODEL PERFORMANCE SUMMARY           ║
╠══════════════════════════════════════════════╣
║  Base RF Model Accuracy   →  ~75%           ║
║  After GridSearchCV       →  ~76%           ║
║  After SMOTE Balancing    →  ~78%  ✅       ║
╠══════════════════════════════════════════════╣
║  Precision (Leave=1)      →  Optimized      ║
║  Recall    (Leave=1)      →  Optimized      ║
║  F1-Score                 →  Balanced       ║
╚══════════════════════════════════════════════╝
```

### Attrition Risk by Segment

| Segment | Risk % | Alert Level |
|---|---|---|
| PaymentTier = 2 | ~60% | 🔴 Critical |
| City = Pune | ~38%+ | 🔴 High |
| EverBenched = Yes | ~35%+ | 🟡 Medium-High |
| PaymentTier = 1 | ~30% | 🟡 Medium |
| PaymentTier = 3 | ~18% | 🟢 Low |

---

## 📸 Visual Outputs

| Output File | Description |
|---|---|
| `dashboard.png` | Full 6-panel EMS analytics dashboard |
| `chart_attrition.png` | Attrition by City, Education, PaymentTier & Age |
| `chart_city_education.png` | City headcount, Education pie, Gender by City |
| `chart_payment_age.png` | PaymentTier distribution, Age histogram, Experience |
| `Employee_Report.xlsx` | 5-sheet Excel: All Employees, City, Education, Attrition Risk, Gender Summary |

---

## 💡 Business Insights

### 1. 💰 Tier 2 Compensation Crisis
> Payment Tier 2 employees show **~60% attrition rate** — the highest across all tiers. An urgent compensation or benefits review is critical for this group.

### 2. 👶 Early Career Burnout
> **JoiningYear** is the #1 ML predictor. Employees who joined in specific high-growth years may lack career progression — leading to early exits.

### 3. 🏙️ Pune Regional Alert
> Pune consistently shows the **highest city-level attrition risk**. Local management should investigate workplace culture, workload balance, or competitive external offers.

### 4. 🪑 Bench Management Impact
> While `EverBenched` has moderate standalone importance, it becomes a **strong secondary trigger** in the combined high-risk profile (Tier 1 + Benched).

### 5. 📅 Age-Attrition Pattern
> Boxplot analysis reveals younger employees in their **late 20s to early 30s** have a higher propensity to leave — suggesting a need for stronger early-career engagement programs.

---

## 📁 Project Structure

```
DS-AttritionScope-PredictiveWorkforceAnalytics/
│
├── 📓 EMS_AttritionScope.ipynb           ← Main Colab Notebook
├── 📄 README.md                           ← This file
├── 📄 LICENSE                             ← MIT License
│
├── 📂 data/
│   └── employee_data.csv                  ← Input dataset (upload in Colab)
│
├── 📂 outputs/
│   ├── Employee_Report.xlsx               ← 5-sheet Excel stakeholder report
│   ├── Attrition_Risk_Predictions.csv     ← Batch prediction output
│   ├── dashboard.png                      ← Full analytics dashboard
│   ├── chart_attrition.png                ← Attrition breakdown visuals
│   ├── chart_city_education.png           ← City & Education charts
│   └── chart_payment_age.png              ← Payment tier & Age charts
│
└── 📂 models/
    └── rf_model.pkl                       ← Saved trained model (optional export)
```

---

## 🏷️ GitHub Topics / Tags

```
data-science          predictive-analytics    random-forest
smote                 hr-analytics            workforce-analytics
sqlite                eda                     gridsearchcv
python                google-colab            attrition
machine-learning      employee-churn          pandas
classification        imbalanced-learn        openpyxl
employee-management   data-pipeline           binary-classification
```

---

## 👤 Author

**Your Name**
- 🐙 GitHub  : [https://github.com/Dhruv139555]
- 💼 LinkedIn: [https://www.linkedin.com/in/dhruv-sathvara-64461b352/]
- 📧 Email   : dhruvsathawara13@gmailcom

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — free to use, modify, and distribute with attribution.

---

<div align="center">

⭐ **If this project helped you, please give it a Star!** ⭐

*Built with ❤️ using Python, scikit-learn & Google Colab*

</div>
