# Adventure Works Power BI Analytics Dashboard

## Project Overview
This project presents an end-to-end analytical dashboard built in Power BI using the Adventure Works dataset.  
The dashboard is designed to deliver both **executive-level insights** and **detailed analytical drill-downs** across sales, revenue, orders, returns, customers, products, and geography.

The focus of this project is on:
- Strong data modeling (star schema)
- Advanced DAX
- Interactive drill-through analysis
- Clean, business-ready dashboard design

---

## Dataset Information
**Dataset Name:** Adventure Works  
**Domain:** Retail / Manufacturing / Sales Analytics  

### Tables Used
- `AW_Sales` (Fact table)
- `Products_Lookup`
- `Product_Categories`
- `Product_Subcategories`
- `Customers_Lookup`
- `Calendar_Lookup`
- `Returns`
- `Territories_Lookup`

A star schema is implemented with proper relationships between fact and dimension tables to ensure optimal performance and correct filter propagation.

---

## Data Modeling
- Fact table at transactional grain
- Separate dimension tables for Products, Customers, Date, and Geography
- One-to-many, single-direction relationships
- Dedicated Date table for time intelligence
- Clean surrogate keys for joins

This model supports advanced time-based analysis such as YoY growth, trend analysis, and cumulative calculations.

---

## Dashboard Pages Overview


Page 1: Executive Summary 
<img width="1382" height="778" alt="AW1" src="https://github.com/user-attachments/assets/080935b9-42fc-4674-9f86-93c0b40d7ec8" />

Page 2: Product Details [drilled from pg 1]  
<img width="1397" height="778" alt="AW2" src="https://github.com/user-attachments/assets/9a58bcee-d0e3-42e4-a948-768e0c0e6e65" />

Page 3 : Customer Deep Dive 
<img width="1395" height="786" alt="AW3" src="https://github.com/user-attachments/assets/64261aa1-f464-4f57-a39c-e1f4a10bf50e" />


## 1. Executive Summary

### Purpose
Provides a high-level overview of business performance for leadership and stakeholders.

### Key KPIs
- Total Revenue
- Total Orders
- Total Quantity Sold
- Total Returns
- Year-over-Year Growth
- Target vs Actual Performance

### Visuals Included
- KPI cards with conditional formatting
- Monthly revenue trend
- Monthly orders trend
- Most ordered product
- Top product by revenue
- Returns vs target KPI
- Revenue distribution by country (Map)
- Total orders by category (Treemap)
- Total orders by subcategory (Hierarchical bar chart)

### Highlights
- Fully interactive slicers for Year, Region, and Category
- Dynamic KPIs responding to filter context
- Clear color consistency for categories
- Executive-ready layout with minimal clutter

---

## 2. Product Details (Drill-Through Page)

### Purpose
Enables deep-dive analysis from summary visuals into detailed product-level insights.

### Drill-Through Configuration
Users can drill through by:
- Category
- Subcategory
- Product Name

The page dynamically adapts based on the drill-through selection.

### Dynamic Title Logic
A dynamic title updates automatically based on drill context:
- If drilled by Category → shows Category name
- If drilled by Subcategory → shows Subcategory name
- If drilled by Product → shows Product name

Implemented using DAX with `SELECTEDVALUE` and `COALESCE`.

### Visuals Included
- Current Month Orders vs Target (Gauge)
- Current Month Returns vs Target (Gauge)
- Weekly Revenue trend with trendline
- Weekly Returns trend with trendline

---

## 3. Customer Analysis

### Purpose
Analyzes customer behavior, demographics, and revenue contribution.

### Visuals Included
- Customer ranking table:
  - Total Orders
  - Total Revenue
- Orders by Gender (Donut chart)
- Orders by Occupation (Donut chart)
- Orders by Age Group (Treemap)
- Monthly Orders & Revenue trend
- Top Customer identification
- Customer-level KPIs

### Insights Enabled
- Identification of high-value customers
- Revenue concentration analysis
- Demographic-based purchasing patterns
- Age-wise order distribution

---

## Advanced DAX Implementation

### Key Measures
- Total Revenue
- Total Orders
- Total Quantity
- Total Returns
- Year-over-Year Growth %
- Previous Year Metrics
- Target Variance Calculations
- Dynamic Measure Switching
- Drill-through aware dynamic titles

### DAX Techniques Used
- CALCULATE
- FILTER
- SELECTEDVALUE
- COALESCE
- DATEADD
- SAMEPERIODLASTYEAR
- Context transition handling
- Filter context optimization

---

## UX & Design Considerations
- Consistent color theme across pages
- Clear visual hierarchy
- Minimal visual clutter
- Drill-through navigation with back buttons
- Executive-friendly layout
- High contrast for readability

---

## Key Learnings
- Importance of proper data modeling for scalable analytics
- Effective use of DAX for dynamic and context-aware insights
- Designing dashboards for both executives and analysts
- Balancing aesthetics with analytical depth

---

## Tools & Technologies
- Power BI Desktop
- DAX
- Power Query
- Star Schema Modeling
- Interactive Data Visualization

---

## How to Use the Report
1. Use slicers on the Executive Summary page to filter by Year, Region, and Category
2. Right-click on visuals to drill through to Product Details
3. Explore customer behavior in the Customer Analysis page
4. Use drill-through navigation to return to summary views

---

## Author
Shreyash Srivastava  
Data Analyst | Business Intelligence | Power BI

---
