# Inventory-Tracking-Dashboard

About this project

Goal

This project focuses on analyzing and set up an inventory dashboard in Microsoft Excel, focusing on essential tools as Power Query, DAX and Power Pivot to manage, clean, transform data and create visual reports effectively.

Data Overview

The data was sourced from YouTube channel, @skillnator dataset titled "Master Excel: Create an Interactive Inventory Tracking Dashboard!". There are three key files intended for the dashboard setup :
- Forecast.xlsx : Contains product IDs and monthly forecasts from May to October 2024.
- Inventory Report.xlsx : Displays product IDs, expiry dates, inventory quantity, value, and report date.
- Mapping.xlsx : Includes a calendar table and product master data, defining product characteristics such as categories and lead times.

Data Transformation

New Excel file is created for the dashboard and uses Power Query to extract data from the key files, bringing all necessary sheets into a single workbook . The process includes transforming the data into a structured format, such as changing data types and unpivoting columns to better facilitate analysis.

Data Modeling

The next step involves data modeling using Power Pivot to establish relationships between the tables. Accessing the Power Pivot window enables visualizing these relationships.

Pivot Table

Using the established data model, a pivot table is created to start analyzing the data.

Dashboard Design

- Metrics and Calculations
Several calculations are key to the dashboard :
  - Stock Cover : Calculated based on stock quantities and average forecasted sales.
  - Expiry Buckets : Products are categorized by expiration dates, indicating stocks expiring within different time frames ( within 6 months, 6-12 months, more than 12 months).
  - Reorder Metrics : Conditions for determining when the stock is low and required replenishment, involving checks on forecast metrics and stock levels.
  - Forecasts : DAX measures such as Fcst M+1, Fcst M+2, Fcst M+3 are created for dynamic future sales forecasting based on existing inventory data. Error handling with IF statements is implemented to account for scenarios where forecasts are absent.

- Charting and Visualization
  - Visual elements such as bar charts for sales forecasts and pie charts are created for stock value distribution by expiry buckets. The data behind these charts gets organized in a separated sheet which are consists of pivot table 2, pivot table 3 and pivot table 4.

- Finalization and Formatting
  - The summary shapes are added in the dashboard. The dashboard then is beautified with formatting options, aligning data, borders, and coloring to create an appealing report. Conditional formatting is added to highlight reorder flags and data labels are managed for clarity. The charts and shapes are aligned correctly to ensure a clean presentation.

- Interactivity
  - Slicers are incorporated to filter data dynamically based on categories, significantly enhancing user interaction with the dashboard.

Conclusion

This structured approach outlines key steps in building an inventory tracking dashboard in Microsoft excel, emphasizing the integration, modeling, calculation and visualization phases necessary for effective data reporting.

Source: https://www.youtube.com/watch?v=F758-wUXznc 
