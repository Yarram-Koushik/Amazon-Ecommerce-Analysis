# Amazon E-Commerce Business Analysis

**Author:** Koushik Yarram  
**Tools & Technologies:** MySQL 8.0, Microsoft Power BI, Microsoft Excel/PowerPoint

---

## 📌 Project Overview
This project delivers an end-to-end business and data analysis of Amazon e-commerce sales performance, customer purchasing behavior, order fulfillment, and revenue drivers.

The repository contains advanced SQL scripts, interactive Power BI analytical dashboards, an executive presentation deck, and detailed business solutions addressing strategic and operational challenges.

---

## 📂 Repository Contents

| File | Description |
| :--- | :--- |
| [`KoushikYarram_Amazon_Ecommerce_Queries.sql`](./KoushikYarram_Amazon_Ecommerce_Queries.sql) | Production-ready MySQL 8.0 analytical queries using CTEs, window functions (`PERCENT_RANK`, `DENSE_RANK`), and aggregation strategies. |
| [`KoushikYarram_Amazon_Ecommerce_Analysis.pbix`](./KoushikYarram_Amazon_Ecommerce_Analysis.pbix) | Interactive Power BI dashboard covering sales KPIs, customer segmentation, category performance, and fulfillment trends. |
| [`KoushikYarram_Amazon_Ecommerce_Presentation.pptx`](./KoushikYarram_Amazon_Ecommerce_Presentation.pptx) | Executive-ready presentation summarizing key findings, strategic recommendations, and data-driven insights. |
| [`KoushikYarram_Amazon_Ecommerce_Answers.docx`](./KoushikYarram_Amazon_Ecommerce_Answers.docx) | Comprehensive analytical report detailing answers and business implications for each objective question. |

---

## 🔍 Key Analysis Highlights
- **Top Customer Identification:** Normalized multi-factor composite scoring combining Total Revenue, Order Frequency, and Average Order Value (AOV) using `PERCENT_RANK()`.
- **Fulfillment & Delivery Optimization:** Analysis of shipping delays, courier performance, and delivery time vs. customer satisfaction.
- **Product & Category Performance:** Sales volume, gross margins, and return rates across merchandise hierarchies.
- **Strategic Recommendations:** Actionable business initiatives to reduce churn, optimize inventory turnover, and expand high-margin product categories.

---

## 🚀 Getting Started

### 1. Database Setup & SQL Execution
1. Clone or download this repository.
2. Ensure you have **MySQL 8.0+** installed.
3. Open `KoushikYarram_Amazon_Ecommerce_Queries.sql` in MySQL Workbench or your preferred SQL IDE.
4. Execute against your `amazon_ecommerce` database schema.

### 2. Exploring Power BI Dashboard
1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Open `KoushikYarram_Amazon_Ecommerce_Analysis.pbix` to interact with slicers, visual drill-downs, and cross-filtered KPIs.
