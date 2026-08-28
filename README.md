Olist E-Commerce Sales & Customer Analytics

Project Overview

This project analyzes the Olist Brazilian E-Commerce Public Dataset
using MySQL to understand customer behavior, sales performance, product
and seller performance, delivery efficiency, and customer satisfaction.

The project focuses on practical business questions and uses SQL to
transform transactional data into meaningful business insights.

Business Objectives

Analyze customer purchasing and repeat-order behavior

Identify high-revenue products and categories

Evaluate seller sales and order performance

Measure delivery time and late-delivery performance

Analyze customer reviews and satisfaction

Track monthly sales and month-over-month changes

Identify high-value customers

Compare average order value across customer states

Dataset

The project uses the Olist Brazilian E-Commerce Public Dataset.

Main tables used:

customers

orders

order_items

products

sellers

payments

reviews

Database Schema

Main table relationships:

customers.customer_id → orders.customer_id

orders.order_id → order_items.order_id

orders.order_id → payments.order_id

orders.order_id → reviews.order_id

order_items.product_id → products.product_id

order_items.seller_id → sellers.seller_id

A database schema and relationship diagram is included in the
repository.

Analysis Performed

Customer Analysis

Customer distribution by state

Unique customer analysis

Repeat-purchase behavior

Customers with multiple orders

Top customers by total spending

Sales Analysis

Total revenue

Revenue by product category

Top products by revenue

Monthly sales trends

Previous-month sales using LAG()

Month-over-month sales change

Month-over-month growth percentage

Product Analysis

Revenue by product category

Top products by revenue

Average product price by category

Items sold by category

Products with the highest number of orders

Seller Analysis

Seller revenue

Top sellers by sales

Orders handled by sellers

Average sales per order

High-volume sellers

Delivery Analysis

Average delivery time by state

Late-delivery rate by state

Seller delivery performance

Delivery performance by product category

Monthly delivery delays

Review Analysis

Review score by order status

Review score for late vs on-time deliveries

Delivery time vs review score

Review performance by product category

Seller review performance

Advanced Business Analysis

Top 3 products within each category

Repeat vs one-time customers

Revenue contribution by category

Month-over-month sales growth

Customer spending segmentation

Average order value by customer state

Key Business Metrics

Metric                                     Result

Average delivery time                  12.49 days
Late delivery rate                          8.11%
Average review score                   ~4.09 / 5
Highest-revenue category           beleza_saude
Highest-revenue category sales            ~1.26M

SQL Concepts Used

SELECT, WHERE, JOIN and INNER JOIN

GROUP BY and HAVING

ORDER BY and LIMIT

SUM(), AVG(), COUNT()

COUNT(DISTINCT)

CASE WHEN

Conditional aggregation

Subqueries

Common Table Expressions (CTEs)

Multiple CTEs

Window functions

LAG()

ROW_NUMBER()

PARTITION BY

YEAR(), MONTH() and DATEDIFF()

Percentage calculations

Project Structure

Olist-Ecommerce-SQL-Analysis/
│
├── sql/
│   ├── 01_customer_analysis.sql
│   ├── 02_sales_analysis.sql
│   ├── 03_product_analysis.sql
│   ├── 04_seller_analysis.sql
│   ├── 05_delivery_analysis.sql
│   ├── 06_review_analysis.sql
│   └── 07_advanced_analysis.sql
│
├── screenshots/
│
└── README.md

Analysis Approach

Business Question
       ↓
Identify Required Tables
       ↓
Understand Table Relationships
       ↓
JOIN Related Data
       ↓
Aggregate / Transform Data
       ↓
Use CTEs or Window Functions
       ↓
Calculate Business KPI
       ↓
Interpret the Result

Data Considerations

Sales analysis using order_items.price represents item-price
revenue and excludes freight unless explicitly included.

Customer spending analysis uses payment_value.

Delivery analysis uses purchase and delivery timestamps.

Undelivered orders are excluded from analyses requiring a delivery
date.

LAG() compares against the previous available month, so missing
calendar months should be interpreted carefully.

Original Olist product category names are stored in Portuguese.

Key Takeaways

The project analyzes the complete e-commerce journey:

Customer
   ↓
Order
   ↓
Product / Seller
   ↓
Payment
   ↓
Delivery
   ↓
Review

This provides a business-focused view of revenue, customer behavior,
seller performance, delivery efficiency, and customer satisfaction.

Tools

MySQL

SQL

GitHub

Conclusion

This project strengthened practical SQL skills by working with a
multi-table e-commerce dataset and solving business-oriented analytical
problems.

The focus was not only on writing SQL queries, but also on understanding
table relationships, choosing the correct level of aggregation, applying
advanced SQL techniques, and translating query results into business
insights.
