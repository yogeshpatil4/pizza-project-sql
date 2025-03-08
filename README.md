Pizza Sales Analysis Project Overview
1. Introduction
This project analyzes pizza sales data to extract actionable insights and identify trends that can drive business decisions. The objective is to understand customer ordering patterns, revenue drivers, and product performance by using SQL queries on a structured dataset.

2. Data Description
Dataset Composition:
The project utilizes multiple tables including:

Orders: Contains overall order information.
Order_Details: Lists individual pizza orders with quantities and prices.
Pizzas: Provides details about each pizza, such as type, size, and price.
Pizza_Types: Categorizes pizzas into various groups (e.g., vegetarian, non-vegetarian).
Data Source & Timeframe:
The dataset is sourced from Kaggle and covers sales data from January 1, 2015 to December 31, 2015.

3. Methodology
The analysis is structured into three levels—Basic, Intermediate, and Advanced—each answering specific business questions using SQL:

Basic Analysis
Total Orders: Retrieve the total number of orders placed.
Revenue Calculation: Calculate the total revenue generated from pizza sales.
Highest-Priced Pizza: Identify the highest-priced pizza.
Popular Size: Determine the most common pizza size ordered.
Top 5 Pizza Types: List the top five most ordered pizza types along with their order quantities.
Intermediate Analysis
Category Quantities: Join tables to find the total quantity ordered for each pizza category.
Hourly Distribution: Determine the distribution of orders by hour of the day to identify peak times.
Category-Wise Distribution: Analyze how pizzas are distributed across different categories.
Daily Averages: Group orders by date and calculate the average number of pizzas ordered per day.
Top 3 Revenue-Driven Pizzas: Identify the top three most ordered pizza types based on revenue.
Advanced Analysis
Revenue Contribution: Calculate the percentage contribution of each pizza type to the total revenue.
Cumulative Revenue: Analyze how revenue accumulates over time.
Category-Specific Top Pizzas: Determine the top three revenue-generating pizza types for each pizza category.
4. Analysis and Findings
Sales Trends: The analysis reveals peak ordering hours and high-demand days, which are critical for resource planning.
Product Performance: Insights into the most popular and highest-priced pizzas help in refining the menu and promotions.
Revenue Drivers: The advanced analysis quantifies the contribution of each pizza type to overall revenue, guiding inventory and marketing strategies.
5. Conclusion and Recommendations
Key Insights:
A significant percentage of orders occur during specific hours, indicating peak demand periods.
Certain pizza types consistently drive higher revenue, suggesting these should be emphasized in marketing and promotions.
Business Implications:
Adjust inventory and staffing levels during peak times.
Consider revising the menu based on the performance of various pizza types.
Future Work:
Extend the analysis by integrating customer feedback data.
Explore predictive models to forecast future sales trends.
