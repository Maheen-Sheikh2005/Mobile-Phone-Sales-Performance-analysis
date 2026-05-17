# Mobile Phone Sales Performance Dashboard (Power BI)

## Project Overview
Hi! This is an end-to-end Power BI data analysis project where I built an interactive dashboard to track and analyze mobile phone sales across India. The dashboard looks closely at performance indicators for top smartphone brands including Apple, Samsung, OnePlus, Motorola, and Vivo. It helps business owners understand revenue patterns, popular payment types, and geographical demand.

## The Problem
In the highly competitive smartphone market, management needs to track daily sales metrics across different cities and phone models. Without a centralized reporting system, it is difficult to answer questions like: Which city drives the highest sales? What is our average transaction value? What payment methods do our customers prefer? I created this dashboard to turn raw, messy sales logs into instant business insights.

## Steps I Followed to Build This

### 1. Data Cleaning & Preparation (Power Query)
I started by importing the raw transaction data into **Power Query**. To make sure the data was completely clean, I did the following:
* Standardized text columns like `Brand`, `Mobile Model`, and `City`.
* Checked for missing values or blank rows and removed them to protect our data quality.
* Set appropriate data types—changing sales figures into currency and formatting date fields so they could power a monthly filtering menu.

### 2. Data Modeling
To keep the dashboard fast and responsive, I structured the data fields cleanly. I ensured all transactional details like `Total Sales`, `Total Quantity`, and `Price Per Unit` lived within a unified core table (`Sales_Data`), which easily connects to my filters for brands, payment modes, and dates.

### 3. DAX Calculations
I wrote several custom DAX measures to calculate the key business metrics shown on the top cards:
Total Sales = SUM(Sales_Data[Sales_Amount])
Transactions = COUNT(Sales_Data[Transaction_ID])
Total Quantity = SUM(Sales_Data[Units_Sold])
Average = AVERAGE(Sales_Data[Sales_Amount])

### 4. Dashboard Layout & Key Features
The finalized interactive interface is structured across a crisp blue-and-white layout:

KPI Header Cards: Instantly display top-level metrics like Total Sales (769M), Total Transactions (4K), and Total Quantity (19K).

Interactive Month Slider: A custom left-hand navigation bar that allows users to instantly filter the entire page by months (January through December).

Geographical Distribution: An interactive map of India pinpointing exactly which cities generate the highest sales volume.

Payment Mode Split: A colorful pie chart analyzing customer preferences across UPI, Debit Cards, Credit Cards, and Cash.

Trend Analysis: Line and bar charts showing sales over specific days of the week, monthly quantity spikes, and customer rating breakdowns.

How to Interact with the Report
Open the .pbix project file inside Power BI Desktop.

Use the left-side month buttons or top slicers (Brand, Payment Method) to filter data instantly!
