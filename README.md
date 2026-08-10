# Data Warehouse and Analytics Project

This project demonstrates a comprehensive data warehousing and analytics solution, from building a data warehouse to generating actionable insights. It is designed as a portfolio project that follows industry best practices in data engineering and data analytics.

## Project Overview

This project involves:

1. **Data Architecture:** Designing a modern data warehouse using the **Medallion Architecture**, consisting of **Bronze**, **Silver**, and **Gold** layers.
2. **ETL Pipelines:** Extracting, transforming, and loading data from source systems into the data warehouse.
3. **Data Modeling:** Developing fact and dimension tables optimized for analytical queries.
4. **Analytics & Reporting:** Creating SQL-based reports and dashboards to generate actionable insights.

## Project Requirements

### Building the Data Warehouse (Data Engineering)

#### Objective

Develop a modern data warehouse using **SQL Server** to consolidate sales data, enabling analytical reporting and informed decision-making.

#### Specifications

* **Data Sources:** Import data from two source systems (**ERP** and **CRM**) provided as CSV files.
* **Data Quality:** Clean and resolve data quality issues before performing analysis.
* **Integration:** Combine data from both sources into a single, user-friendly data model designed for analytical queries.
* **Scope:** Focus on the latest dataset only; data historization is not required.
* **Documentation:** Provide clear documentation of the data model to support both business stakeholders and analytics teams.

## Data Architecture

The data architecture for this project follows the **Medallion Architecture**, consisting of three layers: **Bronze**, **Silver**, and **Gold**.
<img width="424" height="317" alt="image" src="https://github.com/user-attachments/assets/45628c07-041a-4049-97ba-9e63006bf30c" />


### 1. Bronze Layer

The Bronze Layer stores raw data as-is from the source systems. Data is ingested from CSV files into SQL Server with minimal transformation.

### 2. Silver Layer

The Silver Layer focuses on data cleaning, standardization, and normalization. This layer prepares the data for analysis by resolving data quality issues and applying necessary transformations.

### 3. Gold Layer

The Gold Layer contains business-ready data modeled using a **star schema**. It provides optimized, structured data for reporting, analytics, and dashboard development.
