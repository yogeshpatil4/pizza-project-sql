# Pizza Sales Analysis Project Overview

## Table of Contents
- [Introduction](#introduction)
- [Data Description](#data-description)
- [Project Level](#project-level)
- [SQL Concepts Covered](#sql-concepts-covered)
- [Methodology](#methodology)
  - [Basic Analysis](#basic-analysis)
  - [Intermediate Analysis](#intermediate-analysis)
  - [Advanced Analysis](#advanced-analysis)
- [SQL Queries](#sql-queries)
- [Analysis and Findings](#analysis-and-findings)
- [Conclusion and Recommendations](#conclusion-and-recommendations)
- [Appendices](#appendices)

---

## Introduction
This project analyzes pizza sales data to extract actionable insights and identify trends that can drive business decisions. The primary objective is to understand customer ordering patterns, revenue drivers, and product performance using SQL queries on a structured dataset.

---

## Data Description
- **Dataset Composition:**  
  The project utilizes multiple tables including:
  - **Orders:** Contains overall order information.
  - **Order_Details:** Lists individual pizza orders with quantities and prices.
  - **Pizzas:** Provides details about each pizza, such as type, size, and price.
  - **Pizza_Types:** Categorizes pizzas into various groups (e.g., vegetarian, non-vegetarian).

- **Data Source & Timeframe:**  
  The dataset is sourced from **Kaggle** and covers sales data from **January 1, 2015 to December 31, 2015**.

---

## Project Level
- **Beginner:**  
  This project is designed for beginners to intermediate SQL users. It covers fundamental SQL queries and gradually introduces more advanced concepts, making it an ideal resource for those looking to build their SQL skills.

---

## SQL Concepts Covered
- **Basic Concepts:**  
  - SELECT statements, filtering, and sorting.
  - Aggregation functions such as COUNT, SUM, AVG, MAX, and MIN.
  - Basic JOIN operations to combine data from multiple tables.

- **Intermediate Concepts:**  
  - GROUP BY for data aggregation.
  - Time-based data analysis to identify trends (e.g., hourly/daily patterns).
  - Advanced JOINs and subqueries.

- **Advanced Concepts:**  
  - Calculating cumulative sums.
  - Determining percentage contributions.
  - Complex queries combining multiple SQL functions and operations.

---

## Methodology
The analysis is structured into three levels—Basic, Intermediate, and Advanced—each answering specific business questions using SQL.

### Basic Analysis
- **Total Orders:** Retrieve the total number of orders placed.
- **Revenue Calculation:** Calculate the total revenue generated from pizza sales.
- **Highest-Priced Pizza:** Identify the highest-priced pizza.
- **Popular Size:** Determine the most common pizza size ordered.
- **Top 5 Pizza Types:** List the top five most ordered pizza types along with their quantities.

### Intermediate Analysis
- **Category Quantities:** Join tables to find the total quantity ordered for each pizza category.
- **Hourly Distribution:** Determine the distribution of orders by hour of the day to identify peak times.
- **Category-Wise Distribution:** Analyze how pizzas are distributed across different categories.
- **Daily Averages:** Group orders by date and calculate the average number of pizzas ordered per day.
- **Top 3 Revenue-Driven Pizzas:** Identify the top three most ordered pizza types based on revenue.

### Advanced Analysis
- **Revenue Contribution:** Calculate the percentage contribution of each pizza type to total revenue.
- **Cumulative Revenue:** Analyze how revenue accumulates over time.
- **Category-Specific Top Pizzas:** Determine the top three revenue-generating pizza types for each pizza category.

---

## SQL Queries
Here are some sample SQL queries used in this project:

- **Total Orders:**
  ```sql
  SELECT COUNT(*) AS total_orders
  FROM Orders;
