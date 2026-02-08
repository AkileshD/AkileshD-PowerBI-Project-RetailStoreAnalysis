# AkileshD-PowerBI-Project-RetailStoreAnalysis

# Retail Sales Performance Analysis (Power BI)

## 📌 Project Overview
**Role:** Data Analyst  
**Tools:** Power BI, Power Query, DAX  
**Dataset:** Superstore Sales Data (US Region)

A nationwide retail company is experiencing inconsistent profit margins across its four regions (North, South, East, West). While revenue is growing, some regions and product categories are seeing negative profits.

**The Goal:** Build a Power BI dashboard to identifies profitable products, highlight regional performance gaps, and support decision-making for inventory planning.

![Dashboard Preview](dashboard_screenshot.png)
<img width="1115" height="628" alt="image" src="https://github.com/user-attachments/assets/40641fcf-58eb-4304-a858-a39247d1da52" />


## ⚙️ Data Modeling & Transformation
To ensure performance and scalability, I transformed the raw flat file into a **Star Schema** data model.

1.  **ETL Process (Power Query):**
    * Filtered data to "United States" for nationwide analysis.
    * Standardized Region names (Mapped "Central" to "North").
    * Created explicit Dimension tables for **Customers** and **Products** to normalize the data.

2.  **The Data Model:**
    * **Fact_Sales:** Contains quantitative transactional data (Sales, Profit, Discount).
    * **Dim_Product:** Contains static product details (Category, Product Name).
    * **Dim_Customer:** Contains unique customer identifiers.

3.  **Key DAX Measures:**
    * `Total Sales = SUM(Fact_Sales[Sales])`
    * `Total Profit = SUM(Fact_Sales[Profit])`
    * `Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)`

## 📊 Key Insights
* **Category Performance:** "Technology" is the clear leader in both Sales and Profit.
* **The "Furniture" Problem:** While Furniture generates significant revenue (High Sales), it has a dangerously low Profit Margin compared to Office Supplies and Tech. This suggests high operational costs or excessive discounting.
* **Regional Strategy:** The map visualization highlights specific states where profitability is negative, indicating a need to restructure shipping logistics or pricing in those zones.

## 🚀 Conclusion
The analysis suggests discontinuing heavy-discount items in the Furniture category (specifically Tables) and focusing marketing efforts on the high-margin Technology sector.
