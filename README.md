# Power-BI---Retail-Financial-Performance-Customer-Profitability


📌 Project Overview

The Retail Financial Performance & Customer Profitability Dashboard provides a 360° analytical view of sales, profit, customer lifetime value (CLTV), discount patterns, and return-churn metrics. It enables leaders to explore performance across regions, segments, categories, products, and customers with full drill-down capability.

This dashboard helps the business identify growth opportunities, margin threats, and customer-level profitability insights.

🧠 Analytical Approach
1. Data Understanding & Cleaning

Imported transactional retail dataset (Sales, Profit, Returns, Categories, Regions, Customers).

Performed data type fixes, null-value handling, and hierarchical grouping.

Verified consistency of sales–discount–profit calculations.

2. Data Modeling

Built a Star Schema with Fact and Dimension tables:

Fact_Sales (Sales, Quantity, Profit, Discount, Order Date)

Dim_Customer (Customer Name, Segment, Region)

Dim_Product (Category, Sub-Category)

Dim_Date (Calendar hierarchy)

Fact_Returns (Returned Orders, Customer ID)

Established relationships using one-to-many links with Date & Customer dimensions.

Ensured optimized query folding for efficient model refresh.

3. DAX Measures

Created key measures including:

Financial Metrics
Total Sales = SUM(Fact_Sales[Sales])
Total Profit = SUM(Fact_Sales[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales])

Customer Profitability Metrics
CLTV = DIVIDE([Total Profit], DISTINCTCOUNT(Dim_Customer[Customer ID]))

Return-Churn Metrics
Return Rate % = DIVIDE([Total Returns], COUNTROWS(Fact_Sales))
Sales Loss = SUM(Fact_Returns[Sales_Loss])
Profit Loss = SUM(Fact_Returns[Profit_Loss])

Monthly Trends
Sales This Month = CALCULATE([Total Sales], DATEADD(Dim_Date[Date], 0, MONTH))


All measures were optimized using variables (VAR), DIVIDE() for safety, and correct filter context handling.

🛠 Tech Stack
Power BI Desktop

Data Modeling (Star schema)

DAX for calculated metrics

Interactive drill-down visuals

Bookmarks and slicers for guided navigation

Power Query

Data cleaning

Transformations

Date table generation

Relationship validation

Visualization Techniques

KPI Cards

Donut & Bar Charts

Scatter Plot

Line Charts

Region-Wise Analysis

Customer Profitability Matrix

🗂 Data Model Summary

Fact Tables: Sales, Returns

Dimension Tables: Customer, Product, Region, Date

Relationships:

Date → Sales (1:* )

Customer → Sales (1:* )

Product → Sales (1:* )

Customer → Returns (1:* )

Optimizations:

Removed unused columns

Enabled star schema for faster DAX evaluation

Removed unused columns

Enabled star schema for faster DAX evaluation
