# Retail Sales Analysis with SQL and Tableau

---
## Project Overview

This project analyzes an online retail dataset to uncover revenue trends, customer behavior, and sales performance across products and countries. Using **PostgreSQL** for data preparation and **Tableau** for visualization, I created an interactive dashboard highlighting key performance indicators (KPIs) and business insights.

The goal of this project is to demonstrate my ability to:

- Clean and aggregate raw transactional data using **SQL**  
- Build calculated fields and KPIs for decision-making  
- Design a clear, interactive Tableau dashboard for stakeholders  

## Interactive Dashboard

View the full interactive Tableau dashboard here:  
[Tableau Public – Online Retail Dashboard](https://public.tableau.com/app/profile/ben.mihelic/viz/OnlineRetailAnalysis_17558674772550)


---



## ⚙️ Tools & Technologies

- **Dataset:** [UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)  
- **PostgreSQL (psql shell):** data cleaning, joins, aggregation  
- **SQL:** grouping, filtering, creating CSV extracts  
- **Tableau Public:** visualization and dashboard design  
- **GitHub:** project documentation and portfolio publishing  
## Project Workflow

### 1. Data Source
- Dataset: [Online Retail (UCI Machine Learning Repository)](https://archive.ics.uci.edu/ml/datasets/online+retail)  
- Raw format: CSV containing invoice-level transactions.  

Original Dataset viewed in LibreOffice
  
![screenshot of raw CSV](Screenshots/original_data_libre_office.png)

---

### 2. Data Preparation in PostgreSQL
I used **psql** shell to load the dataset into a PostgreSQL database, then created summary tables/CSVs for Tableau.

I had to reformat the invoicedate column in order to extract just the year and month to use in the analysis.

Original table structure used to upload the csv.

![screenshot of raw CSV](Screenshots/psql_original_table.png)

Snapshot of dataset with added formatted date and yearmonth columns to use in monthly revenue and average order size csv's.

![screenshot of raw CSV](Screenshots/psql_table_with_timestamp_and_yearmonth.png)

Monthly Revenue Query

![screenshot of raw CSV](Screenshots/psql_revenue_by_month.png)

Average Order Size Query
  
![screenshot of raw CSV](Screenshots/psql_average_order_size.png)

Top 10 Countries by Revenue Query
  
![screenshot of raw CSV](Screenshots/psql_country_by_revenue.png)

Top 10 Products by Revenue Query
  
![screenshot of raw CSV](Screenshots/psql_product_by_revenue.png)

### 3. Exported Data
The queries above were exported into 4 CSV files for Tableau using the \copy function inside the psql shell.

Example output:  monthly_revenue.csv viewed in LibreOffice

![screenshot of raw CSV](Screenshots/monthly_revenue.png)

### 4. Tableau Visualizations
The CSVs were imported into Tableau to build interactive charts:

![screenshot of raw CSV](Screenshots/Monthly_Revenue_Graph.png)

![screenshot of raw CSV](Screenshots/Average_Order_Total.png)

![screenshot of raw CSV](Screenshots/Revenue_by_Product_Graph.png)

![screenshot of raw CSV](Screenshots/Countries_by_Revenue_Graph.png)


### 5. Key Performance Indicator (KPI) Dashboard
Created a dashboard with 6 key KPIs across the top:

Total Revenue, Average Order Size, Average Monthly Revenue, Total Orders, Average Country Revenue (excluding UK), Average Product Revenue

Reference lines were added to highlight averages.

Final Dashboard:

![screenshot of raw CSV](Screenshots/Final_Product.png)



🚀 Key Insights
Revenue is highly concentrated in the UK, so global averages were recalculated excluding it.

Seasonal patterns appear in monthly revenue trends.

A small number of products drive the majority of sales.

🛠️ Tech Stack
PostgreSQL (psql shell) — data cleaning and SQL transformations

Tableau Public — dashboards and KPI visualizations

GitHub — documentation and version control

