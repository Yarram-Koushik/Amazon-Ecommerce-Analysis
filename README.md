# 📦 Amazon E-Commerce — SQL & Power BI Business Analysis

<p align="center">

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-CC2927?style=for-the-badge&logo=databricks&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data%20Analytics-blue?style=for-the-badge)
![Business Analysis](https://img.shields.io/badge/Business%20Analysis-orange?style=for-the-badge)

</p>

---

# 📌 Project Overview

This project presents an end-to-end **SQL Data Analytics & Business Intelligence** solution for an **Amazon E-Commerce** platform.

The objective is to analyze transaction data spanning over **113,000 customers** to uncover critical business insights regarding sales growth trajectories, customer lifetime value, seasonal purchase cycles, product category expansion, and order fulfillment performance.

The entire technical workflow combines **MySQL 8.0** for production-grade query optimization, window functions, and multi-metric composite scoring, paired with an interactive **Microsoft Power BI** dashboard, an executive slide deck, and a detailed documentation report for leadership decision-making.

---

# 🎯 Business Problem

E-commerce leadership requires data-driven intelligence to maximize customer retention, smooth out seasonal sales fluctuations, allocate warehouse resources efficiently, and reward high-value shopper segments.

The key business questions addressed include:

- **Who are the most valuable customers** when normalizing across Total Spend, Order Frequency, and Average Order Value (AOV)?
- **What is the Month-over-Month (MoM) revenue trend**, and during which months do recurring seasonal slumps happen?
- **How do product categories perform over smoothed quarterly windows** (rolling 3-month average revenue)?
- **Which customer segments generate disproportionate revenue** (> 30% above the company benchmark)?
- **Which product categories achieved the highest Year-over-Year (YoY) sales expansion** from 2019 to 2020?
- **How can automated customer loyalty discounts and repurchase cadence intervals** be modeled and audited safely in an enterprise database?

A comprehensive SQL-based analysis and BI dashboard were developed to answer these questions with concrete, data-backed recommendations.

---

# 🛠 Tools & Skills Used

- **MySQL 8.0** & Relational Database Design
- **Microsoft Power BI Desktop** (Interactive Dashboards, KPI Visuals, DAX, Drill-Downs)
- **Common Table Expressions (CTEs)** & Multi-Stage Query Pipelines
- **Window Functions** (`PERCENT_RANK`, `LAG`, `AVG() OVER (ROWS BETWEEN 2 PRECEDING AND CURRENT ROW)`, `COUNT() OVER`)
- **Composite Value Scoring** (Normalized Multi-Metric Weighting: 50% Revenue, 30% Frequency, 20% AOV)
- **Time-Series Analysis** (Month-over-Month % Growth & Year-over-Year Comparative Growth)
- **Rolling Moving Averages** (3-Month Smoothing for Category Run-Rates)
- **Conditional Pivoting** (`SUM(CASE WHEN ...)` Aggregation without costly self-joins)
- **Safe DML Operations** (`UPDATE ... JOIN` avoiding MySQL Error 1093)
- **Customer Segmentation & Outlier Identification** (Threshold comparisons via `CROSS JOIN`)
- **Cohort Analysis & Cadence Modeling** (`DATEDIFF` order interval analysis)
- **Executive Business Presentation** (MS PowerPoint & Word documentation)

---

# 📂 Repository Structure

```text
Amazon-Ecommerce-Analysis
│
├── Dashboard
│   └── KoushikYarram_Amazon_Ecommerce_Analysis.pbix
├── Documentation
│   └── KoushikYarram_Amazon_Ecommerce_Answers.docx
├── Presentation
│   └── KoushikYarram_Amazon_Ecommerce_Presentation.pptx
├── SQL
│   └── KoushikYarram_Amazon_Ecommerce_Queries.sql
├── README.md
└── .gitignore
```

---

# 📈 Key Performance Indicators (KPIs)

- **Total Gross Merchandise Value (GMV)** & Revenue Velocity
- **Month-over-Month (MoM) Revenue Growth Rate (%)**
- **Category-wise Rolling 3-Month Moving Average Revenue**
- **Customer Composite Value Score** (0–100 Scale using `PERCENT_RANK()`)
- **Company-Wide Benchmark Spend ($949.02)** vs. **High-Value Spender Threshold ($1,233.73)**
- **Customer Spend Concentration** (Top 18.6% of customers driving 56.8% of GMV)
- **Year-over-Year (YoY) Category Sales Growth & Absolute Incremental Revenue**
- **Order Frequency & Average Order Value (AOV)**
- **Fulfillment Lead Times & Delivery Performance**

---

# 📌 Key Insights

✅ **High-Ticket Basket Drivers:** The top-ranked composite score customers generated up to **$8,180.00** in total revenue, heavily driven by premium electronics and professional photography bundles.

✅ **Normalized Composite Scoring:** Using `PERCENT_RANK()` solved scale bias between dollar volumes and transaction counts, creating an equitable 0–100 ranking framework across 113,000 customers.

✅ **Cyclical Seasonality Identified:** Historical analysis revealed consistent revenue troughs in **September (-15.71%)** and **June (-9.17%)**, caused by post-summer spending dips and school transition periods.

✅ **Rolling Demand Smoothing:** Rolling 3-month moving averages removed single-month promotional spikes, demonstrating consistent baseline quarterly run-rates of **$420K–$485K/month** in Electronics.

✅ **Pareto Spend Concentration (80/20 Rule):** Exactly **21,023 customers (18.6% of total customer base)** generated revenue > 30% above the benchmark ($1,233.73+), capturing **56.8% of total revenue** with individual premiums up to +761.9%.

✅ **Tech Sector Expansion (2019 vs 2020):** **Phones & Tablets** drove the highest dollar increase (**+$2.52M / +41.77%**), while **Electronics** recorded the fastest growth percentage (**+$2.40M / +47.29%**), contributing over **+$4.92M in combined incremental GMV**.

---

# 💼 Business Recommendations

- **Launch "Prime Elite" VIP Tier:** Auto-enroll top composite customers into an exclusive tier featuring complimentary priority shipping, dedicated account support, and extended hardware warranties.
- **Counter-Seasonal Promotional Calendar:** Schedule targeted campaigns (**"Mid-Year Flash Sales" in June** and **"Prime Fall Deals" in early September**) to bridge predictable demand troughs.
- **Target High-Value Cohorts:** Prioritize the top 18.6% spenders with early Prime Day access, customized product bundles, and aggressive trade-in incentives.
- **Supply Chain & Shelf Space Prioritization:** Reallocate warehouse inventory capacity and 1-day Prime fulfillment corridors toward fast-accelerating categories (Phones & Tablets, Electronics).
- **Phased Loyalty Milestones:** Replace single high-threshold promotions with stepped loyalty tiers (**5% at 3 orders, 10% at 5 orders, 15% at 10 orders**) to drive repeat purchases earlier in the customer lifecycle.
- **Predictive Replenishment Automation:** Leverage repurchase intervals to power automated reorder reminders and Subscribe & Save recommendations for consumable goods.

---

# 📁 Project Deliverables

| Deliverable | File | Description |
| :--- | :--- | :--- |
| **SQL Analysis Script** | [`SQL/KoushikYarram_Amazon_Ecommerce_Queries.sql`](./SQL/KoushikYarram_Amazon_Ecommerce_Queries.sql) | Production-ready MySQL 8.0 analytical scripts covering all advanced SQL tasks with CTEs and window functions. |
| **Power BI Dashboard** | [`Dashboard/KoushikYarram_Amazon_Ecommerce_Analysis.pbix`](./Dashboard/KoushikYarram_Amazon_Ecommerce_Analysis.pbix) | Interactive multi-page Power BI dashboard featuring sales KPIs, category breakdown, customer segmentation, and fulfillment analytics. |
| **Executive Presentation** | [`Presentation/KoushikYarram_Amazon_Ecommerce_Presentation.pptx`](./Presentation/KoushikYarram_Amazon_Ecommerce_Presentation.pptx) | Executive-ready presentation summarizing findings, business visualizations, and strategic roadmaps. |
| **Analytical Documentation** | [`Documentation/KoushikYarram_Amazon_Ecommerce_Answers.docx`](./Documentation/KoushikYarram_Amazon_Ecommerce_Answers.docx) | Comprehensive analytical report detailing answers, business implications, and technical logic for all questions. |

---

# 📊 Analysis Categories

### Objective Questions & SQL Tasks
- **Question 14:** Top 5 Most Valuable Customers (Composite Score using `PERCENT_RANK()` across Revenue, Frequency, and AOV)
- **Question 15:** Month-over-Month (MoM) Revenue Growth Rate using `LAG()` window function
- **Question 16:** Rolling 3-Month Average Revenue by Product Category using window frame clauses
- **Question 17:** Safe 15% Loyalty Discount Update using `UPDATE ... JOIN` (MySQL Error 1093 prevention)
- **Question 18:** Average Days Between Consecutive Orders for Repeat Customers (`DATEDIFF` & `LAG`)
- **Question 19:** High-Value Customer Identification (> 30% Above Benchmark Spend via `CROSS JOIN`)
- **Question 20:** Top 3 Product Categories by Year-over-Year (YoY) Sales Expansion (Conditional `CASE WHEN` aggregation)

### Business Intelligence & Reporting
- Sales performance tracking across categories, sub-categories, and regions
- Order fulfillment analysis: delivery delays, courier efficiency, and shipping mode evaluation
- Customer purchase behavior and segmentation dashboards
- Interactive visual filters, slicers, and executive KPI summary cards

---

# 📚 What I Learned

- Normalizing multi-dimensional metrics using `PERCENT_RANK()` to eliminate scale bias between currency and order counts
- Using `LAG()` and chronological partitioning for time-series Month-over-Month (MoM) growth calculations
- Implementing moving windows (`ROWS BETWEEN 2 PRECEDING AND CURRENT ROW`) to eliminate promotional volatility
- Writing non-locking, efficient `UPDATE ... JOIN` queries without subquery table collision
- Calculating enterprise benchmark metrics dynamically with `CROSS JOIN`
- Pivoting multi-year data side-by-side using conditional aggregation (`SUM(CASE WHEN ... THEN ... END)`)
- Building interactive Power BI reports with cohesive color themes, KPI indicators, and cross-filtering
- Translating complex data outputs into strategic, executive-level business decisions

---

# 🚀 Future Improvements

- **Predictive Churn & LTV Modeling:** Build Python machine learning models (XGBoost / Random Forest) to forecast customer churn probability.
- **Automated ETL Pipeline:** Implement an Apache Airflow or Python pipeline to automate MySQL data loading and validation.
- **Market Basket Analysis:** Apply the Apriori algorithm to uncover product affinities and improve cross-selling recommendation engines.
- **Power BI Service Deployment:** Publish the dashboard to the Power BI Cloud with automated scheduled gateway refreshes.

---

# 👨💻 Author

**Koushik Yarram**

Data Science Learning Journey (Phase 1 – Data Analytics)

- **GitHub:** [@Yarram-Koushik](https://github.com/Yarram-Koushik)

---

⭐ If you found this project useful, consider giving it a star!
