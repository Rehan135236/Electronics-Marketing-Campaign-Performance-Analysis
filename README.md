# Electronics-Marketing-Campaign-Performance-Analysis
End-to-end marketing analytics project using Python and Power BI to analyze 100K campaign records, evaluate ROAS, conversions, revenue, platform performance, and GCC market trends, and deliver actionable business insights.
# 📊 Electronics Marketing Campaign Performance Analysis

## 📌 Project Overview

This project analyzes **100,000 digital marketing campaign records** for an electronics business operating across the GCC region.

The objective is to evaluate campaign performance across platforms, campaign types, countries, and time periods, identify the strongest and weakest marketing channels, and provide data-driven recommendations for improving advertising efficiency and revenue generation.

The project combines **Python-based data analysis** with an interactive **Power BI dashboard**.

---

## 🎯 Business Problem

The marketing team needs to understand:

- Which advertising platforms generate the best returns?
- Which campaign types perform most effectively?
- Which countries and markets generate the highest revenue?
- How does campaign performance change over time?
- Which channels should receive more or less marketing budget?
- Where are there opportunities to improve conversions and reduce acquisition costs?

---

## 🎯 Project Objectives

The main objectives were to:

1. Clean and validate the marketing dataset.
2. Analyze campaign performance using Python.
3. Calculate important marketing KPIs.
4. Compare advertising platforms and campaign types.
5. Analyze country-level and monthly performance.
6. Identify high-performing campaigns.
7. Build an interactive Power BI dashboard.
8. Generate actionable business recommendations.

---

## 📂 Dataset

The dataset contains **100,000 records and 29 columns**.

### Main dimensions

- Date
- Campaign ID
- Campaign Name
- Platform
- Campaign Type
- Country
- City
- Sales Region
- Manager
- Agency Team
- Campaign Status
- Industry
- Device
- Operating System
- Age Group
- Gender
- Audience Type

### Marketing metrics

- Impressions
- Reach
- Clicks
- Spend
- Conversions
- Revenue
- Add to Cart
- Purchases
- Email Signups
- Video Views
- Bounce Rate
- Session Duration

---

## 🛠️ Tools & Technologies

### Python

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

### Business Intelligence

- Microsoft Power BI
- DAX
- Interactive dashboards
- KPI cards
- Bar charts
- Donut charts
- Time-series analysis

### Version Control

- Git
- GitHub

---

# 🧹 Data Cleaning & Preparation

The dataset was inspected and cleaned before analysis.

### Missing Values

Initially, several columns contained missing values:

- City
- Agency Team
- Operating System
- Gender
- Email Signups
- Bounce Rate
- Session Duration

Missing values were handled during preprocessing.

After cleaning:
Duplicate Records

Duplicate records were checked.

Duplicate records: 0
Data Type Validation

The Date column was converted into a proper datetime format.

Numeric columns were checked to ensure appropriate data types.

Data Quality Checks

Logical validation was performed on important campaign metrics.

Reach > Impressions: 0
Clicks > Impressions: 0
Purchases > Conversions: 0
Purchases > Add_to_Cart: 0
Negative Spend: 0
Negative Revenue: 0
Negative Conversions: 0

The dataset passed the major logical consistency checks.

📐 KPI Calculations

Several marketing performance metrics were created.

CTR
CTR = Clicks / Impressions
CPC
CPC = Spend / Clicks
CPM
CPM = (Spend / Impressions) × 1000
CPA
CPA = Spend / Conversions
ROAS
ROAS = Revenue / Spend
Conversion Rate
Conversion Rate = Conversions / Clicks
Purchase Rate
Purchase Rate = Purchases / Conversions
📊 Executive KPIs
KPI	Result
Total Spend	$17.71M
Total Revenue	$470.16M
Total Conversions	5.11M
Total Purchases	1.59M
Overall ROAS	26.55
Overall CTR	2.06%
Overall Conversion Rate	12.16%

The overall results indicate that the campaigns generated substantially more revenue than advertising spend.

🔎 Exploratory Data Analysis
Platform Performance

The analysis compared five major advertising platforms:

Google Ads
Meta Ads
TikTok Ads
YouTube Ads
LinkedIn Ads
Key Findings

Google Ads generated the highest revenue and strongest overall ROAS.

Meta Ads generated the highest number of conversions.

TikTok Ads delivered strong conversion volume while maintaining relatively low CPC.

YouTube Ads generated lower ROAS compared with Google and Meta.

LinkedIn Ads had the lowest overall ROAS among the major platforms.

📈 Platform Performance
Platform	ROAS	CPA	CTR
Google Ads	45.29	$4.52	3.77%
Meta Ads	23.39	$2.77	1.94%
TikTok Ads	22.27	$2.49	1.67%
YouTube Ads	16.11	$6.25	1.49%
LinkedIn Ads	10.67	$5.08	2.04%
Interpretation

Google Ads was the strongest channel from a revenue-efficiency perspective.

Meta and TikTok were particularly valuable for generating conversions at relatively low acquisition costs.

LinkedIn and YouTube require closer optimization because their acquisition costs were comparatively higher.

📣 Campaign Type Performance

The five campaign types analyzed were:

Shopping
Search
Display
Video
Lead Generation
Key Findings

Shopping and Search campaigns generated the strongest ROAS.

Lead Generation produced the highest conversion rate and lowest CPA.

Display campaigns had relatively high CPA.

Video campaigns generated large volumes of impressions but lower conversion efficiency.

Campaign Type Performance
Campaign Type	ROAS	CPA	Conversion Rate
Shopping	55.63	$3.70	8.63%
Search	55.40	$3.74	8.66%
Display	23.48	$8.91	8.39%
Video	14.92	$6.25	7.01%
Lead Generation	14.86	$1.37	26.57%
Important Insight

Lead Generation campaigns achieved the highest conversion rate and lowest CPA, but their ROAS was considerably lower.

This shows that conversion volume alone should not determine budget allocation. Revenue generation and profitability should also be considered.

🌍 Geographic Analysis

Campaign performance was analyzed across:

Saudi Arabia
United Arab Emirates
Kuwait
Qatar
Oman

Google Ads performed particularly strongly across several GCC markets.

Some of the strongest platform-country combinations included:

Google Ads — Saudi Arabia
Google Ads — United Arab Emirates
Google Ads — Oman
Google Ads — Kuwait
Google Ads — Qatar

This indicates that Google Ads is a strong candidate for further investment across the GCC region.

📅 Monthly Performance

Campaign performance was analyzed throughout 2025.

Strongest Period

November 2025 was the strongest month in terms of revenue, spend, and conversions.

November generated approximately:

Revenue: $59.72M
Spend: $2.17M
Conversions: 640,525
ROAS: 27.53
Seasonal Pattern

Performance showed noticeable fluctuations throughout the year.

Major increases occurred in:

March
April
August
November

November showed the strongest month-over-month growth, with revenue increasing by approximately 59.5%.

🏆 High-Performing Campaigns

The analysis identified campaigns with exceptionally high revenue.

One of the strongest campaigns was:

Campaign ID: CMP-2025-0179
Platform: TikTok Ads
Campaign Type: Display
Country: United Arab Emirates
Revenue: $1.92M

Another major performer was:

Campaign ID: CMP-2025-0021
Platform: Google Ads
Campaign Type: Shopping
Country: United Arab Emirates
Revenue: $1.26M

These campaigns demonstrate that individual campaign performance can vary significantly even within the same platform.

📊 Power BI Dashboard

The final Power BI dashboard contains three pages.

Page 1 — Executive Overview

Provides a high-level view of:

Total Spend
Total Revenue
Total Conversions
Total Purchases
ROAS
Overall campaign performance

The page is designed for management-level decision making.

Page 2 — Platform & Campaign Analysis

This page focuses on:

Platform performance
Campaign type performance
Revenue contribution
ROAS
Conversion performance
Distribution of campaign activity

Interactive visuals allow users to compare marketing channels.

Page 3 — Performance Analysis

The final page provides deeper analysis of:

Monthly performance
Geographic performance
Campaign performance
Marketing efficiency
Revenue and conversion trends

The dashboard allows users to interactively explore different dimensions of the campaign data.

💡 Business Recommendations
1. Increase Investment in Google Ads

Google Ads demonstrated the strongest overall ROAS.

Budget allocation should prioritize high-performing Google Search and Shopping campaigns.

2. Continue Using Meta and TikTok for Conversion Volume

Meta and TikTok generated substantial conversion volumes with relatively low CPA.

These platforms can remain important acquisition channels, particularly for audience expansion.

3. Optimize Lead Generation Campaigns

Lead Generation campaigns achieved:

Conversion Rate: 26.57%
CPA: $1.37

However, their ROAS was:

14.86

The focus should therefore shift from simply generating leads toward improving lead quality and downstream revenue.

4. Review YouTube and LinkedIn Spending

Both platforms showed weaker overall ROAS.

Instead of completely removing these channels, campaign-level performance should be evaluated and low-performing campaigns should be optimized or reduced.

5. Increase Seasonal Budget Allocation

November demonstrated particularly strong performance.

Historical performance suggests that marketing budgets could be increased during high-performing periods while maintaining efficiency targets.

6. Optimize by Platform-Country Combinations

Performance varies significantly by market.

Budget decisions should therefore consider both:

Platform + Country

rather than evaluating platforms independently.

📌 Key Takeaways

The analysis demonstrates several important conclusions:

Google Ads was the strongest revenue and ROAS channel.
Meta Ads generated the highest conversion volume.
TikTok provided strong acquisition efficiency.
Shopping and Search campaigns produced the strongest ROAS.
Lead Generation campaigns achieved the highest conversion rate and lowest CPA.
November was the strongest month of the year.
Platform performance varies significantly across GCC countries.
Campaign-level optimization can identify opportunities that are hidden by overall platform averages.

```text
Total missing values: 0
