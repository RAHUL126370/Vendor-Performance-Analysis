# Vendor-Performance-Analysis

📘 Untitled.ipynb – Initial Data Cleaning & Exploration 🧹🔍

This is the first step in your data workflow.

What it does:

1. Loads the raw data from Excel or CSV files
2. Checks and handles missing values or duplicates
3. Fixes column types (e.g., converting dates, numbers)
4. Cleans column names for consistency
5. Maybe filters out unnecessary rows (like test data or null entries)

✅ Why it matters:
This notebook ensures that the data is clean and usable. Garbage in = garbage out — so this is an essential step to prepare for meaningful analysis.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

📗 Untitled1.ipynb – Exploratory Data Analysis (EDA) & Feature Engineering 📊🛠

This is where you start digging deeper into the cleaned data.

What it does:

1. Groups and summarizes data (e.g., total sales per vendor or brand)
2. Calculates new columns like:
3. Profit = Sales - Purchase
4. Profit Margin = Profit / Purchase
5. Tax = Derived from sales
6. Analyzes trends across categories (like large vs small orders)

📙This SQL query is designed to generate a detailed summary of vendor performance by analyzing data related to purchases, sales, and freight costs. It employs Common Table Expressions (CTEs) to organize the logic into three distinct components for better readability and modularity.

The first CTE, FreightSummary, calculates the total freight cost associated with each vendor by aggregating data from the vendor_invoice table. The second CTE, PurchaseSummary, focuses on the purchase side, summarizing the quantity and dollar value of purchases per vendor and brand. It also joins with the purchase_prices table to include the actual purchase price and volume, providing more accurate insights. The third CTE, SalesSummary, captures the sales performance by aggregating total sales quantity, sales revenue, average price, and excise tax for each vendor-brand combination.

In the final SELECT statement, these summaries are combined using LEFT JOINs to ensure all vendors are included, even if some metrics are missing. The result is a unified dataset that presents vendor information, comparisons of purchase and sales metrics, and freight costs. The output is sorted by total purchase dollars in descending order, allowing quick identification of the most significant vendors in terms of procurement volume. This comprehensive view supports strategic decision-making around vendor performance, pricing, and profitability.

🔍 Why it matters:
This step generates metrics and patterns that are used in your Power BI dashboard. Without this, your visuals won’t have real business value.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

📙 Untitled2.ipynb – Validation & Visual Checks ✅📈

This final notebook helps double-check your calculations and data before using it in Power BI.

What it does:

1. Verifies that the total sales, profits, etc., match with the dashboard
2. Creates simple graphs and charts using Python libraries like matplotlib or seaborn
3. Optionally exports the final data to a new CSV/Excel file

🎯 Why it matters:
It ensures that the numbers shown in your dashboard are accurate and trustworthy. It also helps you preview the insights before presenting them visually.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Dashboard

<img width="1323" height="733" alt="Vendor Performance" src="https://github.com/user-attachments/assets/25274254-bcbe-442c-95cb-8fb4d0fd0174" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1320" height="732" alt="Brand Analysis" src="https://github.com/user-attachments/assets/4f0f2e1d-4bdf-458d-abc0-f3cbbdcf570f" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1318" height="739" alt="Drivers of Sales and Profit" src="https://github.com/user-attachments/assets/05af9434-3cf7-4ce4-8258-39bbd2e6310f" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


