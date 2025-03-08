# Pizza Sales Analysis Project Overview

Welcome to the Pizza Sales Analysis Project! This project leverages SQL to analyze pizza sales data, uncovering actionable insights into customer ordering patterns, revenue drivers, and product performance. The dataset is sourced from **Kaggle** and covers sales records from **January 1, 2015 to December 31, 2015**.

## Table of Contents
- [Objectives](#objectives)
- [Data Description](#data-description)
- [Project Level](#project-level)
- [SQL Concepts Covered](#sql-concepts-covered)
- [Methodology](#methodology)
- [Conclusion](#conclusion)

## Objectives
- **Analyze Sales Data:**  
  Use SQL queries to extract and aggregate key metrics such as total orders, revenue, and popular pizza types.
- **Identify Trends:**  
  Understand customer ordering patterns, peak hours, and daily/weekly trends.
- **Assess Product Performance:**  
  Determine the highest-priced pizza, the most common pizza size, and the top-selling pizza types.
- **Provide Business Insights:**  
  Offer actionable recommendations for optimizing inventory, staffing, and marketing strategies based on data-driven insights.

## Data Description
- **Dataset Composition:**  
  The project uses multiple tables:
  - **Orders:** Contains overall order information.
  - **Order_Details:** Lists individual pizza orders with quantities and prices.
  - **Pizzas:** Provides details about each pizza (type, size, price).
  - **Pizza_Types:** Categorizes pizzas into groups (e.g., vegetarian, non-vegetarian).
- **Data Source & Timeframe:**  
  Data is obtained from **Kaggle** and covers the period from **January 1, 2015 to December 31, 2015**.

## Project Level
**Beginner-Friendly:**  
This project is designed for beginner to intermediate SQL users. It starts with fundamental SQL queries and gradually introduces more advanced analytical techniques.

## SQL Concepts Covered
- **Basic SQL:**  
  SELECT statements, filtering, sorting, and aggregation functions (COUNT, SUM, AVG, MAX, MIN).
- **Intermediate SQL:**  
  GROUP BY, JOIN operations, time-based analysis, and subqueries.
- **Advanced SQL:**  
  Cumulative sums, percentage calculations, and complex queries combining multiple SQL functions.

## Methodology
The analysis is structured into three stages:

### Basic Analysis
- Retrieve the total number of orders.
- Calculate total revenue from pizza sales.
- Identify the highest-priced pizza.
- Determine the most common pizza size.
- List the top 5 most ordered pizza types with their quantities.

### Intermediate Analysis
- Join tables to calculate total quantities per pizza category.
- Analyze the hourly distribution of orders.
- Examine category-wise distribution of pizzas.
- Calculate daily averages of pizza orders.
- Identify the top 3 revenue-driving pizza types.

### Advanced Analysis
- Compute the percentage contribution of each pizza type to the total revenue.
- Analyze cumulative revenue over time.
- Determine the top 3 revenue-generating pizza types by category.

## Conclusion
This project not only demonstrates practical SQL skills but also provides valuable insights to guide business decisions. The analysis can help optimize inventory, staffing, and promotional strategies by identifying peak ordering periods and high-performing products.

