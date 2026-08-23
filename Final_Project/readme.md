BMW Car Sales Business Analytics Dashboard
Project Overview

The BMW Car Sales Business Analytics Dashboard is an end-to-end Business Intelligence project developed to analyze 50,000 BMW vehicle sales records and turn raw data into useful business insights.

The project uses MySQL, SQL, Power Query, DAX, and Power BI to study sales performance, vehicle characteristics, pricing patterns, model performance, regional trends, and market preferences.

The final solution provides an interactive three-page Power BI dashboard with KPIs, charts, slicers, and analytical visuals.

Business Objective

The main objective of this project is to develop a Business Intelligence solution that helps understand BMW sales performance and supports data-driven business decisions.

The analysis focuses on:

Sales trends across model years
High-performing BMW models
Regional sales performance
Fuel type preferences
Transmission preferences
Vehicle color patterns
Engine size and mileage
Pricing and price segments
High and low sales performance
Dataset

Dataset: BMW_Car_Sales_Classification.csv

The dataset contains 50,000 BMW sales records.

Main Columns
Column	Description
Model	BMW vehicle model
Year	Vehicle model year
Region	Sales region
Color	Vehicle color
Fuel_Type	Type of fuel used
Transmission	Transmission type
Engine_Size_L	Engine capacity in liters
Mileage_KM	Vehicle mileage
Price_USD	Vehicle price in USD
Sales_Volume	Number of vehicles sold
Sales_Classification	Sales performance classification
Technologies Used
MySQL 8.0 – Database storage and SQL analysis
SQL – Data analysis and business queries
Power Query – Data transformation
Power BI Desktop – Dashboard development
DAX – KPI and analytical calculations
Power BI Service – Report publishing
Project Workflow
BMW CSV Dataset
       ↓
     MySQL
       ↓
 SQL Analysis
       ↓
  SQL View
       ↓
   Power Query
       ↓
   Power BI
       ↓
 DAX Measures
       ↓
  Interactive Dashboard
       ↓
 Power BI Service
SQL Implementation

The BMW dataset was imported into MySQL and stored in the bmw_sales_db database.

SQL was used for:

Data validation
Row-count verification
Missing-value checks
Duplicate checks
Invalid-value checks
Overall sales analysis
Year-wise sales analysis
Region-wise sales analysis
Model-wise sales analysis
Fuel-type analysis
Transmission analysis
Color analysis
Engine-size analysis
Creation of SQL views for Power BI

The main consolidated view used for Power BI is:

vw_bmw_sales_dashboard
Power Query Transformations

The consolidated BMW sales view was imported into Power BI using the MySQL connector.

The following transformations were performed in Power Query:

Verified the imported data
Renamed columns with business-friendly names
Assigned suitable data types
Created Estimated Sales Value (USD)
Created Engine Size Category
Created Price Segment
Checked the transformed data for errors and blanks
Loaded the prepared data into Power BI
Derived Columns

Estimated Sales Value (USD)

Price (USD) × Sales Volume

Engine Size Category

Below 2L
2L - 2.99L
3L - 3.99L
4L+

Price Segment

Under $50K
$50K - $99K
$100K - $149K
$150K+
Dashboard Pages
Page 1 – BMW Sales Overview

Provides a high-level view of BMW sales performance.

Includes:

KPI cards
BMW sales trend by year
Sales performance by region
Sales volume by fuel type
Top BMW models by sales
Slicers for model year, sales region, and fuel type
Page 2 – BMW Vehicle & Model Analysis

Focuses on vehicle characteristics and model performance.

Includes:

Sales volume
Average vehicle price
Average engine size
Average mileage
BMW model performance
Vehicle price vs. sales volume
Vehicle color analysis
Mileage and price trends
Price segment analysis
Slicers for model, transmission type, and price segment
Page 3 – BMW Regional & Market Analysis

Focuses on regional and market-level performance.

Includes:

Total sales volume
High sales count
Low sales count
High sales percentage
Regional contribution
Fuel type analysis
Transmission analysis
Vehicle color analysis
Sales classification
Interactive market filters
Key Business Questions

The dashboard is designed to answer:

What is the overall BMW sales performance?
Which BMW models have the highest sales volume?
How does sales volume change across model years?
Which fuel type contributes the most to sales?
Is there a relationship between vehicle price and sales volume?
Which engine size category performs best?
Which vehicle colors have stronger sales representation?
Which regions contribute most to sales?
What is the difference between high-sales and low-sales performance?
How does the dashboard change when different filters are applied?
Key Insights

The analysis shows that:

Total sales volume is approximately 253 million.
The average vehicle price is around $75K.
The dataset contains 11 BMW models.
Models such as the 7 Series, i8, X1, 3 Series, and i3 appear among the leading models.
The four fuel types have relatively balanced sales contributions.
The average engine size is approximately 3.25 L.
The average mileage is around 100.31K KM.
South America has the highest contribution in the displayed regional analysis.
The dashboard shows a 30.57% High Sales Percentage.
Interactive filters allow users to compare different years, regions, fuel types, models, transmissions, prices, and sales classifications.
Recommendations

Based on the dashboard analysis:

Focus marketing and inventory planning on stronger-performing BMW models and regions.
Monitor fuel-type performance to understand changes in market demand.
Use pricing and sales analysis to support pricing decisions.
Give additional attention to stronger regional markets.
Study vehicle characteristics such as engine size, mileage, color, and transmission to understand market preferences.
Use the interactive dashboard to compare different business segments before making sales and marketing decisions.
Power BI Service

The completed dashboard was published to Power BI Service for browser-based access.

The published report includes:

Three dashboard pages
Interactive slicers
KPI cards
Power Query transformations
DAX calculations
Interactive visualizations
Project Structure
BMW-Car-Sales-Business-Analytics/
│
├── README.md
├── BMW_Car_Sales_Classification.csv
├── BMW_Car_Sales_Proper_SQL.sql
├── BMW_Car_Sales_Business_Analytics.pbix
└── Documentation/
    ├── Project_Report.docx
    └── Project_Presentation.pptx
How to Use the Project
1. Database

Import the BMW CSV dataset into MySQL and create the required database and SQL objects.

2. Power BI

Open the .pbix file in Power BI Desktop.

3. Refresh Data

Make sure MySQL is running and the database connection is available before refreshing the report.

4. Explore the Dashboard

Use the slicers and page navigation to explore:

Sales trends
BMW model performance
Regional performance
Fuel type
Pricing
Vehicle characteristics
Sales classification
Project Outcome

This project demonstrates how raw automotive sales data can be transformed into a practical Business Intelligence solution using MySQL, SQL, Power Query, DAX, and Power BI. The final dashboard brings important BMW sales information together in an interactive format and supports analysis of models, regions, pricing, and vehicle characteristics.
