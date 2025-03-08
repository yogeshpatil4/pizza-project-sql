# Pizza Sales Analysis Project Overview

Welcome to the Pizza Sales Analysis Project! This project leverages SQL to analyze pizza sales data, uncovering actionable insights into customer ordering patterns, revenue drivers, and product performance. The dataset is sourced from **Kaggle** and covers sales records from **January 1, 2015 to December 31, 2015**.

## Table of Contents
- [Objectives](#objectives)
- [Data Description](#data-description)
- [Project Level](#project-level)
- [SQL Concepts Covered](#sql-concepts-covered)
- [Methodology](#methodology)
- [Conclusion](#conclusion)
- [Sample SQL Query](#sample-sql-query)

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
  - **Pizza_Types:** Categorizes pizzas (e.g., vegetarian, non-vegetarian).
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

## Sample SQL Query
the total number of orders from the dataset:

```sql
SELECT COUNT(*) AS total_orders
FROM Orders;
```
total revenue generated from pizza sales.

```sql
SELECT 
    SUM(d.quantity * p.price)
FROM
    pizzas p
        JOIN
    order_detail d ON d.piza_id = p.pizza_id;
```
Identify the highest-priced pizza.

```sql
SELECT 
    t.name, t.category, t.ingredients, p.price
FROM
    pizza_types t
        JOIN
    pizzas p ON t.pizza_type_id = p.pizza_type_id
ORDER BY p.price DESC
LIMIT 1;
```
Identify the most common pizza size ordered.
```sql
SELECT size,sum(quantity) qua FROM pizzas p
JOIN order_detail d ON d.piza_id=p.pizza_id
GROUP BY size 
ORDER BY qua DESC LIMIT 1;
```
List the top 5 most ordered pizza types along with their quantities.
```sql
SELECT  pizza_type_id,sum(quantity) quantities from pizzas p 
JOIN order_detail d on p.pizza_id=d.piza_id
GROUP BY pizza_type_id
ORDER BY quantities DESC LIMIT 5
```
Join the necessary tables to find the total quantity of each pizza category ordered.
```sql
SELECT 
    category, SUM(quantity)
FROM
    order_detail d
        JOIN
    pizzas p ON d.piza_id = p.pizza_id
        JOIN
    pizza_types t ON p.pizza_type_id = t.pizza_type_id
GROUP BY category;
```
Determine the distribution of orders by hour of the day.
```sql
SELECT DISTINCT
    (HOUR(time)) hours, COUNT(id)
FROM
    orders
GROUP BY hours;
```
Join relevant tables to find the category-wise distribution of pizzas.
```sql
SELECT 
    category, COUNT(pizza_type_id)
FROM
    pizza_types
GROUP BY category;
```
Group the orders by date and calculate the average number of pizzas ordered per day.
```sql
SELECT 
    AVG(quantities)
FROM
    (SELECT 
        date, SUM(quantity) quantities
    FROM
        orders
    JOIN order_detail ON orders.id = order_detail.order_id
    GROUP BY date) AS orderquantity;
```
Determine the top 3 most ordered pizza types based on revenue
```sql
SELECT 
    NAME, SUM(price * quantity) revenue
FROM
    pizzas
        JOIN
    order_detail ON pizzas.pizza_id = order_detail.piza_id
        JOIN
    pizza_types ON pizza_types.pizza_type_id = pizzas.pizza_type_id
GROUP BY name
ORDER BY revenue DESC
LIMIT 3
```
Calculate the percentage contribution of each pizza type to total revenue.
```sql
SELECT 
    category,
    (revenue / (SELECT 
            SUM(price * quantity)
        FROM
            pizzas
                JOIN
            order_detail ON pizzas.pizza_id = order_detail.piza_id
                JOIN
            pizza_types ON pizza_types.pizza_type_id = pizzas.pizza_type_id)) * 100
FROM
    (SELECT 
        category, SUM(price * quantity) AS revenue
    FROM
        pizzas
    JOIN order_detail ON pizzas.pizza_id = order_detail.piza_id
    JOIN pizza_types ON pizza_types.pizza_type_id = pizzas.pizza_type_id
    GROUP BY category) AS categorywise_revenue;
```
Analyze the cumulative revenue generated over time.
```sql
SELECT date, SUM(SUM(revenue)) OVER(ORDER BY date) 
FROM 
(SELECT date,price * quantity revenue FROM pizzas 
JOIN order_detail ON order_detail.piza_id=pizzas.pizza_id
JOIN orders ON orders.id=order_detail.order_id) R
GROUP BY date;
```
Determine the top 3 most ordered pizza types based on revenue for each pizza category.
```sql
SELECT category,name,revenue FROM 
(SELECT category,name,revenue, RANK() OVER(PARTITION BY category ORDER BY revenue DESC) rn
FROM
(SELECT name,category,SUM(price*quantity) as revenue
FROM pizzas 
JOIN order_detail ON order_detail.piza_id=pizzas.pizza_id
JOIN pizza_types ON pizza_types.pizza_type_id=pizzas.pizza_type_id
GROUP BY category,name) a) b
WHERE rn <4
