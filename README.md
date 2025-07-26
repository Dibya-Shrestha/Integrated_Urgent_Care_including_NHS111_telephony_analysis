📊 Integrated urgent care including NHS111 telephony-Excel Project
🔍 Project Overview
This Excel-based dashboard visualises key insights from the Integrated Urgent Care (IUC) dataset published by the NHS, including call handling and patient interaction data from NHS 111 telephony services. The dashboard enables users to track and analyse KPIs over time, by region, and across service categories.

📥 Data Source
Official Source: Patient Experience Survey (PES)
- IUCADC-Apr-to-May25.csv
- IUCADC-Apr2022-to-Mar2023_REVISED.csv
- IUCADC-Apr23-to-Mar24-Revised.csv
- IUCADC-Apr23-to-Mar25-Revised-1.csv
- IUCADC-to-March2022.csv
- IUCADC_Data_KPI_Combined_Time_Series-to-Mar-2025-inc.-revisions-for-Apr23-to-Mar24-v2-1.xlsx(Access Month Sheet for KPI Description)

All files were integrated into a single consolidated Excel file for unified analysis.

🧹 Data Preparation
✅ Cleaning and Standardisation Steps:
- Merged All Files: Combined multiple yearly IUC datasets (2021–2026) into a single structured sheet.
- Date Formatting: Standardised all REPORTING_PERIOD entries (e.g., "APR-2025") into consistent Month-Year format.
- Missing Data Handling: Replaced empty ORG_NAME fields (e.g., Y00415, 0AR) with "UNKNOWN".
- Added a new column for KPI descriptions using VLOOKUP, referencing the downloaded KPI Glossary Excel file.
- Grouped KPIs into letter-based categories for visual clarity (e.g. A = Demand for IUC, B = Call Handling, etc.).

📈 Dashboard Components
🎨 Visual Elements Included:
Chart	Description
- Clinical Workforce Utilisation	Pie chart showing distribution of call assessments by workforce type
- Total Calls by Region	Bar chart comparing total call volumes across NHS regions
- Call Handling Over Time	Line chart showing change in calls (received, answered, abandoned) by year
- Calls Abandonment Analysis	100% stacked bar showing abandonment patterns by year
- Disposition of Calls	Stacked bar chart categorising call outcomes across time
- NHS Service Activity	Combination chart illustrating different KPI categories
- Interactive Cards	KPI cards displaying grand totals.

📊 Output
The Excel file contains the complete analysis pipeline:
- Original Merged Sheet: Raw NHS IUC ADC data as downloaded and consolidated from NHS England.
- Cleaned Sheet: Standardised data with consistent date format, filled missing ORG_NAME as "UNKNOWN", and extracted Month, Year, and KPI Category
- KPI Description Sheet: Copied from Month Sheet from the original KPI file, Transformed KPI Description file to perform analysis
- Pivot Table Sheets: Aggregated views for key metrics such as total calls, abandonment patterns, regional trends, and clinical assessments.
- Dashboard: A visual summary featuring KPI cards, slicers, and charts for stakeholder-ready insights.

🛠 Technical Notes
Excel Formulas Used:
- GETPIVOTDATA() for dynamic card metrics
- TEXT() and MID() to parse REPORTING_PERIOD
- IF() to categorise unknown orgs
- Slicer Integration: Yearly and Monthly slicers are linked to visuals for dynamic filtering.
- VLOOKUP to map and populate each KPI code to its full definition.
- Conditional Formatting: Used in pivot tables for comparative insights.

📌 Future Improvements
- Automate data refresh via Power Query
- Integrate Power BI version
- Add benchmark KPIs for performance comparison
