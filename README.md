# Amazon Sales Dashboard: Customer Behavior & Preferences Analysis

A three-page Power BI dashboard that analyzes Amazon sales data for 2025, with a focus on **who the customers are, where they buy from, what they like to buy, and where orders fall through (cancellations).**

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Business Questions](#business-questions)
3. [Dashboard Pages](#dashboard-pages)
4. [Key Insights: Customer Behavior](#key-insights-customer-behavior)
5. [Key Insights: Customer Preferences (What Customers Like)](#key-insights-customer-preferences-what-customers-like)
6. [Recommendations](#recommendations)
7. [Tools Used](#tools-used)
8. [Data Notes & Limitations](#data-notes--limitations)
9. [How to Use](#how-to-use)
10. [Author](#author)

---

## Project Overview

This project turns raw order data into an interactive Power BI report that helps a business understand its customers and its product performance. It covers the period **January to December 2025** and is built around three pages:

| Page | Purpose |
|------|---------|
| **Executive Overview** | High-level KPIs, sales trend, category performance, cancellation rate |
| **Customer & Geography** | Who the top customers are and which locations drive sales |
| **Product Intelligent** | Which products sell most, earn most per unit, and get cancelled most |

**Headline numbers**

| Metric | Value |
|--------|-------|
| Total Sales | 244K |
| Total Orders | 250 |
| Total Quantity Sold | 714 |
| Average Order Value | 975.38 |
| Cancellation Rate | 30.80% |
| Unique Customers | 10 |
| Average Customer Sales | $24.38K |

---

## Business Questions

- Who are the highest-value customers?
- Which locations generate the most sales, and where do customers spend the most per order?
- Which products and categories do customers prefer?
- When do customers buy, and when does demand drop?
- Which products and categories are cancelled the most, and why might that matter?

---

## Dashboard Pages

### 1. Executive Overview
KPI cards (Total Sales, Total Orders, Total Quantity, Average Order Value, Cancellation Rate), a **Sales Trend Over Time** line chart, a **Sales vs Quantity by Product** scatter plot, **Sales by Category**, and **Cancellation Rate by Category**. Slicers: Date, Category, Product, Order Status.

https://github.com/stephensam-analytics/Amazon-powerbi-analytics-2025/blob/04761c594e83fdf32de370dcb426a13c3d679306/Executive%20Overview.png

### 2. Customer & Geography
Customer-level KPIs, **Top 10 Customers by Sales**, **Sales by Location** (pie), **Average Order by Location**, and **Total Orders by Location**. Slicers: Date, Customer Location, Category.

![Customer & Geography](images/customer-geography.png)

### 3. Product Intelligent
**Revenue per Unit by Product**, **Quantity Sold by Product**, **Cancellation Rate by Product**, and Sales vs Quantity. Slicers: Date, Category, Product.

https://github.com/stephensam-analytics/Amazon-powerbi-analytics-2025/blob/dbba33ea5c47cacd5f033c73e718ddfbb4f3fe56/Product%20Intelligent.png

---

## Key Insights: Customer Behavior

**1. Sales come from a small group of customers.**
Only 10 unique customers account for the 244K in sales. The top spenders are Olivia Wilson (36K), Jane Smith (31K), and Emma Clark (30K), followed by John Doe (27K) and three customers at 23K each. Losing even one top customer would noticeably affect revenue.

**2. Sales are spread fairly evenly across locations, with Miami leading.**
Miami (32K, 13%), Denver (30K, 12.2%), Houston (28K, 11.6%), Dallas (27K, 11.1%) and Seattle (27K, 11.0%) lead, but no single city dominates.

**3. The most orders do not mean the biggest orders.**
- Most orders: Houston (32), Miami (31), Dallas (29).
- Highest average order: Seattle (1,222), Denver (1,146), Los Angeles (1,048).

Seattle and Denver customers place fewer but larger orders, while Houston customers place many smaller ones. Los Angeles has the fewest orders (17) but a high average order value.

**4. Buying activity is highly seasonal.**
Sales peaked in **February and March (about 78K each month)**, then dropped sharply from May onward and stayed low for the rest of the year (roughly 4K to 21K per month). Most of the year's revenue was earned in the first quarter.

**5. Almost one in three orders is cancelled.**
The overall cancellation rate is **30.80%**, which is high and is a major source of lost revenue.

---

## Key Insights: Customer Preferences (What Customers Like)

**Revenue is driven by high-ticket categories.**
Electronics (0.13M) and Home Appliances (0.11M) generate almost all of the sales. Books, Clothing and Footwear contribute very little revenue.

**Customers buy small, affordable items most often.**
Top products by quantity sold:

| Product | Units Sold |
|---------|-----------|
| Smartwatch | 105 |
| Smartphone | 97 |
| Headphones | 73 |
| Laptop | 73 |
| Running Shoes | 72 |
| Book | 69 |

Smartwatches and smartphones are the clear favorites by volume.

**High-priced items earn the most per unit.**
Refrigerator ($1,200), Laptop ($800), Washing Machine ($600) and Smartphone ($500) top revenue per unit, while Jeans ($40) and Running Shoes ($60) sit at the bottom. The **Smartphone** is the strongest all-rounder: high volume *and* high revenue per unit.

**Some products are cancelled far more than others.**

| Product | Cancellation Rate |
|---------|------------------|
| Washing Machine | 50.00% |
| Jeans | 45.00% |
| Headphones | 40.00% |
| Refrigerator | 33.33% |
| Running Shoes | 29.63% |
| Book | 28.00% |
| Smartwatch | 26.47% |

By category, Home Appliances (40%) and Clothing (32.5%) have the highest cancellation rates. Customers appear to hesitate more on big purchases (Washing Machine, Refrigerator) and on size/fit-dependent items (Jeans).

---

## Recommendations

1. **Protect and grow top customers.** Introduce loyalty rewards or priority service for the top 10 spenders, since they drive most revenue.
2. **Investigate cancellations.** Review delivery times, pricing, product descriptions and sizing guides for Washing Machines, Jeans and Headphones.
3. **Promote high-volume, high-value products.** Feature Smartphones and Smartwatches in campaigns and bundle them with accessories.
4. **Plan for seasonality.** Run promotions in the low months (May to December) to reduce reliance on the February to March peak.
5. **Tailor by location.** Push premium and high-ticket offers in Seattle and Denver (large orders), and volume or bundle deals in Houston and Miami (frequent orders).
6. **Improve low-revenue categories.** Books, Clothing and Footwear sell in volume but earn little, so test price increases, bundling or cross-selling with Electronics.

---

## Tools Used

- **Power BI**: data modeling, DAX measures, interactive visuals and slicers
- **Excel**: data preparation and cleaning
- **SQL**: querying and shaping the source data

---

## Data Notes & Limitations

- The data covers **3 January 2025 to 3 December 2025**.
- The dataset has only **10 unique customers**, so findings describe this sample and should not be generalized to a full customer base.
- Customer preference is analyzed at the **product and category level** (what sells most), not individual customer-by-product level.
- Reasons for cancellation are not in the data, so the explanations above are hypotheses to be tested.

---

## How to Use

1. Download the `.pbix` file from this repository.
2. Open it in **Power BI Desktop**.
3. Use the **Date**, **Customer Location**, **Category**, **Product** and **Status** slicers on the left of each page to explore the data.

---

## Author

**Stephen Samuel Kayode**
Data Analyst | SQL · Power BI · Excel
GitHub: [stephensam-analytics](https://github.com/stephensam-analytics)
