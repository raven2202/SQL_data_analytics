# SQL_data_analytics
This repository contains a collection of SQL scripts designed for common business analytics tasks. The queries are structured to provide insights into sales performance, customer behavior, and product trends. These scripts can be adapted to different datasets with similar structures.
Table of Contents
Change Over Time Analysis

Cumulative Analysis

Performance Analysis

Part-to-Whole Analysis

Data Segmentation

Customer Report

Product Report

1. Change Over Time Analysis
File: 1_change_over_time_analysis.sql

Purpose: To track trends, growth, and changes in key metrics over time. This is useful for time-series analysis and identifying seasonality.

Key Functions: YEAR(), MONTH(), DATETRUNC(), FORMAT(), SUM(), COUNT()

2. Cumulative Analysis
File: 2_cumulative_analysis.sql

Purpose: To calculate running totals or moving averages for key metrics. This helps in tracking performance cumulatively and identifying long-term trends.

Key Functions: SUM() OVER(), AVG() OVER()

3. Performance Analysis
File: 3_performance_analysis.sql

Purpose: To measure the performance of products, customers, or regions over time (e.g., Year-over-Year). It's useful for benchmarking and identifying high-performing entities.

Key Functions: LAG(), AVG() OVER(), CASE

4. Part-to-Whole Analysis
File: 4_part_to_whole_analysis.sql

Purpose: To understand the contribution of different segments to the whole. For example, analyzing which product categories contribute the most to overall sales.

Key Functions: SUM() OVER()

5. Data Segmentation
File: 5_data_segmentation.sql

Purpose: To group data into meaningful categories for targeted insights. This includes customer segmentation, product categorization, or regional analysis.

Key Functions: CASE, GROUP BY

6. Customer Report
File: 6_report_customers.sql

Purpose: A comprehensive report that consolidates key customer metrics and behaviors. It segments customers and calculates important KPIs like recency, average order value, and average monthly spend.

Structure: This script creates a view named gold.report_customers.

7. Product Report
File: 7_report_products.sql

Purpose: A detailed report that consolidates key product metrics. It segments products based on revenue and calculates KPIs like recency, average order revenue, and average monthly revenue.

Structure: This script creates a view named gold.report_products.

How to Use
Prerequisites: Ensure you have a SQL environment with tables that have a similar structure to gold.fact_sales, gold.dim_customers, and gold.dim_products.

Adapt: Modify the table and column names in the scripts to match your database schema.

Execute: Run the scripts in your preferred SQL client. The analysis scripts will return results directly, while the report scripts will create views that you can query.

Database Schema Assumption
These queries assume a data model with at least the following tables:

gold.fact_sales: Contains transactional data like order_date, sales_amount, quantity, customer_key, product_key.

gold.dim_customers: Contains customer details like customer_key, first_name, last_name, birthdate.

gold.dim_products: Contains product details like product_key, product_name, category, cost.
