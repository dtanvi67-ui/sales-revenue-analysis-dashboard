# Build the dashboard in Power BI Desktop

## 1. Import the dataset
- Open Power BI Desktop.
- Choose **Home → Get data → Text/CSV**.
- Select `data/sales_data.csv`, then choose **Transform Data**.

## 2. Check and clean data
- Set `OrderDate` to Date.
- Set `Quantity` to Whole number.
- Set `Discount` to Decimal number.
- Set `UnitPrice`, `UnitCost`, `Sales`, `Cost`, and `Profit` to Decimal number.
- Check for blank OrderID values and errors, then choose **Close & Apply**.

## 3. Create the date table and measures
- Select **Modeling → New table** and paste the DateTable expression from `powerbi/measures.dax`.
- Create relationship `DateTable[Date]` to `SalesData[OrderDate]`.
- Mark DateTable as the date table.
- Add each measure from `powerbi/measures.dax` using **Modeling → New measure**.

## 4. Design the report page
- Top: title and slicers for Year, Region, Category, Payment Mode.
- KPI cards: Revenue, Orders, Quantity, Profit, Profit Margin, Average Order Value.
- Middle: monthly revenue line chart and revenue by region bar chart.
- Bottom: revenue by category donut, Top 10 products bar chart, profit by product column chart.

## 5. Add slicers
Use `DateTable[Year]`, `SalesData[Region]`, `SalesData[Category]`, and `SalesData[PaymentMode]`. Use dropdown style and check **Format → Edit interactions**.

## 6. Format
Use a clean light background, consistent font, Indian Rupee (₹) for revenue/profit, and percentage formatting for margins and discounts. Import `powerbi/sales_theme.json` from **View → Themes → Browse for themes**.

## 7. Save
Save as `Sales_Revenue_Analysis.pbix`. The PBIX must be created in Power BI Desktop; it is not included as a prebuilt file.

## Business questions
1. Which region generated the highest revenue?
2. Which product generated the highest revenue?
3. Which month had the highest revenue?
4. Which category contributed the most revenue?
5. Which products or regions have lower profit margins?

The included practice dataset is synthetic. Do not present its findings as real company results.
