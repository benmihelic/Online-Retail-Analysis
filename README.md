# Retail Sales Analysis with SQL and Tableau

This project analyzes an [Online Retail dataset](https://archive.ics.uci.edu/ml/datasets/online+retail) using **PostgreSQL** for data preparation and **Tableau** for visualization.  
The goal is to transform raw transaction data into clear business insights through **KPIs, dashboards, and visual analytics**.

---

## Project Workflow

### 1. Data Source
- Dataset: [Online Retail (UCI Machine Learning Repository)](https://archive.ics.uci.edu/ml/datasets/online+retail)  
- Raw format: CSV containing invoice-level transactions.  

- Original Dataset viewed in LibreOffice
  
![screenshot of raw CSV](Screenshots/.png)

---

### 2. Data Preparation in PostgreSQL
I used **psql** shell to load the dataset into a PostgreSQL database, then created summary tables/CSVs for Tableau.

- **Monthly Revenue**
- **Average Order Size by Month**
- **Top 10 Countries by Revenue**
- **Top 10 Products by Revenue**

SQL example:

```sql
SELECT DATE_TRUNC('month', invoicedate) AS month,
       ROUND(SUM(quantity * unitprice), 2) AS revenue
FROM retail
GROUP BY month
ORDER BY month;

3. Exported Data
The queries above were exported into 4 CSV files for Tableau:

monthly_revenue.csv

average_order_size.csv

top_countries_revenue.csv

top_products_revenue.csv


4. Tableau Visualizations
The CSVs were imported into Tableau to build interactive charts:

Monthly Revenue (Line Chart)

Top 10 Products by Revenue (Bar Chart)

Top 10 Countries by Revenue (Bar Chart, excluding UK in KPI calc)

Average Order Value (Line Chart)


5. KPI Dashboard
Created a dashboard with 6 key KPIs across the top:

Total Revenue

Average Order Size

Average Monthly Revenue

Total Orders

Average Country Revenue (excluding UK)

Average Product Revenue

Reference lines were added to highlight averages.


🚀 Key Insights
Revenue is highly concentrated in the UK, so global averages were recalculated excluding it.

Seasonal patterns appear in monthly revenue trends.

A small number of products drive the majority of sales.

🛠️ Tech Stack
PostgreSQL (psql shell) — data cleaning and SQL transformations

Tableau Public — dashboards and KPI visualizations

GitHub — documentation and version control

