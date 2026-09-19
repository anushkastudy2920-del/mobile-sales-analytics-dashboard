# Mobile Sales Intelligence Dashboard

> **Turning raw sales transactions into business decisions.**

This project transforms **3,800+ mobile sales transactions** into an interactive **Business Intelligence solution using Microsoft Power BI**. It uncovers patterns across products, brands, customers, time, payment behavior, and geographic markets.

The dashboard is designed around practical business questions:

- What is selling?
- Where is it selling?
- Who is buying?
- Which brands and products contribute most to revenue?
- How does sales performance change over time?

---

## Project Highlights

- **3,800+** sales transactions analyzed
- **5** mobile brands
- **15** mobile models
- **19** cities
- **900+** unique customers
- **2021–2024** sales data
- **4** interactive analytical dashboard pages
- Custom **DAX measures**
- **Power Query** based data transformation
- Dedicated **Date Table** for time-based analysis
- Interactive filtering and cross-analysis
- KPI-driven business reporting

---

## Business Objective

Raw transaction-level data contains valuable information, but identifying meaningful patterns directly from the data can be difficult.

The objective of this project was to transform raw mobile sales data into an interactive Business Intelligence dashboard that enables users to:

- Monitor overall sales performance
- Compare brands and mobile models
- Understand customer demographics and purchasing behavior
- Identify geographic sales patterns
- Analyze payment behavior
- Track revenue trends over time
- Compare performance across different business segments

---

## Key Business Questions

The dashboard is designed to answer questions such as:

- Which brands generate the highest revenue?
- Which mobile models have the highest sales volume?
- Which cities contribute most to overall revenue?
- How does customer behavior vary across age groups?
- Which payment methods are most commonly used?
- How does revenue change across months and years?
- Which brands perform strongly across different cities?
- How does sales activity vary across days of the week?

---

# Data-to-Insight Workflow

The project follows a structured workflow to transform raw transaction data into meaningful business insights.

1. **Raw Transaction Data**
   - Collect and use transaction-level sales data from Microsoft Excel.

2. **Data Cleaning & Transformation**
   - Clean data and prepare fields using Power Query.

3. **Data Modeling**
   - Create relationships and a dedicated Date Table for time-based analysis.

4. **DAX Measures & Business Metrics**
   - Create DAX measures for revenue, units sold, transactions, customers, ratings, and other KPIs.

5. **Interactive Power BI Dashboard**
   - Build interactive dashboards using charts, KPI cards, slicers, filters, and matrix visuals.

6. **Business Analysis & Insights**
   - Analyze sales, products, brands, customers, and geographic performance to derive meaningful business insights.

# Dashboard Structure

## 1. Executive Overview

Provides a consolidated view of overall business performance.

### Key Analysis

- Total Revenue
- Total Units Sold
- Total Transactions
- Unique Customers
- Average Customer Rating
- Average Selling Price
- Revenue trends
- Revenue by brand
- Top-performing cities
- Revenue by payment method

### Interactive Filters

- Year
- Brand
- City

This page provides a high-level view of overall sales performance and acts as the main entry point to the dashboard.

---

## 2. Product & Brand Intelligence

Focuses on product demand and brand-level performance.

### Key Analysis

- Revenue by brand
- Units sold by brand
- Revenue by mobile model
- Units sold by mobile model
- Brand revenue trends
- Revenue share by brand
- Brand performance across cities

This page enables comparison between **sales volume and revenue contribution** across different products and brands.

---

## 3. Customer Intelligence

Focuses on customer demographics and purchasing behavior.

### Key Analysis

- Customer distribution by age group
- Revenue by age group
- Customer rating distribution
- Payment method analysis
- Brand performance across customer segments
- Average customer age
- Average customer rating

### Customer Age Groups

- Under 20
- 20–29
- 30–39
- 40–49
- 50–59
- 60+

This page helps identify differences in purchasing behavior and revenue contribution across customer segments.

---

## 4. Geographic & Business Insights

Focuses on geographic patterns and market performance.

### Key Analysis

- Revenue by city
- Units sold by city
- Annual revenue trends
- Revenue by day of week
- City × Brand revenue analysis

This view helps identify differences in sales performance and product demand across geographic markets.

---

# Data Preparation

Power Query was used to prepare the transaction data before analysis.

### Key Transformations

- Corrected data types
- Created a proper transaction date
- Standardized day names
- Created customer age groups
- Prepared the dataset for analytical modeling

### Date Table

A dedicated Date Table was created to support:

- Year analysis
- Month analysis
- Quarter analysis
- Year-month trends
- Time-based filtering

---

# Data Model

The project uses a structured date relationship between the Date Table and the transaction dataset.


              DateTable
                  |
                  | Date
                  |
                  v
          Sales Transaction Data
# DAX Measures

Custom DAX measures were created to calculate the major business metrics used throughout the dashboard.

## 1. Total Revenue

Calculates the total revenue generated from all transactions.

```DAX
Total Revenue =
SUMX(
    Sheet1,
    Sheet1[Units Sold] * Sheet1[Price Per Unit]
)
2. Total Units Sold

Calculates the total number of mobile units sold.

Total Units Sold =
SUM(Sheet1[Units Sold])
3. Total Transactions

Counts the number of unique transactions.

Total Transactions =
DISTINCTCOUNT(Sheet1[Transaction ID])
4. Unique Customers

Calculates the number of unique customers in the dataset.

Unique Customers =
DISTINCTCOUNT(Sheet1[Customer Name])
5. Average Rating

Calculates the average customer rating.

Average Rating =
AVERAGE(Sheet1[Customer Ratings])
6. Average Selling Price

Calculates the weighted average selling price based on total revenue and total units sold.

Average Selling Price =
DIVIDE(
    [Total Revenue],
    [Total Units Sold]
)
7. Total Cities

Calculates the number of unique cities represented in the dataset.

Total Cities =
DISTINCTCOUNT(Sheet1[City])
Key Metrics Covered
Revenue Performance
Sales Volume
Transaction Activity
Customer Reach
Customer Satisfaction
Average Selling Price
Geographic Coverage
```
# Analytical Techniques

The dashboard uses multiple analytical approaches to move beyond basic visualization.

1. **KPI Analysis** — High-level performance monitoring
2. **Trend Analysis** — Time-based revenue patterns
3. **Comparative Analysis** — Comparison across brands and products
4. **Customer Segmentation** — Analysis using age groups
5. **Geographic Analysis** — Comparison across cities
6. **Brand × City Analysis** — Understanding brand performance by location
7. **Age Group × Brand Analysis** — Comparing customer segments and brands
8. **Revenue vs Units Analysis** — Comparing sales volume with revenue contribution
9. **Conditional Formatting** — Highlighting performance patterns in matrix visuals
10. **Interactive Filtering** — Exploring data dynamically across dashboard pages

---

# Interactive Features

The dashboard provides an interactive experience through:

1. **Year Slicers**
2. **Brand Slicers**
3. **City Slicers**
4. **Payment Method Slicers**
5. **KPI Cards**
6. **Interactive Charts**
7. **Cross-Filtering**
8. **Conditional Formatting**
9. **Time-Based Analysis**
10. **Multi-Page Dashboard Navigation**

Technology Stack :
Microsoft Power BI — Dashboard development and visualization
Power Query — Data cleaning and transformation
DAX — Business calculations and analytical measures
Microsoft Excel — Source transaction data
Data Modeling — Relationships and time-based analysis

# Skills Demonstrated

## Data & Analytics

- Business Intelligence
- Data Analytics
- Data Cleaning
- Data Transformation
- Data Modeling
- Customer Segmentation
- Trend Analysis
- Geographic Analysis

## Power BI

- Power Query
- DAX
- KPI Development
- Interactive Visualizations
- Slicers and Filters
- Conditional Formatting
- Dashboard Navigation
- Time-based Analysis

## Business Analysis

- Sales Performance Analysis
- Product Performance Analysis
- Brand Analysis
- Customer Behavior Analysis
- Geographic Market Analysis
- Business-focused Analytical Thinking


Project Outcome : 

The final solution converts raw transactional records into an interactive analytical environment where users can explore sales performance from multiple business perspectives.

Instead of presenting isolated charts, the dashboard connects:

Revenue
Products
Brands
Customers
Locations
Payment methods
Time

into a single analytical workflow.

The result is a structured Business Intelligence dashboard that makes complex transaction-level data easier to explore, compare, and understand.

Final Takeaway :

Every transaction contains a signal. The goal of Business Intelligence is to turn that signal into something a business can understand and act upon.This project demonstrates the complete journey from raw data to business insight — combining:
Data Preparation → Data Modeling → DAX → Visualization → Business Analysis
into a single Power BI solution.

