🍕 Pizza Sales Report | Power BI + SQL Project

📊 Overview
This project analyzes pizza sales data to uncover key business insights such as revenue trends, order behavior, and sales performance by category and size. The insights are visualized in a dynamic Power BI dashboard, supported by structured SQL queries used for data extraction and KPIs.

🔧 Tools Used
PostgreSQL
Power BI
DAX
Data Cleaning & Modeling

📁 Files Included
Pizza Sales Dashboard (Power BI Screenshot).png – Preview of the Power BI dashboard
PIZZA ORDERS SQL QUERIES.docx – Document containing all SQL queries used
README.md – Project explanation

📌 Key KPIs Calculated (SQL)
sql
Copy
Edit
-- 1. Total Revenue
SELECT SUM(total_price) AS Total_Revenue FROM pizza_sales;

-- 2. Average Order Value
SELECT (SUM(total_price) / COUNT(DISTINCT order_id)) AS Avg_order_Value FROM pizza_sales;

-- 3. Total Pizzas Sold
SELECT SUM(quantity) AS Total_pizza_sold FROM pizza_sales;

-- 4. Total Orders
SELECT COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales;

-- 5. Average Pizzas Per Order
SELECT CAST(SUM(quantity) AS DECIMAL(10,2)) / 
       CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS Avg_Pizzas_per_order
FROM pizza_sales;

📈 Dashboard Highlights (Power BI)

Total Revenue: 817.86K
Avg Order Value: $38.31
Total Orders: 21,350
Pizzas Sold: 49,574
Avg Pizzas/Order: 2.32
Top Category: Classic
Top Size: Large
Busiest Days: Friday/Saturday
Best Months: July & January

📊 Additional Insights

➤ Daily & Monthly Order Trends
Bar and line visuals reveal peak days and months.

➤ % Sales by Category & Size
Pie charts demonstrate revenue share across categories and pizza sizes.

➤ Best/Worst Performing Pizzas
SQL logic to find:
Top/Bottom by Revenue
Top/Bottom by Quantity Sold
Top/Bottom by Orders Placed

📥 How to Use
Run the SQL queries on your pizza sales database.
Import the output or the table directly into Power BI.
Load visualizations and apply DAX where needed.
Explore insights and share interactive dashboards.
