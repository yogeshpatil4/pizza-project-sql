# Pizza Sales Analysis Project Overview

## Table of Contents
- [Introduction](#introduction)
- [Data Description](#data-description)
- [Methodology](#methodology)
  - [Basic Analysis](#basic-analysis)
  - [Intermediate Analysis](#intermediate-analysis)
  - [Advanced Analysis](#advanced-analysis)
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

## Analysis and Findings
- **Sales Trends:**  
  The analysis reveals peak ordering hours and high-demand days, which are critical for planning staffing and inventory.
- **Product Performance:**  
  Insights into the most popular and highest-priced pizzas help in refining the menu and targeting promotions.
- **Revenue Drivers:**  
  Advanced metrics highlight which pizza types contribute most significantly to overall revenue, guiding pricing and marketing strategies.

---

## Conclusion and Recommendations
- **Key Insights:**  
  - A significant percentage of orders occur during specific peak hours.
  - Certain pizza types consistently drive higher revenue.
- **Business Implications:**  
  - Adjust inventory and staffing levels during identified peak periods.
  - Consider revising the menu or launching targeted promotions for high-performing pizzas.
- **Future Work:**  
  - Extend the analysis by integrating customer feedback data.
  - Develop predictive models to forecast future sales trends.

