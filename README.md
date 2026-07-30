Financial Model & Performance Analytics Dashboard (Power BI)
A Power BI financial dashboard built to track core P&L metrics, contribution margins, and rolling cash flow balances against Budget and Prior Year (PY) benchmarks.

🛠️ Architecture & Tech Stack
Reporting & Data Engine: Power BI Desktop, DAX

ETL & Data Transformation: Power Query (M Language)

Data Sources: Excel spreadsheets, transactional financial records

🧹 Data Modeling & ETL Pipeline
Raw financial data was transformed in Power Query to construct a clean star schema model:

Header & Schema Normalization: Handled multi-row headers, dynamically promoted column names via M script, and stripped non-tabular metadata.

Data Cleansing: Standardized data types, filled down category hierarchies, and applied error handling across income/expense records.

Data Integration: Merged and appended transaction logs with budget targets to streamline actual vs. budget comparison logic.

Custom Calendar Table: Generated a dedicated date table via M code (Date, Year, Month, MonthNo, Quarter, Day) to support Time Intelligence DAX functions.

🧠 DAX Logic & Measures
Dynamic P&L Rendering: Utilized SWITCH and SELECTEDVALUE pattern for dynamic metric toggling across rows.

Context Preservation: Implemented ISINSCOPE logic to prevent row-level aggregation skew and control subtotal visibility across hierarchies.

Comparison Engine: Toggled dynamically between Budget and Last Year (PY) metrics to compute variance and % Actual vs. Target using normalized absolute deltas.

⚡ Key Dashboard Features
Interactive Target Toggling: Dynamic slicers allowing end-users to swap comparison targets (Actual vs. Budget / Actual vs. PY).

Profitability Insights: Real-time calculation of Contribution Margin % and Net Profit %.

Cash Flow Monitoring: Dynamic inflow vs. outflow visual tracking with end-of-period cash balance projections.

Cash Flow Tracking: Computed running net flows and rolling bank balance measures.

Organization: Categorized all measures into dedicated Display Folders with custom format strings for improved UI legibility.
