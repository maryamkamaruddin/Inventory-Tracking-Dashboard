# Inventory-Tracking-Dashboard

- About this project : Guided Project
- Tools : Excel

Goal

This project focuses on building an interactive inventory management dashboard in Microsoft Excel using Power Query, Power Pivot, and DAX. The objective is to clean, transform, model, and analyze inventory and forecast data to support inventory monitoring, expiry risk management, and replenishment decision-making.

Data Overview

The data was sourced from YouTube channel, @skillnator dataset titled "Master Excel: Create an Interactive Inventory Tracking Dashboard!". There are three key files intended for the dashboard setup :
- Forecast.xlsx : Contains product IDs and monthly forecasts from May to October 2024.
- Inventory Report.xlsx : Displays product IDs, expiry dates, inventory quantity, value, and report date.
- Mapping.xlsx : Includes a calendar table and product master data, defining product characteristics such as categories and lead times.

Data Transformation

New Excel file is created for the dashboard and uses Power Query to extract data from the key files, bringing all necessary sheets into a single workbook . The process includes transforming the data into a structured format, such as changing data types and unpivoting columns to better facilitate analysis.

Data Modeling

Data modeling was performed using Power Pivot, where relationships between forecast, inventory, and mapping tables were established. The Power Pivot data model enables accurate aggregation, filtering, and calculation across multiple tables.

![Image Alt](https://github.com/maryamkamaruddin/Inventory-Tracking-Dashboard/blob/e63a7ea6b48baadb1d7a09024e98b7e508dd98f6/data%20model.JPG)

Pivot Table

Using the established data model, a pivot table is created to start analyzing the data.

- Pivot table 1 : Product-level table showing stock quantities, forecasts, stock cover, lead time, reorder indicators, reorder quantity, and expiry buckets. This table forms the core analytical view of the dashboard.
- Pivot table 2 : Monthly forecast totals used for the forecast-by-month bar chart.
- Pivot table 3 : Stock quantities aggregated by product category for the category pie chart.
- Pivot table 4 : Stock quantities aggregated by expiry buckets for the expiry risk pie chart.

Dashboard Design

![Image Alt](https://github.com/maryamkamaruddin/Inventory-Tracking-Dashboard/blob/e63a7ea6b48baadb1d7a09024e98b7e508dd98f6/Dashboard.JPG)


- Metrics and Calculations
Several calculations are key to the dashboard :
  - Stock Cover : Calculated using current stock quantities and average forecasted sales to estimate how long inventory will last.
  - Expiry Buckets : Products are categorized by expiration dates, indicating stocks expiring within different time frames ( within 6 months, 6-12 months, more than 12 months).
  - Reorder Metrics : Logic to flag low-stock items and calculate reorder quantities based on forecast demand and available stock.
  - Forecasts : DAX measures such as Fcst M+1, Fcst M+2, Fcst M+3 are created for dynamic future sales forecasting based on existing inventory data. Error handling with IF statements is implemented to account for scenarios where forecasts are absent.

- Charting and Visualization
  - The dashboard includes multiple visual elements:
      - Bar chart showing forecasted demand by month
      - Pie chart showing stock quantity distribution by product category
      - Pie chart showing stock distribution by expiry bucket
  - The pivot tables supporting these visuals are organized in a separate worksheet to maintain a clean and structured dashboard layout.

- Finalization and Formatting
  - The dashboard was finalized by adding KPI summary cards, conditional formatting, and clear data labels. Formatting techniques such as alignment, borders, color coding, and visual hierarchy were applied to improve readability and presentation quality. Reorder flags were highlighted to draw attention to critical inventory items.

- Interactivity
  - Slicers were added to allow users to dynamically filter the dashboard by product category, enhancing interactivity and usability for different analysis needs.

Conclusion

This project demonstrates a structured end-to-end approach to building an inventory tracking and decision-support dashboard in Excel, covering data integration, transformation, modeling, calculation, visualization, and interactivity. The dashboard provides actionable insights into inventory health, expiry risk, and replenishment requirements.

Source: https://www.youtube.com/watch?v=F758-wUXznc 
