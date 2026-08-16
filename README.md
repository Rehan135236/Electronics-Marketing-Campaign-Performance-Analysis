# 📊 Electronics Marketing Campaign Performance Analysis

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811.svg?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Pandas](https://img.shields.io/badge/Pandas-2.2%2B-150458.svg?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)]()

> An end-to-end data analytics project evaluating **100,000 digital advertising campaign records** for an electronics retailer across the **GCC region** (UAE, Saudi Arabia, Qatar, Kuwait, Oman). Combines Python data wrangling & EDA with an interactive 3-page Power BI dashboard to drive strategic budget optimization and revenue growth.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Problem](#-business-problem)
- [Key Executive KPIs](#-key-executive-kpis)
- [Exploratory Data Analysis & Insights](#-exploratory-data-analysis--insights)
  - [Platform Performance](#1-platform-performance)
  - [Campaign Type Performance](#2-campaign-type-performance)
  - [Geographic & Market Analysis](#3-geographic--market-analysis)
  - [Monthly Seasonality & Trends](#4-monthly-seasonality--trends)
  - [Top Performing Campaigns](#5-top-performing-campaigns)
- [Power BI Dashboard Architecture](#-power-bi-dashboard-architecture)
- [Data Pipeline & Validation](#-data-pipeline--validation)
- [Strategic Business Recommendations](#-strategic-business-recommendations)
- [Repository Structure](#-repository-structure)
- [How to Run the Project](#-how-to-run-the-project)
- [Author & Contact](#-author--contact)

---

## 📌 Project Overview

This project provides an end-to-end analysis of multi-channel advertising performance for a leading electronics brand operating in the GCC region. By leveraging **100,000 daily campaign performance records** spanning the full calendar year of 2025, this analysis evaluates campaign efficacy across advertising platforms, campaign formats, target geographies, and customer segments.

```
       ┌────────────────────────┐
       │   100,000 Raw Records  │
       └───────────┬────────────┘
                   │
                   ▼
       ┌────────────────────────┐
       │  Python Data Pipeline  │ ──► Data Cleaning & Validation (0 Nulls, 0 Duplicates)
       └───────────┬────────────┘
                   │
                   ▼
       ┌────────────────────────┐
       │ EDA & KPI Engineering  │ ──► ROAS, CPA, CTR, CPM, CVR Calculations
       └───────────┬────────────┘
                   │
                   ▼
       ┌────────────────────────┐
       │  Power BI Dashboard    │ ──► 3 Interactive Report Pages
       └────────────────────────┘
```

---

## 🎯 Business Problem

The marketing executive team needed actionable insights to resolve key operational questions:

1. **Platform Efficiency**: Which ad platforms deliver the highest Return on Ad Spend (ROAS) versus volume?
2. **Format Selection**: How do Shopping, Search, Display, Video, and Lead Gen campaigns compare in unit economics?
3. **Geographic Allocation**: Which GCC country-platform combinations yield the strongest revenue returns?
4. **Seasonal Timing**: When do performance spikes occur, and how should promotional budgets be allocated across months?
5. **Budget Optimization**: Where can marketing spend be reallocated from low-margin channels to high-margin growth drivers?

---

## 📈 Key Executive KPIs

Across **$17.71M** in total advertising spend, the campaign portfolio generated **$470.16M** in total revenue, yielding an overall **ROAS of 26.55**.

| Metric | Result | Description / Notes |
|:---|:---:|:---|
| 💵 **Total Spend** | **$17.71M** | Total ad investment across all 5 platforms |
| 💰 **Total Revenue** | **$470.16M** | Gross sales generated from campaign activity |
| 🎯 **Total Conversions** | **5.11M** | Purchases + Email Signups captured |
| 🛒 **Total Purchases** | **1.59M** | E-commerce checkout orders completed |
| 🚀 **Overall ROAS** | **26.55** | Gross Revenue generated per $1 ad spend |
| 🖱️ **Overall CTR** | **2.06%** | Total Clicks / Total Impressions |
| 📈 **Overall Conversion Rate** | **12.16%** | Total Conversions / Total Clicks |
| 💳 **Average CPA** | **$3.47** | Cost Per Acquisition across all conversions |

---

## 🔎 Exploratory Data Analysis & Insights

### 1. Platform Performance

Five major ad networks were evaluated on ROAS, CPA, and CTR metrics:

| Platform | Spend ($M) | Revenue ($M) | ROAS | CPA ($) | CTR (%) | Key Strategic Role |
|:---|:---:|:---:|:---:|:---:|:---:|:---|
| **Google Ads** | **$5.31** | **$240.48** | **45.29** | $4.52 | **3.77%** | **Revenue & Profitability Powerhouse** |
| **Meta Ads** | $5.30 | $123.96 | **23.39** | $2.77 | 1.94% | High-Volume Conversion Driver |
| **TikTok Ads** | $3.19 | $71.04 | **22.27** | **$2.49** | 1.67% | Lowest CPA / Youth Audience Growth |
| **YouTube Ads** | $2.14 | $34.47 | **16.11** | $6.25 | 1.49% | Brand Awareness & Reach |
| **LinkedIn Ads** | $1.77 | $18.89 | **10.67** | $5.08 | 2.04% | High-AOV Enterprise B2B Leads |

---

### 2. Campaign Type Performance

| Campaign Type | ROAS | CPA ($) | Conversion Rate (%) | Primary Strength |
|:---|:---:|:---:|:---:|:---|
| **Shopping** | **55.63** | $3.70 | 8.63% | Immediate high-intent product sales |
| **Search** | **55.40** | $3.74 | 8.66% | High-intent capture on active queries |
| **Display** | **23.48** | $8.91 | 8.39% | Retargeting & mid-funnel consideration |
| **Video** | **14.92** | $6.25 | 7.01% | Massive impressions & brand awareness |
| **Lead Generation** | **14.86** | **$1.37** | **26.57%** | Highest signup conversion rate at lowest CPA |

---

### 3. Geographic & Market Analysis

Performance was evaluated across all 5 GCC member nations:

```
     ┌─────────────────────────────────────────────────────────────┐
     │           TOP GOOGLE ADS ROAS BY GCC COUNTRY                │
     ├─────────────────────────────────────────────────────────────┤
     │  Saudi Arabia (KSA)  ████████████████████████████  48.19    │
     │  United Arab Emirates ███████████████████████████  47.36    │
     │  Oman               ███████████████████████████  47.23    │
     │  Kuwait             █████████████████████████    41.29    │
     │  Qatar              █████████████████████        36.96    │
     └─────────────────────────────────────────────────────────────┘
```

- **Saudi Arabia & UAE**: Represent the largest volume markets, accounting for ~65% of regional revenue.
- **Oman**: Displays exceptional ad efficiency (47.23 ROAS on Google Ads), representing an under-allocated growth opportunity.

---

### 4. Monthly Seasonality & Trends

Ad performance exhibits strong seasonal peaks aligned with regional shopping festivals and quarter-end campaigns:

| Month | Spend ($M) | Revenue ($M) | Conversions | Monthly ROAS | MoM Revenue Growth |
|:---|:---:|:---:|:---:|:---:|:---:|
| **January** | $1.30 | $33.49 | 368,120 | 25.76 | Base |
| **February** | $1.16 | $29.75 | 329,410 | 25.65 | -11.2% |
| **March** *(Ramadan Prep)* | $1.68 | $45.78 | 496,230 | 27.25 | **+53.9%** 🚀 |
| **April** *(Eid Sales)* | $1.87 | $49.39 | 537,110 | 26.41 | +7.9% |
| **May** | $1.42 | $37.08 | 405,180 | 26.11 | -24.9% |
| **June** | $1.28 | $33.98 | 369,840 | 26.55 | -8.4% |
| **July** *(Summer Slump)* | $1.15 | $29.11 | 318,450 | 25.31 | -14.3% |
| **August** *(Back to School)* | $1.63 | $42.79 | 468,900 | 26.25 | **+47.0%** 🚀 |
| **September** | $1.70 | $45.49 | 495,300 | 26.76 | +6.3% |
| **October** | $1.52 | $40.48 | 441,200 | 26.63 | -11.0% |
| **November** *(White Friday)* | **$2.17** | **$59.72** | **640,525** | **27.53** | **+47.5%** 🔥 |
| **December** *(Year-End)* | $1.83 | $49.52 | 536,250 | 27.06 | -17.1% |

---

### 5. Top Performing Campaigns

Individual campaign-level performance shows significant high-end outliers:

```
🏆 #1 Top Revenue Campaign
├── Campaign ID: CMP-2025-0179
├── Platform: TikTok Ads
├── Campaign Type: Display
├── Country: United Arab Emirates
└── Gross Revenue: $1.92M

🥈 #2 Top Revenue Campaign
├── Campaign ID: CMP-2025-0021
├── Platform: Google Ads
├── Campaign Type: Shopping
├── Country: United Arab Emirates
└── Gross Revenue: $1.26M
```

---

## 📊 Power BI Dashboard Architecture

The companion Power BI report (`Dashboards/Electronics_Marketing_Dashboard.pbix`) consists of **3 interactive analytical pages**:

```
 ┌────────────────────────────────────────────────────────────────────────┐
 │                      POWER BI DASHBOARD PAGES                          │
 ├────────────────────────────────────────────────────────────────────────┤
 │                                                                        │
 │  PAGE 1: EXECUTIVE OVERVIEW                                            │
 │  ├── KPI Summary Cards (Spend, Revenue, Conversions, Purchases, ROAS)  │
 │  ├── Monthly Revenue vs. Spend Dual-Axis Combination Chart            │
 │  ├── Platform Revenue Contribution Donut Chart                         │
 │  └── High-Level Regional Heatmap Matrix                                │
 │                                                                        │
 │  PAGE 2: PLATFORM & CAMPAIGN ANALYSIS                                  │
 │  ├── Platform ROAS vs. CPA Scatter Plot Matrix                         │
 │  ├── Campaign Type Conversion Rate & Revenue Bar Charts                │
 │  ├── Audience Type & Device Breakdown Slicers                          │
 │  └── ROAS Performance Decomposition Tree                               │
 │                                                                        │
 │  PAGE 3: DEEP-DIVE PERFORMANCE ANALYSIS                                │
 │  ├── Country x Platform Matrix Heatmap                                 │
 │  ├── MoM Growth Trendline & Seasonality Decomposition                  │
 │  ├── Outliers & Campaign-Level Top 20 Data Table                       │
 │  └── Cross-filtering Slicers (Date, Country, Manager, Status)         │
 └────────────────────────────────────────────────────────────────────────┘
```

---

## 🧹 Data Pipeline & Validation

### Preprocessing & Integrity Checks

```python
import pandas as pd
import numpy as np

# 1. Load Dataset
df = pd.read_csv("data/Marketing_Campaign_Data.csv")

# 2. Logical Validation Checks (Must return 0 anomalies)
assert (df['Reach'] > df['Impressions']).sum() == 0, "Reach > Impressions anomaly detected"
assert (df['Clicks'] > df['Reach']).sum() == 0, "Clicks > Reach anomaly detected"
assert (df['Purchases'] > df['Add_to_Cart']).sum() == 0, "Purchases > Add_to_Cart anomaly detected"

# 3. Missing Value Imputation
non_critical_cols = ['City', 'Agency_Team', 'Operating_System', 'Gender', 'Email_Signups', 'Bounce_Rate', 'Session_Duration_Minutes']
df[non_critical_cols] = df[non_critical_cols].fillna("Unknown")

# 4. Feature Engineering
df['CTR'] = df['Clicks'] / df['Impressions']
df['CPC'] = df['Spend_USD'] / df['Clicks']
df['CPM'] = (df['Spend_USD'] / df['Impressions']) * 1000
df['CPA'] = np.where(df['Conversions'] > 0, df['Spend_USD'] / df['Conversions'], 0)
df['ROAS'] = np.where(df['Spend_USD'] > 0, df['Revenue_USD'] / df['Spend_USD'], 0)
df['Conversion_Rate'] = np.where(df['Clicks'] > 0, df['Conversions'] / df['Clicks'], 0)
```

---

## 💡 Strategic Business Recommendations

> [!IMPORTANT]
> **1. Scale Google Ads Investment (+15–20% Budget Increase)**
> Google Ads delivers an unmatched **45.29 ROAS**. Shift budget from lower-margin awareness channels into **Google Shopping & Search** campaigns, particularly in Saudi Arabia and the UAE.

> [!TIP]
> **2. Optimize Lead Generation Downstream Monetization**
> Lead Gen campaigns achieve a phenomenal **26.57% conversion rate at $1.37 CPA**, but lag in immediate ROAS (14.86). Implement automated email nurture workflows to convert signups into high-ticket electronics buyers.

> [!NOTE]
> **3. Maximize High-Season Promotional Blitzing**
> Double promotional budget allocations during **November (White Friday)**, **March/April (Ramadan/Eid)**, and **August (Back to School)** where consumer purchasing intent and ROAS peak.

> [!WARNING]
> **4. Restructure LinkedIn & YouTube Ad Allocations**
> LinkedIn ($5.08 CPA, 10.67 ROAS) and YouTube ($6.25 CPA, 16.11 ROAS) require campaign-level trimming. Audit low-performing video creatives and focus LinkedIn purely on high-margin B2B bulk enterprise deals.

> [!TIP]
> **5. Utilize TikTok & Meta for Low-Cost Upper-Funnel Growth**
> TikTok Ads provides the lowest CPA (**$2.49**). Maintain Meta and TikTok as primary engines for new customer acquisition and audience retargeting.

> [!IMPORTANT]
> **6. Implement Country-Platform Matrix Bidding**
> Avoid uniform platform budgets. Allocate capital based on market-specific efficiency (e.g., prioritize Google Ads in Saudi Arabia [48.19 ROAS] and UAE [47.36 ROAS]).

---

## 📂 Repository Structure

```text
Electronics-Marketing-Campaign-Performance-Analysis/
│
├── 📁 data/
│   └── Marketing_Campaign_Data.csv       # Cleaned synthetic dataset (100k rows)
│
├── 📁 notebooks/
│   └── exploratory_data_analysis.ipynb   # Jupyter Notebook for EDA & Data Processing
│
├── 📁 scripts/
│   ├── generate_marketing_data.py        # Synthetic dataset generator script
│   └── data_cleaning_and_kpis.py         # KPI calculation & validation script
│
├── 📁 dashboards/
│   └── Electronics_Marketing_Dashboard.pbix # Interactive 3-page Power BI Dashboard
│
├── 📁 assets/
│   ├── executive_overview_preview.png    # Power BI Dashboard Page 1 Screenshot
│   ├── platform_analysis_preview.png     # Power BI Dashboard Page 2 Screenshot
│   └── performance_deepdive_preview.png  # Power BI Dashboard Page 3 Screenshot
│
├── .gitignore                            # Git ignore configuration
├── LICENSE                               # MIT License
└── README.md                             # Project Documentation
```

---

## 🛠️ How to Run the Project

### Prerequisites

- Python 3.10+ installed
- Power BI Desktop installed (to view `.pbix` report)
- Jupyter Notebook / VS Code

### Installation & Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Rehan135236/Electronics-Marketing-Campaign-Performance-Analysis.git
   cd Electronics-Marketing-Campaign-Performance-Analysis
   ```

2. **Set Up Python Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate        # On Linux/macOS
   # venv\Scripts\activate          # On Windows
   ```

3. **Install Dependencies**:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

4. **Run Analysis Notebook**:
   ```bash
   jupyter notebook notebooks/exploratory_data_analysis.ipynb
   ```

5. **Open Power BI Dashboard**:
   - Double click `dashboards/Electronics_Marketing_Dashboard.pbix` to launch in Power BI Desktop.

---

## 👤 Author & Contact

**Rehan**  
*Data Analyst & Business Intelligence Specialist*

- **GitHub**: [@Rehan135236](https://github.com/Rehan135236)
- **Repository**: [Electronics-Marketing-Campaign-Performance-Analysis](https://github.com/Rehan135236/Electronics-Marketing-Campaign-Performance-Analysis)

---

<div align="center">
  <sub>Built with ❤️ using Python & Power BI for Electronics E-Commerce Analytics.</sub>
</div>
