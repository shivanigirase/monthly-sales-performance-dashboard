# Monthly Sales Performance Dashboard (2016–2018)

## Project Overview
This project presents an interactive Power BI dashboard built using the Olist Brazilian E-Commerce Public Dataset. It helps analyze monthly sales performance, order trends, average payment, and yearly business performance from 2016 to 2018.

The dashboard contains two pages:
1. **Monthly Sales Performance**
2. **Business Insights**

## Project Objectives
- Analyze monthly revenue and order trends.
- Track key business performance indicators.
- Compare yearly revenue and order performance.
- Provide interactive filtering through date and year slicers.
- Present business data in an easy-to-understand visual format.

## Tools and Technologies
- Microsoft Power BI
- Power Query
- DAX
- CSV Dataset

## Dataset
**Source:** [Olist Brazilian E-Commerce Public Dataset on Kaggle](https://www.kaggle.com/olistbr/brazilian-ecommerce)

The dataset contains Brazilian e-commerce order information from 2016 to 2018.

## Data Cleaning and Transformation
- Imported the prepared dataset into Power BI.
- Inspected column data types and data quality using Power Query.
- Checked the `monthly_revenue` table for valid, error, and empty values.
- Verified that all four columns in this table showed 100% valid values, with 0% errors and 0% empty values.
- Applied the data to the Power BI model.

No unnecessary cleaning operations were performed on this table because the inspected data was already valid.

## Dashboard Features

### Page 1: Monthly Sales Performance
- Total Revenue KPI
- Total Orders KPI
- Average Payment KPI
- Monthly Revenue Trend
- Monthly Orders Trend
- Monthly Average Payment Trend
- Monthly Revenue vs Orders comparison
- Date Range Slicer
- Reset Filters Button

### Page 2: Business Insights
- Key Performance Indicators
- Monthly Performance Table
- Annual Revenue Comparison
- Annual Orders Comparison
- Year Slicer

Both pages support synchronized filtering, allowing users to explore performance by date and year.

## DAX Measure

The following DAX measure was created to calculate the correct average payment in the monthly performance table:

dax
Average Payment Correct =
DIVIDE(
    SUM(monthly_revenue[monthly_revenue]),
    SUM(monthly_revenue[total_orders]),
    0
)

This calculates the overall average using total revenue divided by total orders, ensuring that the total matches the Average Payment KPI.

## Key Insights
- The dashboard makes it possible to compare monthly revenue and order trends.
- Users can examine differences in yearly revenue and order performance.
- Monthly average payment can be compared across different periods.
- Date and year filters help explore specific periods.

**Note:** The dataset covers partial years in 2016 and 2018, so yearly comparisons should be interpreted with that limitation in mind.

## Currency Display Note
The dashboard uses the ₹ symbol as a display format. The original dataset's monetary values were not converted from Brazilian Real to Indian Rupees. Therefore, the symbol should not be interpreted as a currency conversion.

## Dashboard Screenshots
Monthly_Sales_Performance.png
Business_Insights.png
## Conclusion
This project demonstrates the use of Power BI, Power Query, and DAX to build an interactive sales performance dashboard. It provides a clear view of revenue, orders, and average payment trends and allows users to explore business performance through interactive filters.
