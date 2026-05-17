# Food-delivery-business-analysis
## Project Overview
Hi! This is an end-to-end Power BI project where I analyzed the sales and operations data of a food delivery business. The main goal of this project was to take messy raw data, clean it up, connect it properly, and build an interactive dashboard. This dashboard helps the business tracking their daily orders, total revenue, profit margins, and customer satisfaction.

## The Problem
The management of this food delivery service was struggling to see how their business was performing. They did not have a clear view of their total sales or profits. They also did not know which food categories were selling the most, which restaurants were making losses, or why some orders were being cancelled. I built this dashboard to solve these problems and provide clear answers.

## What I Did (Step-by-Step)

### 1. Data Cleaning (Power Query)
The raw data had some missing values and incorrect data types. I imported the data into **Power Query** and did the following:
* Removed blank rows and fixed errors in important columns like Order ID and Customer ID.
* Changed data types so that prices show as currency and dates are easy to filter.
* Filtered out unnecessary columns to keep the file size small and fast.

### 2. Data Modeling
Instead of putting everything into one massive, messy sheet, I organized the data into a **Star Schema**. I created:
* **Fact Table:** `Fact_Orders` (contains numbers like sales amounts and order dates).
* **Dimension Tables:** `Dim_Customers`, `Dim_Restaurants`, and `Dim_Products` (contain details about people, places, and food items).
I connected them using 1-to-many relationships so the dashboard updates smoothly when you click on any filter.

### 3. DAX Calculations
I wrote simple and effective DAX formulas to calculate the key business metrics
Total Orders = COUNT(Fact_Orders[Order_ID])
Total Revenue = SUM(Fact_Orders[Sales_Amount])
Total Profit = SUM(Fact_Orders[Revenue_Amount]) - SUM(Fact_Orders[Cost_Amount])
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)

###4. Dashboard Insights & Results
The final dashboard shows exactly how the business is running:
•	KPI Cards: Show total orders, total sales, and profit percentage right at the top.
•	Food & Restaurant Performance: Charts show which food categories bring in the highest profit and which items are performing poorly or causing losses.
•	Order Status Tracker: Shows the percentage of delivered versus cancelled orders. It helps management look at the specific reasons why orders got cancelled so they can fix those operational issues.
•	Time Trends: A simple line chart that displays sales trends across months and quarters, helping to spot busy seasons.

How to Check Out My Project
1.	Download and open the .pbix file using Power BI Desktop.
2.	Click on different charts, months, or food categories to see how the numbers change automatically!


