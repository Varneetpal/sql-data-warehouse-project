# Data Warehouse and Analytics project

This project demonstrates a comprehensive data warehousing and analytics solution, from building a data warehousen to generating actionable insights. Designed as a portfolio project following the industry best practices in data engineering and data analytics.

**Project Overview**

This project involves:
1. **Data Architecture:** Designing a modern data warehouse using Medallion Architecture **Bronze**, **Silver**, and **Gold** layers.
2. **ETL Pipelines**: Extracting, transforming, and loading data from source systems into the warehouse.
3. **Data Modeling**: Developing fact and dimension tables optimized for analytical queries.
4. **Analytics & Reporting**: Creating SQL-based reports and dashboards for actionable insights.


**Project Requirements**

Building the Data Warehouse (Data Engineering)

**Objective**

Develop a modern data warehouse using SQL server to consolidte sales data, enabling analytical reporting and informed decision-making.

**Specifications**

- Data Sources: Import data from two source systems (ERP and CRM) provided as CSV files.
- Data Quality: Clean and resolve data quality issues prior to analysis.
- Integration: Combine both sources into a single, user-friendly data model designed for analytical queries.
- Scope: Focus on the latest dataset only; historization of data is not required.
- Documentation: Provide clear documentation of the data model to support both business stakeholders and analytics teams.


**Data Architecture**

The data architecture for this project follows Medallion Architecture Bronze, Silver, and Gold layers:
<img width="424" height="317" alt="image" src="https://github.com/user-attachments/assets/d7e3b402-0b28-4ae7-8ae3-991ccbcab3ec" />

1. Bronze Layer: Stores raw data as-is from the source systems. Data is integrated from CSV files into SQL server database.
2. Silver Layer: This layer includes data cleaning, standarization, and normalization processes to prepare data for analysis.
3. Gold Layer: Houses business-ready modeled into a star schema required for reporting and analytics.
