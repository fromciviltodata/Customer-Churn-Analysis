# 📡 Customer Churn Analysis — Telecom
### SQL • Power BI • Exploratory Data Analysis

> **27% churn rate. $1.3M annual revenue at risk. 1 in 3 customers leaving.**  
> This project uncovers *why* — and what the business should do about it.

![Dashboard Preview](https://github.com/EktaMistri/Telecom-Customer-Churn-Analysis/blob/main/overview.png)

---

## 📌 Project Overview

This end-to-end data analysis project examines customer churn behaviour across **6,418 telecom subscribers** to identify the root causes of a 27% churn rate — nearly double the industry benchmark of 15–20%.

The analysis moves beyond surface-level reporting to uncover **counterintuitive findings**, quantify revenue impact, and deliver four prioritised, data-driven retention recommendations.

**Tools Used:** PostgreSQL • Microsoft Power BI • DAX • Microsoft Excel  
**Skills Demonstrated:** Data Cleaning • EDA • Statistical Analysis • DAX Measures • Dashboard Design • Business Storytelling

---

## ❓ Problem Statement

A telecom company is losing customers at an alarming rate. The business knows *how many* customers are churning but not *why* — or *which* customers are most at risk.

**Three core questions this analysis answers:**
1. Who is churning — and what do they have in common?
2. What are the strongest predictors of churn in this dataset?
3. What should the business do about it — and what is the revenue impact of acting?

---

## 📁 Repository Structure

```
customer-churn-analysis/
│
├── data/
│   ├── raw/                        # Original dataset (CSV)
│   └── cleaned/                    # Cleaned dataset after preprocessing
│
├── sql/
│   ├── 01_data_cleaning.sql        # Deduplication, null handling, type fixes
│   ├── 02_exploratory_analysis.sql # EDA queries — churn by segment
│   └── 03_churn_metrics.sql        # Churn rate, ARPU, revenue at risk
│
├── powerbi/
│   └── churn_analysis.pbix         # Full 3-page Power BI dashboard
│
├── screenshots/
│   ├── page1_overview.png          # Churn Overview page
│   ├── page2_drivers.png           # Churn Drivers page
│   └── page3_recommendations.png  # Insights & Recommendations page
│
└── README.md
```

---

## 🧹 Data Cleaning & Preparation

Before any analysis, the raw dataset was cleaned and validated in **PostgreSQL**:

- ✅ Removed duplicate customer records
- ✅ Standardised date formats and corrected data types
- ✅ Handled NULL values in monthly charge and contract columns
- ✅ Validated churn flag consistency across all rows
- ✅ Normalised categorical values (e.g. inconsistent contract type labels)
- ✅ Created derived columns: tenure buckets, age groups, revenue at risk flag

**Dataset:** 6,418 customer records • 21 columns • 1 year of subscription data

---

## 📊 Dashboard Structure

The Power BI dashboard is structured across **3 pages**, each serving a different analytical purpose:

### Page 1 — Churn Overview *(Who is churning?)*
High-level KPIs and demographic breakdown to establish the scale and profile of churn.

| KPI | Value |
|---|---|
| Total Customers | 6,418 |
| Churn Rate | **27.0%** ⚠ |
| Churned Customers | 1,732 |
| Retained Customers | 4,686 |
| Est. Monthly Revenue at Risk | **$112K** |

**Visuals:** KPI cards • Age group combo chart • Tenure trend • Gender split • State churn ranking

---

### Page 2 — Churn Drivers *(Why are they churning?)*
Drills into the behavioural and service-level factors that predict churn.

**Key visuals:** Contract type churn rate • Top churn reasons • Service-level churn table • Payment method analysis • Internet type breakdown

 ![view](https://github.com/EktaMistri/Telecom-Customer-Churn-Analysis/blob/main/drivers.png)
---

### Page 3 — Insights & Recommendations *(What should the business do?)*
Translates every finding into a prioritised business action with estimated revenue impact.

**Est. monthly recovery potential: $40K–$67K** from partial implementation of four recommendations.

---

## 🔍 Key Findings

### Finding 1 — Contract Type Is the Strongest Churn Predictor
Month-to-month customers churn at **46.5%** compared to just **2.7%** for two-year contract holders — a **17x difference**. Contract type alone is the most actionable lever in the entire dataset.

---

### Finding 2 — The Counterintuitive Internet Service Signal ⚡
> *Conventional logic says customers with more services are more embedded and less likely to leave. The data says the opposite.*

Customers **with internet service churn at 93.7%** — the highest rate of any variable in the dataset. Fiber Optic customers account for **1,136 churned customers**, making it the 3rd largest churn driver overall.

This signals a **pricing-versus-value mismatch** in the premium service tier — customers paying more are leaving more.

---

### Finding 3 — Long-Tenure Customers Are Leaving
Churn spikes in the **24+ month tenure group** (2,100 customers). Customers who have stayed long enough to evaluate alternatives are churning at a disproportionate rate.

**Insight:** No loyalty reward = no reason to stay. The business is not converting tenure into commitment.

---

### Finding 4 — Competitor Churn Is an Active Signal
**761 customers left specifically for a competitor** — these made an active, evaluated decision to leave. They are the most important segment to understand and the highest-value win-back target.

---

### Finding 5 — Gender Is NOT a Useful Predictor
Female churn: 27.4% | Male churn: 26.2% — a **1.2% difference** that is statistically negligible. Retention resources should not be allocated by gender.

---

## 💡 Recommendations

| # | Finding | Action | Est. Monthly Impact | Priority |
|---|---|---|---|---|
| 01 | Month-to-month 46.5% churn | Contract upgrade incentive program | $15K–$25K | 🔴 High |
| 02 | Fiber Optic premium churn | Exit survey + Fiber loyalty tier | $12K–$20K | 🔴 High |
| 03 | 50+ age group churn spike | Senior support pathway + proactive outreach | $8K–$12K | 🟡 High |
| 04 | 761 left for competitor | Win-back campaign + pricing audit | $5K–$10K | 🟡 Medium |
| | | **Total Est. Monthly Recovery** | **$40K–$67K** | |

---
## 💭 What I Would Do Next

Given access to additional data, the next analytical steps would be:

- **Predictive churn model** — use logistic regression or a decision tree with contract type, tenure, and internet service as input features to score customers *before* they churn
- **CLV segmentation** — identify which churned customers had the highest lifetime value to prioritise win-back budget
- **Exit survey analysis** — text analysis of competitor churn reasons to quantify the pricing gap
- **Cohort analysis** — track churn rate by acquisition month to identify whether certain customer cohorts are structurally more at risk

---

## 🧠 Skills Demonstrated

| Category | Details |
|---|---|
| **Data Cleaning** | Deduplication, null handling, type standardisation, derived columns |
| **Exploratory Analysis** | Segmentation, distribution analysis, anomaly detection |
| **Statistical Thinking** | Benchmark comparison, rate analysis, correlation vs causation awareness |
| **DAX & Power BI** | Custom measures, conditional formatting, multi-page dashboard, slicers |
| **Business Communication** | Findings translated into revenue impact and prioritised recommendations |
| **Attention to Detail** | Data quality validation before analysis; limitations flagged in findings |

---

## 📬 Connect

**LinkedIn:** [www.linkedin.com/in/ektamistri]  



*This project is part of my data analytics portfolio. Built independently as a demonstration of end-to-end analytical thinking — from raw data to business recommendations.*
