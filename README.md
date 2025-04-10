# Ecommerce-sales-analysis-excel
### Project Overview

This project explores synthetic online retail data that simulates realistic e-commerce transactions. The objective is to conduct comprehensive data analysis—spanning data cleaning, transformation, exploration, and visualization—to generate insights into customer segmentation, product performance, and purchasing behavior.
### Data Source

+ Dataset Name: Online Retail & E-Commerce Dataset
+	Source: [Kaggle Dataset by ertugrulesol](https://www.kaggle.com/datasets/ertugrulesol/online-retail-data/data)
+	Rows: 1,000 transactions
+	Generated With: Python Faker Library
+	Data Type: Fully synthetic, privacy-safe
+	Note: This dataset contains no real customer or business data. It was generated to reflect realistic distributions and behaviors observed in e-commerce, making it ideal for analysis and modeling practice.
### Data Structure

+ customer_id - Unique identifier for each customer (values range from 10,000 to 99,999)
+ order_date - Date of purchase, randomly selected within the past year
+ product_id - Unique product ID (values range from 100 to 999)
+ category_id - Identifier for the product's category (possible values: 10, 20, 30, 40, 50)
+ category_name - Name of the product category (e.g., Electronics, Fashion, Home & Living, etc.)
+ product_name - Product name corresponding to the category
+ quantity - Number of units purchased (ranges from 1 to 5)
+ price - Unit price of the product (£10.00 – £500.00, rounded to two decimal places)
+ payment_method - Method of payment (Credit Card, Bank Transfer, Cash on Delivery)
+ city - Customer's city, randomly generated using the Faker library
+ review_score	Integer/Null	Customer’s rating of the product (1 to 5 stars, or missing with 20% chance)
+ gender	 - Customer’s gender (M/F, or missing with 10% probability)
+ age - Customer’s age (ranges from 18 to 75 years old)
### Data Cleaning & Preparation

+ Standardized order_date format to DD-MM-YYYY
+ Converted price field to numeric and added currency formatting
+ Handled missing values:
  + review_score: marked nulls as "No Review"
  + gender: marked nulls as “Not Provided”
+ Created a new revenue field
  + revenue = price × quantity
### Key Calculations & Metrics

+ Monthly revenue trends over time
+ Total Revenue per category and by gender
+ Total Revenue and number of sales by customer review score
+ Top 10 products ranked by:
  + Total revenue
  + Average review score
  + Total number of reviews
### Assumptions

+ Missing values for reviews and gender were treated as “No Review” and “Not Provided,” respectively, rather than data errors
+ All transactions are assumed to be successful (no refunds or returns modeled)
+ Age values reflect adult customers (18+)
### Insights & Summary

+ Monthly Revenue Trends
  + The highest total revenue was observed in August and December, whereas March 2024 and March 2025 marked the lowest-performing months.
  + Home & Living experienced a steady increase in revenue until January 2025, followed by a sharp decline in March. This requires further investigation, potentially considering:
    + Shifts in consumer preferences
    + Product quality issues
    + Competitive market changes

| Category    | Highest Month | Lowest Month |
| -------- | ------- | ------- |
| Books & Stationery | August 2024 |	October 2024 |
| Electronics |	December 2024 |	March 2024 |
| Fashion |	August 2024	| March 2024 |
|Home & Living |	January 2025 |	March 2025 |
| Sports & Outdoors |	June 2024 |	March 2024|

+ Gender-Based Product Preferences
  + Fashion products are predominantly purchased by female customers
  + Sports & Outdoors products are more popular among male customers
  + Recommendation: Use this segmentation to tailor marketing strategies by gender
+ Impact of Reviews on Sales
  + The top 10 products by revenue all had average ratings above 4.0 stars
  + Products with 4-5 star ratings consistently generated the highest revenue and order volume
  + Action Items:
    + Improve review scores by enhancing customer satisfaction and product quality
    + Encourage more customer feedback, as many transactions currently lack reviews
    + More reviews = richer data for smarter, data-driven decisions
### Sheet Guide

+ Online Retail Data - Original cleaned dataset
+ Analysis - Pivot tables
+ Dashboard - Visual summary of key KPIs and insights
+ Documentation - This write-up: project overview, process, and results
