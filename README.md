# 🌍 Global Fuel Price Analysis 2020–2026
### Built with Microsoft Power BI | April Data Challenges

---

## 📌 Project Overview

This project analyses global fuel pricing patterns across **84 countries** and **7 regions** 
from **January 2020 to April 2026** — covering one of the most economically turbulent 
periods in modern history. The analysis examines how COVID-19, the Russia-Ukraine war, 
government subsidy policies and tax structures have shaped what citizens around the world 
pay at the pump.

The dashboard was submitted as an entry for the **April Data Challenge** hosted by 
**TS Academy** and represents my first end-to-end Power BI project built on a dataset 
outside my comfort zone — global fuel economics rather than sales or churn data.

---

## ❓ Business Problem

> *"Global fuel prices are one of the most significant economic forces affecting governments, 
> businesses and households worldwide. Between 2020 and 2026 the world has experienced 
> COVID-driven price collapses, post-pandemic surges, geopolitical shocks and subsidy 
> policy changes — all of which have created dramatic differences in what citizens across 
> 84 countries pay at the pump. This analysis examines the global fuel pricing landscape 
> to identify which regions and countries face the highest fuel burden, how government 
> subsidies and tax policies shape consumer prices independent of global oil markets, 
> and how prices have evolved across six years of unprecedented global disruption. 
> The goal is to provide decision-makers with clear insights into the structural drivers 
> of global fuel prices and the countries most exposed to energy cost vulnerability."*

---

## 📊 Dashboard Preview

### Overview Page
![Dashboard Overview](assets/Global%20fuel%20price%20analysis%20dashboard.png)

---

## 🔍 Insight Questions

1. How have global fuel prices trended from 2020 to 2026?
2. Which region has the most expensive fuel and which has the cheapest?
3. How much does subsidy level affect what citizens pay at the pump?
4. Which countries have the most expensive and cheapest petrol globally?
5. Which countries have the most volatile fuel prices over time?
6. What is the impact of tax rate on the final price citizens pay?

---

## 💡 Key Findings

**Finding 1 — Tax Rate is a Stronger Price Driver Than Crude Oil**
Tax rate correlates with petrol price at **0.52** — nearly double the influence of 
Brent Crude at **0.26**. Government policy shapes what citizens pay more than the 
global oil market. A Nigerian and a Norwegian may draw from the same barrel of 
Brent Crude — but the Norwegian pays $4.76/litre while the Nigerian pays $0.21.

**Finding 2 — Subsidies Create a 23x Price Difference**
Countries with Very High subsidies pay an average of just **$0.15/litre**. Countries 
with Low subsidies pay **$3.45/litre** — a 23x gap driven entirely by government 
policy, not market forces.

**Finding 3 — The World Never Returned to Pre-COVID Prices**
Global petrol averaged **$1.48/litre** in 2020 during the COVID demand collapse. 
By 2026 it sits at **$2.65/litre** — a 79.1% increase from the pandemic low. 
Prices have never recovered to pre-2021 levels.

**Finding 4 — Europe is the Most Expensive Region — but Not Because of Oil**
Europe averages **$3.70/litre** driven by tax rates averaging **34.6%**. The Middle 
East averages just **$1.23/litre** despite having the same access to global oil — 
because governments fund heavy subsidies from oil revenues.

**Finding 5 — Hong Kong is the World's Most Expensive Fuel Market**
At **$6.78/litre** Hong Kong leads global petrol prices — a High income, Low subsidy 
nation with one of the world's highest fuel tax rates. Venezuela at **$0.01/litre** 
represents the opposite extreme through extreme government subsidies.

---

## ✅ Recommendations

**Recommendation 1 — Governments in Low-Subsidy Nations Should Review Fuel Tax Structures**
With tax rate being the primary driver of fuel costs (correlation 0.52 vs 0.26 for 
Brent Crude), high-tax nations should evaluate whether current tax levels create 
disproportionate economic burden — especially for lower-income households who 
spend a larger percentage of income on fuel.

**Recommendation 2 — Subsidy-Dependent Nations Need Transition Strategies**
Countries with Very High subsidies (Venezuela, Iran, Libya) keep prices artificially 
low but create unsustainable fiscal burdens. A phased subsidy reduction strategy 
paired with targeted cash transfers would be more economically sustainable than 
indefinite blanket subsidies.

**Recommendation 3 — Businesses Should Use Brent Crude as a Leading Indicator — With Caution**
Given that Brent Crude only explains 26% of retail price variation, businesses using 
crude oil futures to forecast retail fuel costs should factor in regional tax policy 
and subsidy changes as equal or greater variables in their price modelling.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Power BI | Dashboard design and visualisation |
| Power Query | Data cleaning and date column transformation |
| DAX | Dynamic insight text measures and KPI calculations |
| April Data Challenge Dataset | Source data (TS Academy) |

---

## 🔧 Data Cleaning Steps

1. Converted `date` column from Excel serial number format to proper Date type in Power Query
2. Created `year` calculated column from date for yearly trend analysis
3. Verified zero null values across all 11 columns — dataset was clean on import
4. Created Date Table using CALENDAR DAX function and marked as date table
5. Connected Date Table to main data table via date relationship
6. Created calculated columns for regional groupings and income level labels
7. Built subsidy level sort order column to ensure correct chart sequencing
8. Created `petrol_category` calculated column classifying countries as Most Expensive,
   Mid Range or Cheapest for scatter chart legend coloring

---

## 📐 DAX Measures Written

- Avg Global Petrol Price
- Avg Global Diesel Price  
- Avg Global LPG Price
- Avg Brent Crude Price
- Avg Tax Rate
- Most Expensive Country Dynamic Text
- Cheapest Country Dynamic Text
- Regional Avg Petrol Dynamic Text
- Subsidy Impact Dynamic Text
- Tax Correlation Insight Text
- Fuel Trend Insight Text
- Scatter Insight Text (Route Performance)
- YoY Petrol Price Change

---

## 📂 Dataset Information

| Field | Detail |
|---|---|
| Source | TS Academy — April Data Challenge 2025 |
| Records | 27,468 rows |
| Countries | 84 |
| Regions | 7 (Africa, Asia, Europe, Middle East, North America, Oceania, South America) |
| Date Range | January 2020 — April 2026 |
| Key Variables | Petrol price, Diesel price, LPG price, Brent Crude, Tax %, Subsidy level, Income level |

---

## 📊 Dataset Column Dictionary

| Column | Description | Type |
|---|---|---|
| date | Week the price was recorded | Date |
| country | Country name | Text |
| region | Geographic region | Text (7 categories) |
| income_level | World Bank income classification | Text |
| subsidy_level | Government subsidy intensity | Text (4 levels) |
| petrol_usd_liter | Retail petrol price in USD | Number |
| diesel_usd_liter | Retail diesel price in USD | Number |
| lpg_usd_liter | LPG/cooking gas price in USD | Number |
| brent_crude_usd | Global Brent crude benchmark per barrel | Number |
| tax_percentage | Fuel tax rate applied in country | Number |

---

## 🌟 What Made This Project Challenging

This was the first Power BI project I built on a dataset completely outside my 
previous experience. Every prior project had been sales or churn data — revenue, 
profit, customers. This dataset was global fuel economics — tax policy, subsidy 
structures, geopolitical impacts and cross-country income comparisons.

The challenge pushed me to:
- Learn correlation analysis and how to present it visually (scatter chart with trend line)
- Understand how to make a dashboard readable to non-technical audiences
- Apply the unpivot transformation in a new context
- Build dynamic text that updates across 84 countries and 7 regions with every filter
- Research enough domain knowledge to write accurate and insightful callout text

It also required **three brains** — mine, my colleagues and significant research — 
which taught me that knowing when to collaborate is itself an analytical skill.

---

## 👤 About the Analyst

**Fatimoh Ojuolape Olatunji**
Aspiring Data Analyst | Business Administration Graduate (In View)
Obafemi Awolowo University (OAU)
Day 50+ of my public data analytics learning journey

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/fatimoh-olatunji)
[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=flat&logo=twitter)](https://twitter.com/ojuolape124)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-181717?style=flat&logo=github)](https://github.com/ojuolape124)

---

*This project was submitted for the April Data Challenge and represents 
my first Power BI dashboard built on a global economics dataset. Every step of the 
analysis — from understanding fuel economics to building dynamic DAX measures — 
was documented publicly on LinkedIn, TikTok and Instagram.*

*I am still learning. I am still building. And I am nowhere near done.* 🎯
