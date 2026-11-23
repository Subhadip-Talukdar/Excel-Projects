# Everlasting Earrings Sales Analysis (Excel)

An exploratory data analysis (EDA) and multi-dimensional Pivot Table project built in Microsoft Excel using 300 sales transaction records across Indian regions from January to June 2025.

## Project Files
- **`RAW_everlasting_earrings_sales_300_rows.csv`**: Raw dataset containing 300 order records and 11 attributes (`OrderID`, `Region`, `State`, `City`, `Month`, `SalesRep`, `ProductType`, `UnitsSold`, `UnitPrice`, `SalesValue`, `CustomerType`).
- **`Pivot_everlasting_earrings_sales_300_rows.xlsx`**: Completed Excel workbook containing standardized date formatting (`Month` converted to date values) and a hierarchical Pivot Table (`Pivot Table 2`) for granular sales reporting.

## Pivot Table Structure & Hierarchies
Built a multi-level tabular Pivot Table (`Pivot Table 2`) to drill down across geographical, operational, and product dimensions:
- **Row Hierarchies**: `Region` → `State` → `City` → `SalesRep` → `CustomerType` → `ProductType`
- **Aggregated Metrics**:
  - `COUNT of OrderID` (Order volume)
  - `SUM of UnitsSold` (Total unit quantity)
  - `AVERAGE of UnitPrice` (Pricing benchmark)
  - `SUM of SalesValue` (Total revenue)

## Analytical Highlights & KPIs
Across **300 orders** spanning **4 regions** (`North`, `East`, `South`, `West`), **18 states**, and **20 sales representatives** (Jan–Jun 2025):
- **Total Revenue**: ₹5,184,250 across 6,680 total units sold (average order value of ₹17,280.83).
- **Regional Performance**: **North** led total sales at ₹1,433,950, closely followed by **East** (₹1,401,500), **South** (₹1,211,450), and **West** (₹1,137,350).
- **Product Category Breakdown**: **Drop Earrings** generated the highest revenue (₹2,102,350), followed by **Hoop Earrings** (₹2,060,400) and **Stud Earrings** (₹1,021,500).
- **Customer Segment Split**: **Wholesale** accounted for ₹2,794,600 (53.9%) of total revenue, outperforming **Retail** at ₹2,389,650 (46.1%).
- **Top Sales Representative**: **Saurav Roy** led individual sales performance with ₹371,600 in total sales value.

## Tools & Excel Features Used
- **Data Cleaning**: Standardized text month strings (`Jan-2025`–`Jun-2025`) into proper Excel date formats.
- **Reporting & Aggregation**: Multi-level tabular Excel Pivot Tables with custom value summarizations (`Count`, `Sum`, `Average`).
