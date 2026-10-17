# 📉 Telco Customer Churn Analysis Dashboard (Power BI)

An interactive Power BI dashboard that analyses subscriber churn for a telecom company, showing **who is leaving, why, and how much monthly revenue is at risk**.

![Overview](images/overview.png)
![Risk Detail](images/risk-detail.png)

## 🎯 Business Problem
Customer churn directly hurts recurring revenue. This project helps retention teams
identify high-risk customer segments and prioritise where to intervene.

## 📊 Dashboard Pages
**1. Overview**
- KPI cards: Total Customers, Retained Customers, Churn Rate %, Monthly Revenue at Risk
- Churn Rate by Contract Type
- Customer Retention Overview (donut)
- Customers vs. Churned by Tenure Band
- Internet Service split and Churn Rate by Payment Method

**2. Risk Detail**
- Churn distribution across Monthly Charges bins
- High-Risk Segments matrix (Contract × Internet Service × Payment Method)
- Support Add-ons vs. Churn (Tech Support and Online Security)

**Interactive slicers:** Contract, Payment Method, Internet Service, Gender, Tenure Band

## 🧮 Key DAX Measures
`Total Customers` · `Churned Customers` · `Retained Customers` · `Churn Rate %` ·
`Monthly Revenue at Risk` · `TechSupport Churn (Yes/No)` · `OnlineSecurity Churn (Has/No)`

## 🧹 Data Preparation
- Source: Telco customer churn dataset (raw/unclean version)
- Cleaned and transformed in Power Query (handled missing values, fixed data types, standardised categories)
- Created a calculated **Tenure Band** column and **MonthlyCharges bins**

## 🔍 Key Insights
- Overall churn rate is **26.5%** (1,869 of 7,043 customers), putting **Rs.139K/month (30.5% of revenue)** at risk
- **Contract type is the strongest driver:** month-to-month churn is 42.7% vs 11.3% (1-year) and 2.8% (2-year)
- **First-year customers are most fragile:** 0–6 month tenure churns at 52.9% vs 17.1% for 12+ months
- **Fiber optic users churn at 41.9%**, more than double DSL (19.0%)
- **Electronic check users churn at 45.3%**, vs ~15–17% for automatic payment methods
- **Tech Support and Online Security cut churn by about two-thirds** (15% vs 42%)
- **Highest-risk segment:** month-to-month + fiber optic + electronic check, with a **60.4%** churn rate
- Senior citizens (41.7%) and customers without dependents (31.3%) also churn above average; gender has no meaningful impact

## 💡 Recommendations
- Incentivise month-to-month customers to move to annual contracts
- Build a first-12-months retention and onboarding programme
- Promote auto-pay and bundle Tech Support / Online Security
- Investigate fiber pricing and service quality

## 🛠️ Tools Used
Power BI Desktop · Power Query · DAX · Data Modelling · Data Visualization

## ▶️ How to Open
1. Download `Churn_Data_Analysis.pbix`
2. Open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows)
