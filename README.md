☕ Starbucks Sales Dashboard – Power BI Project
This project showcases an interactive Power BI dashboard built using real-world Starbucks sales data. It focuses on sales insights, trends, top-performing categories, and visual storytelling through clean and meaningful visualizations.

📌 Project Overview
After attending a Power BI webinar, I started building an initial version of the Starbucks Sales Dashboard.
This project is the enhanced and complete version, incorporating data cleaning, transformation, visualization, and DAX-based analysis.

🔄 Workflow
1. Dataset Collection
Source: Starbucks Raw Sales Data (CSV format/Excel format)
Contains: Order ID, Product_Id,Product Type, Category, Store Location, Quantity, Unit Price, Total Amount,transaction_Qty,transaction_Date, Size,Product_type, etc.
2. Data Cleaning
Removed null values and duplicates
Standardized column names and formatting
Verified data types for each column
3. Data Transformation
Performed in Power Query Editor
Added new calculated columns
Converted date fields to proper format for time-series analysis
4. Data Loading
Loaded cleaned and transformed data into Power BI Data Model
5. DAX Measures Used
Average Order Value (AOV) -AOV = ROUND([sales]/COUNTROWS(Orders_Table), 2)
Total Sales -sales = SUMX(Orders_Table, Orders_Table[transaction_qty] * RELATED(Products_Table[unit_price]))
Sales from Coffee Category -sales_coffee = CALCULATE([sales], Products_Table[product_category] = "Coffee")
Total Products -total_products = COUNTROWS(Products_Table)
Total Quantity Sold -total_quantity = SUM(Orders_Table[transaction_qty])
📊 Dashboard Highlights
Total Quantity Sold: 214K+
Total Sales: ₹58.87M
Top-Selling Category: Coffee – ₹2.27Cr+
Visualizations:
Card KPIs (Total Sales, AOV, Quantity)
Bar & Line Charts (Monthly Trends)
Donut Charts (Product Categories)
Slicers (Month, Category, Store Location)
Tooltips & Drill-down features
🛠️ Tools & Technologies
Tool	Purpose
Power BI	Data visualization & dashboard
Power Query	Data transformation & shaping
DAX	Custom measures & calculations
Excel / CSV	Initial raw data format.
