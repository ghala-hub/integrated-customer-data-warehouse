# Integrated Customer Data Warehouse
Course project for Data Integration and Warehousing at Umm Al-Qura University, built by a team of 3.

## Overview
We integrated three datasets into a star-schema data warehouse to build a complete view of customer profiles and purchases.

## Data Sources
- Amazon Products & Reviews (semi-structured, 1,465 records)
- Shopping Trends (structured, 3,900 records)
- Customer Purchases (structured, 100,000 records)

## Data Cleaning
- Converted price and discount fields from text to numeric values
- Split hierarchical product categories into separate levels
- Handled invalid and missing ratings and rating counts
- Removed age outliers using the IQR method

## Schema Matching and Mapping
Matched seven shared attributes between Shopping Trends and Customer Purchases (e.g., age, gender, purchase amount), and applied SQL mappings, including a CASE expression for discount flags.

## Data Warehouse Design
Star schema with `FACT_PURCHASE` and four dimensions: `DIM_CUSTOMER`, `DIM_PRODUCT`, `DIM_DATE`, `DIM_PAYMENT`.

## ETL
Extract from the three sources, transform with cleaning and mapping rules, and load into the star schema tables.

## Analytical Questions
1. Which product category generated the highest revenue?
2. Which loyalty segment spends the most?
3. Which season has the highest sales and promotion usage?
4. Which region underperforms in revenue and satisfaction?

## Tools
SQL, MySQL Workbench



