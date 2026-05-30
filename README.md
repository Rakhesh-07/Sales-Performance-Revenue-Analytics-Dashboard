# Sales Performance & Revenue Analytics Dashboard

An interactive **Power BI sales analytics dashboard** built to analyze revenue, orders, average order value, product sales, customer behavior, monthly trends, and country-level performance from a structured Excel-based sales dataset.

## Project Overview

This project solves the problem of scattered sales data by converting raw Excel tables into a clean, interactive Power BI report. The dashboard helps users move from high-level business performance monitoring to deeper product, customer, country, and order-level analysis.

The report is designed for business users, analysts, and decision-makers who need to quickly understand sales performance, identify revenue drivers, compare monthly performance, and investigate detailed transactions without manually reviewing raw Excel data.

## Business Problem

Sales data is often stored across multiple tables and is difficult to analyze manually. This dashboard brings key business metrics into one interactive report, allowing users to:

- Track revenue, orders, average order value, and sold products.
- Compare current performance with previous-month values.
- Identify top-performing categories, products, customers, and countries.
- Analyze customer behavior and product-level contribution.
- Drill into order-level details for deeper investigation.
- Support faster and more data-driven business decisions.

## Tools Used

| Tool | Purpose |
|---|---|
| **Power BI** | Dashboard development, data modeling, visualization, and reporting |
| **Power Query** | Data cleaning, transformation, merging, and preparation |
| **DAX** | KPI measures, previous-month comparisons, growth metrics, and dynamic calculations |
| **Excel** | Source dataset containing structured sales, product, customer, date, and lookup tables |

## Dataset

The dashboard uses a sample business sales dataset from an Excel workbook named **SalesDashboardSampleData_2024.xlsx**.

### Tables Used

| Table | Rows | Description |
|---|---:|---|
| **Sales** | 21,931 | Main transaction table containing order-level sales data |
| **Products** | 7 | Product details including product name, category, price, and image-related fields |
| **Customers** | 500 | Customer details including names, countries, flags, and visit-related information |
| **Date** | 366 | Calendar table used for month-based filtering and time analysis |
| **Country Flag** | 4 | Lookup table used to display country flag visuals |
| **Products Img** | 3 | Supporting table used for product/category image visuals |

## Data Model

The dashboard follows a **star-schema style data model** with the **Sales** table as the central fact table.

### Fact Table

**Sales** contains transaction-level records such as:

- Order ID
- Date
- Customer ID
- Product ID
- Quantity
- Total Amount
- Seen Count / Product View Count

### Dimension and Lookup Tables

- **Products** connects to Sales through ProductID and supports analysis by product name, category, and price.
- **Customers** connects to Sales through CustomerID and supports customer-level and country-level analysis.
- **Date** connects to Sales through the Date field and supports month-based filtering and time intelligence.
- **Country Flag** connects through country-related fields and enhances geographic visuals.
- **Products Img** supports product/category image visuals.
- Supporting tables such as parameter, measure, and KPI definition tables are used for dynamic filtering, documentation, and DAX organization.

## Dashboard Pages

### 1. Overview Page

The Overview page provides a high-level view of sales performance through KPI cards and trend visuals. It helps users quickly monitor total revenue, orders, average order value, sold products, category contribution, customer behavior, and monthly revenue performance.

### 2. Performance Page

The Performance page allows users to compare performance across different business dimensions such as category, product, customer, and country. A dynamic filter selector helps switch the analysis view, making it easier to identify revenue drivers and compare business segments.

### 3. Details Page

The Details page provides order-level sales information for deeper analysis. Users can drill through from summary visuals and investigate specific transactions, products, customers, revenue, and sales patterns.

### 4. Info Page

The Info page documents the dashboard structure, KPI definitions, data model, data source, filters, interactions, navigation, and report refresh information. This improves usability and makes the report easier to understand for new users.

### 5. Hidden Tooltip Pages

The report includes hidden tooltip pages:

- **Cat TT**: Category tooltip page
- **Country TT**: Country tooltip page

These pages provide additional context without overcrowding the main dashboard pages.

## Key KPIs

The dashboard tracks the following KPIs:

- **Revenue**
- **Orders**
- **Average Order Value (AOV)**
- **Sold Products**
- **Customer Habits**
- **Best Performing Category**
- **Customer by Location**
- **Previous-Month Comparisons**
- **Revenue Contribution by Category, Product, Customer, and Country**

## Power Query Transformations

Power Query was used to clean and prepare the dataset before building the report. Key preparation steps included:

- Removed duplicate records.
- Changed data types for accurate analysis.
- Handled null values.
- Created calculated columns.
- Merged queries across related tables.
- Built a Date table for time-based reporting.
- Prepared lookup tables for country flags and product image visuals.

## DAX and Analytics

DAX was used to create custom measures for KPI tracking and business analysis, including:

- Total revenue calculations.
- Order count calculations.
- Average order value calculations.
- Sold product calculations.
- Previous-month value comparisons.
- Growth and performance comparison metrics.
- Dynamic KPI calculations.
- Revenue contribution analysis across categories, products, customers, and countries.

## Dashboard Features

This Power BI report includes several interactive features to improve usability and analysis:

- Synced month slicers across report pages.
- Category, product, customer, country, and customer segment slicers.
- Dynamic filter selector on the Performance page.
- Drillthrough from high-level visuals to order-level details.
- Hidden tooltip pages for category and country visuals.
- Page navigation buttons with custom icons.
- Bookmarks for interactive visual switching.
- Dynamic KPI cards and previous-month comparisons.
- Conditional formatting.
- Product images and country flag visuals.
- Clean card-based dashboard layout.
- Info page for report documentation and KPI explanations.

## Key Insights

Based on the dashboard analysis:

1. **Electronics** is the strongest revenue-driving category, contributing the highest share of total sales compared with Furniture and Home Appliance.
2. **Laptop** is the top-performing product by revenue, followed by Smartphone, showing that high-value electronics are the main sales drivers.
3. **March** is the best-performing month for revenue, while **September** shows the lowest monthly sales performance.
4. **Cote d'Ivoire** generates the highest country-level revenue, followed closely by Ghana and Togo, while Benin has the lowest revenue contribution.
5. Revenue is mainly concentrated in electronics products, indicating that product category performance has a stronger impact than country-level variation.

## Business Value

This dashboard helps users track sales performance in one interactive report instead of manually reviewing raw Excel data. It supports better decision-making by helping users identify top-performing products, strong revenue-driving categories, low-performing areas, customer trends, country-level sales patterns, and potential revenue opportunities.

By combining KPI cards, trend analysis, slicers, tooltips, bookmarks, drillthrough, and order-level details, the report allows users to move from summary-level insights to detailed business investigation in a structured and efficient way.

## Dashboard Preview

> Add the dashboard screenshots to a `screenshots` folder in your repository and update the image paths below if needed.

### Overview Page

![Overview Page](screenshots/overview.png)

### Performance Page

![Performance Page](screenshots/performance.png)

### Sales Details Page

![Sales Details Page](screenshots/details.png)

### Info Page

![Info Page](screenshots/info.png)

### Data Model

![Data Model](screenshots/data-model.png)

## Repository Structure

```text
Sales-Performance-Revenue-Analytics-Dashboard/
│
├── Sales_Dashboard.pbix
├── SalesDashboardSampleData_2024.xlsx
├── README.md
│
└── screenshots/
    ├── overview.png
    ├── performance.png
    ├── details.png
    ├── info.png
    └── data-model.png
```

## How to Use

1. Download or clone this repository.
2. Open **Sales_Dashboard.pbix** in Power BI Desktop.
3. Review the data model and Power Query transformations.
4. Use the slicers, filters, bookmarks, tooltips, and drillthrough features to explore sales performance.
5. Navigate between Overview, Performance, Details, and Info pages using the sidebar navigation.

## Future Enhancements

Potential improvements for future versions include:

- Adding sales forecasting for future revenue trends.
- Creating additional customer segmentation analysis.
- Adding profit and margin-based KPIs if cost data is available.
- Building product recommendation or cross-selling insights.
- Connecting the report to a live database instead of a static Excel file.
- Adding role-level security for different business users.

## Project Summary

The **Sales Performance & Revenue Analytics Dashboard** is an interactive Power BI project designed to analyze business sales performance across revenue, orders, AOV, product sales, customer behavior, and country-level trends. Using an Excel-based sales dataset, the project applies Power Query for data preparation, a star-schema model for structured analysis, and DAX measures for KPI reporting and performance comparisons. The final dashboard provides clear business insights through interactive visuals, slicers, drillthrough, tooltips, bookmarks, and detailed transaction-level analysis.

## Author

**Rakhesh Varshan Dhamodaran**  
Data Analyst / BI Analyst / Power BI Developer  

