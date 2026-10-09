# DS5110 Homework 2 — Writeup

## 1. Raw Data Inspection

The original revenue table contains 5 rows and 13 columns. Each row represents one company, while twelve columns store revenue values for different quarters. This violates tidy data principles because the quarter values are stored as column names instead of observations in a separate variable.

The orders and shipments tables have a more appropriate structure, with each row representing an individual order or shipment.

## 2. Reshaping Revenue Data

I used `pd.melt()` to transform the revenue table from wide format to long format. The resulting table contains 60 rows and 3 columns: company, quarter, and revenue.

Each row now represents one company-quarter observation. This structure makes it easier to group, filter, and visualize revenue data across different quarters.

## 3. Join Cardinality

I checked whether `order_id` was unique in both the orders and shipments tables. The results showed that order IDs were unique in the orders table but not in the shipments table.

Therefore, the relationship is one-to-many. After performing a left join, the number of rows increased from 20 to 35 because some orders had multiple shipments.

## 4. Mean Amount Comparison

I compared the mean order amount per customer using the joined table and the original orders table.

The results were different for four customers because some orders appeared multiple times after the join. This creates row multiplication and gives orders with more shipments greater weight in the average.

For example, customer C107 had a mean amount of 106.00 in the joined table, compared with 96.50 in the original orders table, a difference of 9.50.

The original orders table provides the correct mean order amount because each order is counted only once.

## 5. Final Table and Visualization

I created an analysis-ready table by joining the orders table with the tidy revenue table using company and quarter as composite keys.

To avoid duplicating orders, I summarized the shipment data into a `shipment_count` column before joining it with the analysis table.

The final table contains 20 rows and 7 columns. I checked its shape, missing values, duplicate order IDs, and whether all original order IDs were preserved. All validation checks passed.

The raw-data visualization shows company revenue for one quarter. In comparison, the tidy-data visualization shows revenue trends across twelve quarters for multiple companies. This makes it easier to compare changes over time.
