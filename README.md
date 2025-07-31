# TASK-6B-DATA-ANALYTICS-TECHNOHACKS-INTERNSHIP
📁 Project: Mobile Sales Analytics Dashboard using Power BI
This project is a comprehensive Power BI solution built during my summer internship to analyze and visualize mobile sales performance using interactive dashboards. It consists of three interlinked pages — each focused on a key performance aspect — connected via toggle buttons for seamless user navigation.

🔧 Key Features & Functionality
🧭 Navigation Structure:

Main Dashboard: High-level overview including KPIs, sales by city, mobile models, day names, and rating insights.

Month-to-Date (MTD) Dashboard: Trend analysis of monthly performance for the current month across years.

Same Period Last Year Dashboard: A YOY comparison of sales data by year, quarter, and month using DAX’s SAMEPERIODLASTYEAR.

📈 KPIs Used:

Total Sales (dynamic measure using SUMX)

Total Quantity Sold

Number of Transactions

Average Price

📊 Visualizations:

Line chart for Monthly Sales Trends

Bar/Column charts comparing sales by:

City

Mobile Model

Day Name

Rating Status

Payment Method (including Pie Chart)

YOY sales comparison by Year, Quarter, and Month

Map visualization for geo-level insights

🎯 Measures & DAX Logic:

DAX
Copy
Edit
Total_Quantity = SUM(Sales_Data[Units Sold])
Total_Sales = SUMX(Sales_Data, Sales_Data[Units Sold] * Sales_Data[Price Per Unit])
Transactions = COUNTROWS(Sales_Data)
Average_Price = AVERAGE(Sales_Data[Price Per Unit])
MTD = TOTALMTD([Total_Sales], Custom_Calendar[Date].[Date])
Same Period Last Year = CALCULATE([Total_Sales], SAMEPERIODLASTYEAR(Custom_Calendar[Date].[Date]))
📅 Time Intelligence:

Used a custom calendar table created using Power Query (List.Dates) to support advanced time-based calculations (MTD, YOY).

Enabled data slicing by Year, Quarter, Month, and Day with slicers.

🎨 Design Choices:

Used light blue icons for KPIs to ensure visual hierarchy.

Alternate row backgrounds in tables for readability.

Uniform slicer layout on the left panel across pages.

Interactive icons and illustrations to enhance user engagement.

💡 Impact:
This dashboard enables stakeholders to:

Monitor real-time trends.

Identify top-performing products and regions.

Compare performance across different time frames.

Make informed decisions based on customer behavior and payment preferences.

🔗 Tech Stack:
Power BI Desktop

DAX

Power Query (M Language)

Data Modeling (Star Schema with Calendar Table)
