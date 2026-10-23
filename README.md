# Power BI Multi-Process Data Modelling

A Power BI semantic modelling project integrating sales, inventory, marketing, order fulfilment, and sales target data to support consistent business reporting and analytical decision-making.

## Project Overview

This project demonstrates the development of a multi-process semantic model using Power BI Desktop.

The objective is to organize business data into a structured dimensional model, establish relationships between fact and dimension tables, and create a foundation for accurate reporting across different business functions.

The project focuses on star schema design, relationship management, data modelling principles, and the use of a shared date dimension.

## Technologies & Skills

**Tools**
- Power BI Desktop
- Power Query
- DAX

**Technical Skills**
- Dimensional Data Modelling
- Star Schema Design
- Fact and Dimension Tables
- Data Relationships and Cardinality
- Active and Inactive Relationships
- Data Granularity
- Data Quality Review
- Semantic Model Design

## Data Model Architecture

![Power BI Data Model](screenshots/model-overview.png)

The semantic model consists of **14 tables**, organized into three categories.

### Fact Tables

| Table | Purpose |
|---|---|
| `fact_sales` | Stores sales transactions and related business measures |
| `fact_inventory` | Contains inventory-related data |
| `fact_campaign_spend` | Contains marketing campaign expenditure data |
| `fact_promotion_coverage` | Supports analysis of promotional activities |
| `fact_order_process` | Contains order processing and fulfilment information |
| `fact_sales_targets` | Stores sales targets for performance comparison |

### Dimension Tables

| Table | Purpose |
|---|---|
| `dim_customer` | Customer attributes for segmentation |
| `dim_product` | Product information and categories |
| `dim_geo` | Geographical attributes |
| `dim_date` | Shared calendar dimension for date-based analysis |
| `dim_campaign` | Marketing campaign attributes |
| `dim_order_flags` | Order-related classifications and indicators |

### Supporting Tables

| Table | Purpose |
|---|---|
| `_measures` | Dedicated table for organizing analytical measures |
| `security` | Supporting table for security-related modelling |

## Key Modelling Features

### 1. Dimensional Modelling

Organized business data into fact and dimension tables to separate measurable events from descriptive business attributes.

This structure supports filtering, aggregation, and analysis across multiple business areas.

### 2. Relationship Management

Configured relationships between fact and dimension tables to support data filtering and reporting.

The model includes one-to-many relationships and both active and inactive relationships.

### 3. Shared Date Dimension

Used a common date dimension to support time-based analysis across business processes.

The model includes multiple date fields, such as order dates, invoice dates, delivery dates, and payment dates.

### 4. Multiple Business Processes

Integrated datasets from different operational areas within one semantic model, providing a foundation for cross-functional reporting.

### 5. Centralized Measures

Included a dedicated `_measures` table to organize DAX calculations and support maintainable analytical reporting.

## Business Questions Supported

The model provides a foundation for investigating questions such as:

1. How does sales revenue vary by product, customer, geography, and time?
2. How do actual sales compare with sales targets?
3. What are the inventory trends across products and periods?
4. How does marketing expenditure vary across campaigns?
5. How long does it take to process, deliver, and receive payment for orders?
6. How can different operational datasets be combined to support business decisions?

These represent potential analytical use cases; not all have been implemented as report pages.

## Project Structure

```text
powerbi-multi-process-data-model/
│
├── README.md
├── model-documentation.md
├── data-modeling.pbix
│
└── screenshots/
    ├── model-overview.png
    ├── table-relationships.png
```

The Power BI project file contains the semantic model, while the screenshots provide a visual overview of its architecture.

For further technical details, see [Model Documentation](model-documentation.md).

## Future Enhancements

- [ ] Validate relationship cardinality and filter directions.
- [ ] Develop additional business-focused DAX measures.
- [ ] Build an order and payment performance dashboard.
- [ ] Validate analytical results against source data.
- [ ] Test and document row-level security, if configured.
- [ ] Develop interactive reporting dashboards.
- [ ] Document key analytical findings.

## Project Background

This project was completed as a practical learning exercise to strengthen my understanding of Power BI semantic modelling, dimensional architecture, and relationships across business datasets.
