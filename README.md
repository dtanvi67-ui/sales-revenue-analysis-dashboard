# Sales & Revenue Analysis Dashboard (Power BI)

A beginner-friendly Power BI portfolio project for exploring sales performance, revenue trends, product performance, and regional results.

> **Dataset note:** The practice data is synthetic and does not represent a real company or real customers. Currency values are in INR (₹).

## Dashboard features
- KPI cards: Total Revenue, Total Orders, Quantity Sold, Total Profit, Profit Margin, Average Order Value
- Monthly revenue trend
- Revenue by region and category
- Top 10 products by revenue
- Profit by product
- Interactive slicers: Year, Region, Category, Payment Mode

## Tools
- Microsoft Power BI Desktop
- Power Query
- DAX
- Excel / CSV

## Quick start
1. Open Power BI Desktop.
2. Select Home → Get data → Text/CSV and import `data/sales_data.csv`.
3. Set `OrderDate` to Date, `Quantity` to Whole number, and numeric sales fields to Decimal number.
4. Select Close & Apply.
5. Create the DateTable and measures from `powerbi/measures.dax`.
6. Create relationship `DateTable[Date]` (one) to `SalesData[OrderDate]` (many).
7. Follow `docs/build_steps.md` to create the report visuals.
8. Save the report as `Sales_Revenue_Analysis.pbix`.

## Project files
- `data/sales_data.csv` — synthetic sample sales data
- `powerbi/measures.dax` — date table and KPI measures
- `powerbi/sales_theme.json` — optional report theme
- `docs/build_steps.md` — step-by-step Power BI instructions

The `.pbix` report is created in Power BI Desktop after following the guide; it is not prebuilt in this repository.

## Tutorial reference
https://youtu.be/hhZ6EDiVboI
