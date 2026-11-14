# E-Commerce-User-Conversion-Funnel-Analysis

# 📊 E-Commerce User Conversion & Funnel Optimization Analysis

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Visuals-3F4F75?logo=plotly&logoColor=white)
![Status](https://img.shields.io/badge/Status-Portfolio%20Ready-success)

## 📌 Project Overview
An end-to-end **Product & Conversion Rate Optimization (CRO) Analytics** project evaluating **17,175 user journey interactions** across five sequential e-commerce stages (`Homepage` $\rightarrow$ `Product Page` $\rightarrow$ `Cart` $\rightarrow$ `Checkout` $\rightarrow$ `Purchase`). 

Beyond tracking descriptive funnel drop-offs, this project isolates high-friction mid-funnel bottlenecks and models a **"What-If" Revenue Sensitivity Simulator** to quantify the exact financial upside of targeted UX interventions.

---

## 🎯 Business Problem & Objectives
While top-of-funnel acquisition drives **10,000 homepage sessions**, overall end-to-end conversion stands at just **2.25% (225 completed purchases)**—a **97.75% cumulative drop-off**. The primary objectives of this analysis are:
1. **Quantify Stage-Level Progression:** Measure *Overall Conversion (%)*, *Step-to-Step Retention (%)*, and *Immediate Drop-Off (%)* across all 5 funnel stages.
2. **Isolate Revenue Bottlenecks:** Pinpoint where user intent collapses most sharply.
3. **Prescribe Actionable CRO Interventions:** Map data-backed UX/product fixes to each friction point.
4. **Simulate Financial Lift:** Model incremental order and revenue growth without increasing Customer Acquisition Cost (CAC).

---

## 📊 Key Funnel Metrics & Diagnostic Insights

| Funnel Stage | Active Users | Overall Conversion (%) | Step Retention (%) | Step Drop-Off (%) | Share of Total Events (%) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Homepage** | 10,000 | 100.00% | 100.00% | 0.00% | 58.22% |
| **Product Page** | 5,000 | 50.00% | 50.00% | **50.00%** | 29.11% |
| **Cart** | 1,500 | 15.00% | 30.00% | **70.00%** | 8.73% |
| **Checkout** | 450 | 4.50% | 30.00% | **70.00%** | 2.62% |
| **Purchase** | 225 | **2.25%** | 50.00% | **50.00%** | 1.31% |

### 🔍 Core Findings
* **Top-of-Funnel Traffic Skew:** `Homepage` and `Product Page` interactions account for **87.33%** of all recorded events, while transactional stages (`Cart`, `Checkout`, `Purchase`) represent only **12.66%**.
* **Severe Mid-Funnel Bottlenecks:** The steepest attrition occurs at **`Product Page → Cart` (-70.0%)** and **`Cart → Checkout` (-70.0%)**, indicating friction around pricing clarity, shipping costs, and mandatory account registration.
* **Late-Stage Checkout Abandonment:** **50.0%** of users who initiate checkout (225 out of 450) drop off before payment completion.

---

## 💡 Prioritized CRO Recommendations

| Bottleneck Transition | Drop-Off | Root Cause Hypothesis | Recommended Product / UX Action | Expected Impact |
| :--- | :---: | :--- | :--- | :---: |
| **Product Page $\rightarrow$ Cart** | -70.0% | Weak value reinforcement or unclear delivery timelines. | Add verified social proof badges, sticky *Add to Cart* CTAs, and upfront delivery date estimates. | **+10% to +15%** Cart Additions |
| **Cart $\rightarrow$ Checkout** | -70.0% | Surprise delivery fees or forced login walls. | Introduce **Guest Checkout**, upfront shipping calculators, and one-click UPI/Wallet express checkout. | **+12% to +18%** Checkout Starts |
| **Checkout $\rightarrow$ Purchase** | -50.0% | Multi-page form fatigue or payment failures. | Consolidate into a single-page checkout and trigger automated **30-min Abandoned Cart WhatsApp/Email nudges**. | **+5% to +8%** Final Purchases |

---

## 🚀 "What-If" Revenue & Conversion Sensitivity Simulator
Assuming an **Average Order Value (AOV) of ₹1,500**, improving `Cart → Checkout` retention by just **+10 percentage points** (from `30%` to `40%`, moving 600 users into checkout instead of 450) yields:
* **Completed Purchases:** Increases from `225` $\rightarrow$ **`300 orders` (+33.3% growth)**
* **Overall Funnel Conversion:** Lifts from `2.25%` $\rightarrow$ **`3.00%`**
* **Incremental Revenue:** **+₹1,12,500** per 10,000 homepage visitors (with **₹0 additional ad spend**)

---

## 🛠️ Tech Stack & Visualizations
* **Data Manipulation:** `Python`, `Pandas`, `NumPy`
* **Interactive Visualizations (`Plotly`):**
  * **Horizontal Tapered Funnel (`go.Funnel`):** Displays user volume, cumulative conversion (`% initial`), and step retention (`% previous`).
  * **Proportional Area Funnel (`go.Funnelarea`):** Illustrates stage share across total funnel interactions.
  * **Pattern-Encoded Accessibility Funnel:** Uses geometric hatched fills (`/`, `x`) to visually isolate high-friction bottleneck stages.
  * **Grouped Baseline vs. Optimized Bar Chart:** Compares current funnel performance against the simulated CRO uplift scenario.

---

## 📂 Repository Structure
```text
├── funnel-analysis.ipynb                    # Complete Jupyter Notebook with theory, KPIs, visuals & simulator
├── Funnel_Analysis_Executive_Report.pdf     # Standalone executive summary & recommendation report
├── user_data.csv                            # E-commerce user journey dataset (17,175 records)
└── README.md                                # Project documentation
