# BMW Car Sales Business Analytics Dashboard

## Project Overview

The **BMW Car Sales Business Analytics Dashboard** is an end-to-end Business Intelligence project developed to analyze **50,000 BMW vehicle sales records** and turn raw sales data into useful business insights.

The project combines **MySQL, SQL, Power Query, DAX, and Power BI** to study sales performance, vehicle characteristics, pricing patterns, model performance, regional trends, and market preferences.

The final solution provides an interactive **three-page Power BI dashboard** that helps users explore BMW sales data through KPIs, charts, slicers, and analytical visuals.

---

## Business Objective

The main objective of this project is to develop a Business Intelligence solution that helps understand BMW sales performance and supports data-driven business decisions.

The analysis focuses on:

- Sales trends across model years
- High-performing BMW models
- Regional sales performance
- Fuel type preferences
- Transmission preferences
- Vehicle color patterns
- Engine size and mileage
- Pricing and price segments
- High and low sales performance

---

## Dataset

**Dataset:** `BMW_Car_Sales_Classification.csv`

The dataset contains **50,000 BMW sales records**.

### Main Columns

| Column | Description |
|---|---|
| Model | BMW vehicle model |
| Year | Vehicle model year |
| Region | Sales region |
| Color | Vehicle color |
| Fuel_Type | Type of fuel used |
| Transmission | Transmission type |
| Engine_Size_L | Engine capacity in liters |
| Mileage_KM | Vehicle mileage |
| Price_USD | Vehicle price in USD |
| Sales_Volume | Number of vehicles sold |
| Sales_Classification | Sales performance classification |

---

## Technologies Used

- **MySQL 8.0** – Database storage and SQL analysis
- **SQL** – Data validation, business analysis, tables, and views
- **Power Query** – Data transformation and derived columns
- **Power BI Desktop** – Dashboard development
- **DAX** – KPI and analytical measures
- **Power BI Service** – Report publishing and deployment

---

## Project Workflow

```text
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
   DAX Measures
       ↓
  Power BI Dashboard
       ↓
 Power BI Service
```

---

## SQL Implementation

The BMW dataset was imported into MySQL and stored in the `bmw_sales_db` database.

SQL was used for:

- Data validation
- Row-count verification
- Missing-value checks
- Duplicate checks
- Invalid-value checks
- Overall KPI analysis
- Year-wise sales analysis
- Region-wise sales analysis
- Model-wise sales analysis
- Fuel-type analysis
- Transmission analysis
- Color analysis
- Engine-size analysis
- Business-oriented SQL views

The main consolidated view used for Power BI is:

```text
vw_bmw_sales_dashboard
```

This view brings the required BMW sales information together for dashboard development.

---

## Power Query Transformations

The consolidated BMW sales view was imported into Power BI using the MySQL connector.

The following transformations were performed in Power Query:

- Verified the imported dataset
- Renamed columns using business-friendly names
- Assigned appropriate data types
- Created **Estimated Sales Value (USD)**
- Created **Engine Size Category**
- Created **Price Segment**
- Checked transformed columns for errors and blanks
- Loaded the prepared dataset into Power BI

### Derived Columns

**Estimated Sales Value (USD)**

```text
Price (USD) × Sales Volume
```

**Engine Size Category**

```text
Below 2L
2L - 2.99L
3L - 3.99L
4L+
```

**Price Segment**

```text
Under $50K
$50K - $99K
$100K - $149K
$150K+
```

---

## DAX Measures

The Power BI report uses the following key DAX measures:

```DAX
Total Sales Volume =
SUM(bmw_sales_Data[Sales_Volume])
```

```DAX
Average Vehicle Price =
AVERAGE(bmw_sales_Data[Price_USD])
```

```DAX
Total BMW Models =
DISTINCTCOUNT(bmw_sales_Data[Model])
```

```DAX
High Sales Count =
CALCULATE(
    COUNTROWS(bmw_sales_Data),
    bmw_sales_Data[Sales_Classification] = "High"
)
```

```DAX
Low Sales Count =
CALCULATE(
    COUNTROWS(bmw_sales_Data),
    bmw_sales_Data[Sales_Classification] = "Low"
)
```

```DAX
High Sales Percentage =
DIVIDE(
    [High Sales Count],
    COUNTROWS(bmw_sales_Data),
    0
)
```

```DAX
Average Engine Size =
AVERAGE(bmw_sales_Data[Engine_Size_L])
```

```DAX
Average Mileage =
AVERAGE(bmw_sales_Data[Mileage_KM])
```

```DAX
Maximum Sales Volume =
MAX(bmw_sales_Data[Sales_Volume])
```

---

## Dashboard Pages

### Page 1 – BMW Sales Overview

Provides an executive-level view of the business.

Includes:

- KPI cards
- BMW sales trend by year
- Sales performance by region
- Sales volume by fuel type
- Top BMW models by sales
- Slicers for model year, sales region, and fuel type

### Page 2 – BMW Vehicle & Model Analysis

Focuses on vehicle characteristics and model performance.

Includes:

- Total sales volume
- Average vehicle price
- Average engine size
- Average mileage
- BMW model sales performance
- Vehicle price vs. sales volume
- Sales by vehicle color
- Mileage and average price trend
- Slicers for model, transmission type, and price

### Page 3 – BMW Regional & Market Analysis

Focuses on market and regional performance.

Includes:

- Total sales volume
- High sales count
- Low sales count
- High sales percentage
- Regional contribution to total sales
- Sales classification
- Fuel type distribution
- High-sales performance gauge
- Regional and market filtering

---

## Key Business Questions

The dashboard is designed to answer questions such as:

1. What is the overall BMW sales performance?
2. Which BMW models generate the highest sales volume?
3. How does sales volume change across model years?
4. Which fuel type contributes most to sales?
5. Is there a relationship between vehicle price and sales volume?
6. Which engine size category performs best?
7. Which vehicle colors have stronger sales representation?
8. Which regions contribute most to sales?
9. What is the difference between high-sales and low-sales performance?
10. How does dashboard performance change when different filters are applied?

---

## Key Insights

The dashboard analysis shows that:

- Total sales volume is approximately **253 million**.
- The average vehicle price is around **$75K**.
- There are **11 BMW models** in the dataset.
- The **7 Series, i8, X1, 3 Series, and i3** appear among the leading models in the model analysis.
- Fuel types have a relatively balanced contribution, with Hybrid slightly ahead in the dashboard.
- The average engine size is approximately **3.25 L**.
- The average mileage is approximately **100.31K KM**.
- South America has the highest contribution in the displayed regional analysis.
- High-sales records account for approximately **30.57%** according to the dashboard KPI.
- The dashboard can be filtered interactively to compare different model years, regions, fuel types, transmissions, models, prices, and sales classifications.

---

## Recommendations

Based on the dashboard analysis, the project recommends:

- Focus inventory and marketing efforts on better-performing BMW models and regions.
- Monitor fuel-type performance to understand changes in market demand.
- Use price and sales analysis to support pricing decisions.
- Give additional attention to stronger-performing regions when planning marketing campaigns.
- Study vehicle characteristics such as engine size, mileage, color, and transmission to better understand customer preferences.
- Use the interactive dashboard regularly to compare different business segments before making sales and marketing decisions.

---

## Power BI Service

The completed Power BI report was published to **Power BI Service** for browser-based access.

The published report contains:

- Three dashboard pages
- Interactive slicers
- KPI cards
- DAX-based measures
- Power Query transformations
- Interactive visualizations

---

## Project Structure

```text
BMW-Car-Sales-Business-Analytics/
│
├── README.md
├── BMW_Car_Sales_Classification.csv
├── BMW_Car_Sales_Proper_SQL.sql
├── BMW_Car_Sales_Business_Analytics.pbix
└── Documentation/
    ├── Project_Report.docx
    └── Project_Presentation.pptx
```

> File names can be updated to match the final files uploaded to GitHub.

---

## How to Use the Project

### 1. Database

Import the BMW CSV dataset into MySQL and create the required database and SQL objects.

### 2. Power BI

Open the `.pbix` file in Power BI Desktop.

### 3. Refresh Data

Make sure the MySQL service is running and the database connection is available before refreshing the report.

### 4. Explore the Dashboard

Use the slicers and page navigation to explore:

- Sales trends
- BMW model performance
- Regional performance
- Fuel type
- Pricing
- Vehicle characteristics
- Sales classification

---

## Project Outcome

This project demonstrates how a raw automotive sales dataset can be converted into a practical Business Intelligence solution using **MySQL, SQL, Power Query, DAX, and Power BI**. The final dashboard provides a clear and interactive way to study BMW sales performance and supports data-driven analysis across models, regions, pricing, and vehicle characteristics.

---

## Author

**Ganesh A**

**MCA – Business Analytics / Data Analytics Project**

---

## License

This project is created for **academic and educational purposes**.
