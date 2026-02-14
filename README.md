# Automotive Financial Performance & Gross Margin Report (SAP Integrated)

## Project Overview
This project is an Enterprise-grade Business Intelligence solution designed for the automotive industry. It transforms raw, fragmented SAP monthly sales reports into a high-performance, interactive dashboard suite. The system provides deep visibility into profitability (EBIT, CM1/CM2), cost structures, and data integrity for multiple departments.

**Business Impact:** Automated the monthly financial closing analysis, reducing manual verification time by ~80% and providing instant outlier detection for the Cost Engineering and Sales Controlling team.

## Tech Stack
- **Tool:** Power BI Desktop
- **Data Source:** SAP ERP Exports (Multi-source SharePoint integration)
- **Languages:** DAX (Data Analysis Expressions), M (Power Query)

## Data Architecture & Modeling
The solution leverages a robust **Star Schema** to connect multiple SharePoint-hosted Excel databases. 
- **Fact Table:** Cumulative Sales & Cost data (Turnover, Material Cost, 3rd Party, Scrap, Labor, Overheads, EBIT).
- **Dimension Tables:** Customers, Sales Organizations, Material Master, and Project Mapping.
- **Logic Layer:** Advanced Power Query (M) scripts handle data cleansing and automated merging of disparate naming conventions.


## Key Dashboards & Features

### 1. Key Account Manager (KAM) Dashboard
- **Monthly Matrix View:** Interactive P&L breakdown by customer part numbers.
- **Dynamic Slicers:** Multi-year selection and customer-specific drill-downs.
- **Custom Visuals:** Integrated navigation and tooltips for instant KPI previews.
- **Dictioniary:** Advanced Power BI function to decrease the loading time by using merging into main data tables.

![KAM Dashboard View](logic/docs/screenshots/dashboard1-1.png)

### 2. Purchasing & Procurement View
- **Cost Driver Analysis:** Circle charts identifying TOP 3 materials with the highest monthly cost variance.
- **Trend Tracking:** Area charts for EBIT, Volume, and Material Cost performance.

![Purchasing View](logic/docs/screenshots/dashboard2.png)

### 3. Generic YTD Summary
- **Advanced Navigation:** Bookmark-based toggles to switch between Scatter Charts and Detailed Matrix views.
- **Profitability Gauges:** Real-time tracking against budget and target margins.

![Generic YTD View](logic/docs/screenshots/dashboard3.png)

### 4. Anomaly & Profitability Tracker (Data Integrity)
- **Outlier Detection:** Flagging of non-compliant SAP entries (e.g., Negative Turnover, Material Ratio > 100%, EBIT % etc. anomalies).
- **Strategic Focus:** Bottom 5 Customers and Bottom 3 Products identification based on negative total EBIT.

![Anomaly & Profitability Tracker](logic/docs/screenshots/dashboard4.png)

## Technical Showcase (DAX & M)
The project includes complex business logic, such as:
- **Dynamic KPI Naming:** Leveraging a bridge table to switch between SAP, P&L, and Gross Margin naming conventions dynamically.
- **Variance Analysis:** DAX measures for Year-over-Year and Month-over-Month comparisons.

> **Note:** You can find the raw logic scripts in the `/logic` folder of this repository.

## Repository Content
- `/logic`: Technical documentation of DAX measures and Power Query scripts.
- `/logic/docs`: High-resolution screenshots of the reporting pages, model view and data tables.
