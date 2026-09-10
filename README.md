# Sales Performance Dashboard

A Power BI dashboard for analyzing sales performance across regions, customer segments, and product categories with interactive filtering and key performance indicators.

---

## Overview

This portfolio project demonstrates the design and development of an interactive sales analytics dashboard in Power BI. The dashboard consolidates sales data into a single, filterable view with KPI cards and multiple visualizations for comprehensive sales analysis.

The dashboard provides visibility into:
- Sales trends over time (monthly)
- Regional performance comparison
- Product category performance
- Customer segment analysis
- Top-performing products
- Key business metrics (Sales, Orders, Customers, Quantity, AOV, Discount)

---

## Business Problem

This dashboard addresses the need to answer key business questions about sales performance:

- How do sales perform across different time periods?
- Which regions contribute the most to total sales?
- Which product categories generate the most revenue?
- How do different customer segments perform in terms of sales?
- Which products are the top performers?
- How do key metrics change when filtering by region, year, customer segment, or product category?

---

## Tools & Technologies

| Component | Technology |
|-----------|-----------|
| **BI Platform** | Power BI Desktop |
| **Data Transformation** | Power Query |
| **Calculations** | DAX (Data Analysis Expressions) |
| **Data Structure** | Star Schema (Dimensional Model) |
| **Visualizations** | Power BI Native Visuals |

---

## Data Preparation

The dataset underwent the following preparation steps using Power Query:

- **Duplicate Detection & Removal**: Identified and removed duplicate records
- **Missing Value Handling**: 
  - Found and handled 8 missing/null values in the Quantity field
  - Found and handled 10 blank WarehouseID entries
- **Header Promotion**: Promoted the first row as column headers
- **Data Type Validation**: Ensured correct data types for all columns

---

## Data Model

The dashboard uses a **star-schema dimensional data model** with a central fact table connected to multiple dimension tables:

### FactSales (Fact Table)
- Central table containing transactional sales data
- Connected to dimension tables via foreign keys
- Contains base measures: Sales Amount, Order Quantity, Discount

### Dimension Tables

| Table | Purpose |
|-------|---------|
| **dim_customer** | Customer information and attributes |
| **dim_product** | Product information and categorization |
| **dim_warehouse** | Warehouse/location information |
| **DimDate** | Calendar table for time-based analysis |

**Relationships**: Dimension tables connect to FactSales using CustomerID, ProductID, WarehouseID, and OrderDate, enabling multi-dimensional analysis.

---

## DAX Measures

The following DAX measures are used in the dashboard:

| Measure | Purpose |
|---------|---------|
| **Total Sales** | Sum of all sales revenue |
| **Total Orders** | Count of distinct orders |
| **Total Customers** | Count of unique customers |
| **Total Quantity** | Sum of units sold across all transactions |
| **Average Order Value** | Total Sales divided by Total Orders |
| **Total Discount** | Sum of discount amounts (calculated from sales amount and discount percentage) |

---

## Dashboard Features

### KPI Cards
Display key metrics at a glance:
- Total Sales
- Total Orders
- Total Customers
- Total Quantity
- Average Order Value
- Total Discount

### Interactive Slicers
Allow filtering across multiple dimensions:
- **Region Slicer**: Filter by geographic region
- **Year Slicer**: Filter by year
- **Segment Slicer**: Filter by customer segment
- **Category Slicer**: Filter by product category

All visualizations update dynamically based on slicer selections.

### Visualizations
- **Monthly Sales Trend**: Line chart showing sales performance over time
- **Sales by Region**: Horizontal bar chart ranking regions by sales
- **Sales by Category**: Horizontal bar chart showing category performance
- **Sales by Customer Segment**: Horizontal bar chart displaying segment contribution
- **Top 10 Products by Sales**: Horizontal bar chart highlighting top products

---

## Key Insights & Analytical Capabilities

The dashboard enables analysis of:

- **Monthly trends**: Observe sales patterns across different time periods
- **Regional performance**: Compare sales contribution and performance by region
- **Category performance**: Identify which product categories contribute most to revenue
- **Customer segment behavior**: Analyze sales distribution across different customer segments
- **Product performance**: Recognize top-performing products and their sales contribution
- **KPI monitoring**: Track overall sales volume, order count, customer base, and order value metrics
- **Filtered analysis**: Use interactive slicers to drill into specific regions, years, segments, or categories

---

## Potential Business Recommendations

Based on the dashboard's analytical capabilities, businesses can:

1. **Monitor Performance Trends**: Review monthly sales trends to identify periods of stronger or weaker performance
2. **Regional Analysis**: Compare regional performance to inform strategy and resource allocation decisions
3. **Category Focus**: Analyze product category performance to prioritize marketing and inventory efforts
4. **Segment Strategy**: Review customer segment performance to understand which segments drive the most sales
5. **Product Analysis**: Identify top-performing products and investigate what drives their success
6. **Discount Review**: Monitor discount amounts and their relationship to sales to inform pricing strategy
7. **Ongoing Monitoring**: Establish a regular review cadence using the interactive dashboard to support performance tracking

---

## Repository Structure

```
sales-performance-powerbi/
├── README.md
├── Sales_Performance_Dashboard.pbix
├── Sales dashboard.png
├── dashboard/
│   └── README.md
├── screenshots/
│   └── README.md
```

---

## How to Use

1. **Download** the `Sales_Performance_Dashboard.pbix` file from the repository root
2. **Open** the file in Power BI Desktop
3. **Interact with Slicers**: Use the Region, Year, Segment, and Category slicers to filter the data
4. **View KPIs**: Monitor the key performance indicators at the top of the dashboard
5. **Analyze Visualizations**: Review trends, comparisons, and top performers across all charts

The dashboard contains all necessary data and does not require external connections to function.

---

## Future Improvements

Potential enhancements to this dashboard could include:

- Additional visualizations for deeper analysis
- Drill-through pages for detailed product or customer-level insights
- Additional DAX measures for profitability or performance variance analysis
- Segmented views for specific business departments or teams
- Export functionality for report sharing

---

## Contact

For questions about this project or to discuss further, feel free to reach out.

---

**Built with Power BI | Star Schema Data Model | Interactive Analytics**
