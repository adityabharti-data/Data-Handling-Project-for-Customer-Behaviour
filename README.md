# Data-Handling-Project-for-Customer-Behaviour
Retail Sales Data Pipeline: Cleaning raw consumer data in Python, migrating to MySQL for advanced relational analysis, and building an interactive executive dashboard in Power BI.
# 📊 End-to-End Customer Behavior Analysis & Data Pipeline

An end-to-end data analytics project mapping out a complete data pipeline: from **Raw Data Ingestion & Engineering (Python)**, through **Relational Database Querying & Aggregation (MySQL)**, to **Interactive Business Intelligence Reporting (Power BI)**.

---

## 🛠️ Tech Stack & Architecture

| Phase | Tool | Key Techniques & Libraries |
| :--- | :--- | :--- |
| **Data Engineering** | 🐍 Python (Jupyter Notebook) | Pandas, NumPy, Data Profiling, Type Casting, Missing Value Handling |
| **Database Layer** | 🛢️ MySQL Workbench | Relational Schemas, Window Functions, Complex Grouping, CTEs |
| **Business Intelligence**| 📊 Power BI | Data Modeling, DAX (Data Analysis Expressions), Dynamic Visualizations |

```text
  [Raw CSV Data] ──> [Jupyter Notebook (Cleaning)] ──> [MySQL Database] ──> [Power BI Dashboard]

Project Overview & Objectives
In modern retail, understanding how demographics, purchasing channels, and promotional strategies interact is vital for maximizing profitability. This project analyzes retail transaction records to answer critical business questions:

1. Demographic Insights: How do gender and age demographics influence purchasing volume and product category preferences?

2. Promotion Performance: Do discount incentives drive sustainable long-term revenue, or do they unsustainably erode net profit margins?

3. Logistics Optimization: Which shipping methods yield the highest average purchase sizes, and where are the fulfillment bottlenecks?

Data Pipeline Execution Breakdown

Phase 1: Data Preprocessing & Cleaning (Python)
Using Customer_Behaviour.ipynb, the raw transaction dataset was profiled and cleaned to guarantee structural integrity for database migration.

Data Auditing: Inspected shapes, null distributions, and evaluated descriptive statistics to identify anomalies.

Feature Cleaning: Stripped anomalies, standardized categorical text boundaries (e.g., ensuring binary 'Yes'/'No' flags were uniform), and formatted continuous monetary variables.

Exporting: Delivered a normalized dataset structured cleanly for immediate standard relational mapping.

Phase 2: Relational Database Analytics (MySQL)
The processed data was loaded into a MySQL instance (addydb1.mytable). Advanced analytical queries were implemented in customer_behavior_Sql.sql to surface core business matrices:

Cohort Revenue Analysis: Aggregated revenue pools utilizing advanced grouping criteria across specific demographic segments.

Sub-query Filtering: Extracted high-value customer records by dynamically filtering users whose net transaction totals exceeded macro population averages.

Common Table Expressions (CTEs) & Window Functions: Implemented dense partitioning algorithms (ROW_NUMBER() OVER (PARTITION BY ... ORDER BY ...)) to dynamically rank and isolate the Top 3 performing products across every distinct category vertical

Phase 3: Interactive Dashboard Development (Power BI)
Connected Power BI directly to the prepared dataset to create an executive-level reporting layout (customer_behavior_pbi.pbix):

Robust Data Model: Designed clean dimensional hierarchies to optimize cross-filtering speeds.

DAX Calculations: Written dedicated measures for key performance indicators (KPIs) tracking average transaction values, purchase velocity, and discount activation rates.

Dynamic UX: Crafted an interactive canvas optimized for drill-down exploration across Category, Shipping Priority, and Demographics.

Core Business Insights Derived
Discount Mechanics: While applied discounts significantly drive transaction frequency, a sub-query evaluation highlights that premium non-discounted tiers continue to account for the highest net average order value (AOV).

Category Dominance: By leveraging SQL Window Functions to isolate top products per category, specific core inventory pillars were identified that drive over 40% of standard category revenue, signaling items prime for targeted up-selling.

Logistics Value: Customers utilizing Express shipping options exhibit a higher average checkout basket size compared to standard shipping profiles, suggesting a strong strategic opportunity to bundle express shipping incentives with high-threshold minimum spending limits.
