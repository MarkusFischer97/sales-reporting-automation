# Sales Reporting Automation with Power BI

A portfolio project demonstrating how a manual, Excel-based sales reporting process can be transformed into a repeatable Power BI reporting workflow.

## Business Problem

A fictional mid-sized manufacturing company receives monthly sales data as Excel exports.

The previous reporting process requires manual work:

- collecting monthly Excel files
- combining and cleaning data
- enriching sales data with customer and product information
- calculating KPIs
- updating management reports

This makes the reporting process repetitive and increases the risk of inconsistent calculations and manual errors.

## Solution

The project transforms the process into a structured reporting workflow:

Excel files
→ Power Query
→ Data Model
→ DAX Measures
→ Power BI Dashboard

The goal is not to introduce unnecessary technology, but to use the appropriate tool for each part of the workflow.

## Dashboard

The management dashboard provides an overview of:

- Total Revenue
- Gross Profit
- Gross Margin
- Budget Revenue
- Revenue Variance
- Revenue development over time
- Actual vs. Budget
- Revenue by Region
- Top Customers

Interactive filters allow the user to analyze the results by:

- Year
- Month
- Region
- Product Category
- Customer Segment

## Data Model

The Power BI model follows a simple star-schema approach.

### Fact tables

- `FactSales`
- `Budget`

### Dimension tables

- `DimDate`
- `DimRegion`
- `DimCustomer`
- `DimProduct`

The shared dimensions allow sales and budget data to be analyzed consistently by time, region, customer and product.

## Data Transformation

Power Query is used to transform the raw Excel exports into analysis-ready tables.

The transformation layer handles typical issues found in recurring Excel-based reporting processes, such as:

- combining monthly files
- standardizing column names
- cleaning inconsistent values
- handling missing values
- removing duplicate records
- applying consistent data types

## Key Metrics

The report uses DAX measures for the main business KPIs, including:

- Total Revenue
- Total Cost
- Gross Profit
- Gross Margin %
- Order Count
- Average Order Value
- Budget Revenue
- Revenue Variance
- Revenue Variance %

Measures are used instead of hard-coded calculations so that the KPIs respond dynamically to report filters.

## Business Value

The resulting workflow demonstrates how a repetitive Excel-based reporting process can be turned into a more structured and reusable reporting solution.

Potential benefits include:

- less repetitive manual reporting work
- consistent KPI definitions
- easier Actual-vs-Budget analysis
- interactive management reporting
- easier analysis across regions, customers and products
- a repeatable monthly reporting workflow

This project is a synthetic portfolio demonstration and does not represent a real client implementation. Therefore, no specific time or cost savings are claimed.

## Technology

- Power BI
- Power Query / M
- DAX
- Excel
- Git / GitHub

## Project Structure

```text
sales-reporting-automation/
│
├── data/
│   └── raw/
│
├── powerbi/
│   ├── SalesReportingAutomation.pbip
│   ├── SalesReportingAutomation.Report/
│   └── SalesReportingAutomation.SemanticModel/
│
├── screenshots/
│
├── README.md
└── .gitignore


## Project Status

The first management dashboard page is implemented.

Future improvements may include:

- a detailed sales analysis page
- additional management KPIs
- further automation of the data ingestion process
- optional Python/SQL integration where it provides a meaningful business benefit