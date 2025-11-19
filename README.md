# City Super Store Retail Financial Performance Customer Profitability


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

Fact Orders

Dim Returns

Dim Managers

Ensured optimized query folding for efficient model refresh.

3. DAX Measures

Created key measures including:

Avg_Discount_% 

AVG Profit 

AVG_SaIes 

CLTV 

CustomerCount 

Orders Count 

Orders PerCustomer 

Profit_ %

Profit YOY

Return Rate % 

Returned Orders 

Sales YOY 

Total Profit 

Total_Quantity 

Total Retum Profit Loss 

Total Retum Sales Loss 

Total Retums 

Total_SaIes 

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

Dim Returns → Fact Orders (1:* )

Dim Managers → Fact Orders (1:* )

Optimizations:

Removed unused columns

Enabled star schema for faster DAX evaluation

Removed unused columns

Enabled star schema for faster DAX evaluation


📘 Project Story — Retail Financial Performance & Customer Profitability Dashboard (Power BI)

City Super Store, a multi-regional retail chain, needed a unified analytical view to understand financial performance, profitability, and customer value across its entire business. Fragmented reports made it difficult for leadership to identify where revenue was being generated, where profits were leaking, and which customers had the highest long-term value.

This Power BI dashboard consolidates sales, profit, discount, and customer-level metrics into an interactive decision-support system. It gives managers and executives the ability to monitor business performance at both strategic and operational levels.

🔍 Customer Profitability & CLTV Insights

The Customer Analysis view highlights how customer groups contribute differently to long-term value and profitability:

Corporate customers lead average CLTV (₹335.32) with consistent repeat purchases.

Home Office follows (₹328.3), demonstrating stable profitability.

Consumer segment has the lowest CLTV (₹269.12) despite being the largest group — signalling lower retention profitability.

Sales distribution shows 49% revenue coming from Corporate, proving their financial importance.

A Sales vs Profit scatterplot identifies high-spend low-profit customers, helping the business refine discount or service strategies for these profiles.

📍 Regional Financial Performance Story

Through the Region-Wise Profitability view, the dashboard reveals:

West drives the highest revenue (~₹577K)

East delivers strong sales (~₹550K) with stable profits

Central region shows opportunity for growth with better discount control

Technology category contributes the most (~₹660K), followed by Furniture and Office Supplies

A monthly Sales vs Discount trend helps managers detect seasonal opportunities and discount inefficiencies.

⚠ Return-Churn Insights — Revenue & Profit Leakage

Returns significantly impact profit margins. The Return/Churn page highlights the issue clearly:

Return Rate: 6.01%

Total Returns: 243

Profit Loss: ₹22.76K | Sales Loss: ₹151.28K

Consumer segment accounts for 52% of returns

West region has the highest return volume (159)

Office Supplies category leads in returns (194 orders)

This enables category managers to inspect product quality gaps, over-promotions, or mismatched customer expectations.

📈 Business Impact

This unified dashboard helps City Super Store:

Improve profit margins across regions

Identify high-value customers & personalize retention strategies

Optimize discounting decisions using real-time financial impact

Reduce return-induced revenue leakage

Strengthen operational insights across categories & segments

The solution transforms raw data into practical insights that support executive decisions and improve business performance.
