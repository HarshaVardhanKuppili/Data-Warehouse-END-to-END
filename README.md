# Data-Warehouse-END-to-END
📦 Data Warehouse Project (PostgreSQL + Medallion Architecture)

This project demonstrates an end-to-end data warehousing pipeline using PostgreSQL, following the Medallion Architecture (Bronze → Silver → Gold).
It includes raw data ingestion, data cleaning, dimensional modelling, and creation of analytics-ready fact & dimension views used for Power BI dashboards.

🚀 Project Overview

I designed a PostgreSQL-based data warehouse that integrates CRM and ERP data covering customers, sales, products, categories, and locations.
The warehouse is structured in three layers, each with its own purpose and transformation logic:

🔹 Bronze Layer – Raw Ingestion

Created bronze schema with staging tables for CRM and ERP sources.

Loaded CSV data using PostgreSQL COPY commands.

Ensured repeatable ingestion using TRUNCATE for clean reloads.

🔸 Silver Layer – Cleansing & Standardisation

Applied data quality rules and transformations:

Normalised text fields using TRIM, UPPER, and COALESCE.

Removed duplicate customer records using window functions:

ROW_NUMBER()

RANK()

Standardised gender and marital status using CASE logic.

Ensured consistent date formats and numeric types.

Joined CRM + ERP tables to enrich customer and product datasets.

🟡 Gold Layer – Dimensional Modelling

Created analytics-ready views following a star schema:

gold.dim_customers – Cleaned & enriched customer dimension

gold.dim_products – CRM product attributes + ERP category hierarchy

gold.fact_sales – Fact view with order, product, customer, dates, quantity, and revenue

These views power downstream dashboards such as:

Sales Analysis

Product Performance

Customer Segmentation

Category Profitability

🧠 Key SQL Techniques Used
Data Definition & Structuring

CREATE SCHEMA, CREATE TABLE, DROP TABLE, CREATE VIEW

Proper layering of Bronze → Silver → Gold

Data Ingestion

PostgreSQL COPY … FROM for fast bulk loading

Data Cleaning

TRIM(), UPPER(), COALESCE()

CASE WHEN mappings for business rules

Date standardisation and type corrections

Window Functions

ROW_NUMBER() for latest-record selection

RANK() for de-duplication and SCD-style logic

Joins & Modelling

LEFT JOIN to build dimensions

Merging CRM + ERP sources

Fact/dimension separation aligned with star schema design

Data Quality Validation

Duplicate key checks (GROUP BY … HAVING COUNT(*) > 1)

Range checks (MIN() / MAX())

📊 Final Output

Clean, reliable fact-sales model for reporting

Customer and product dimensions enriched from multiple systems

A complete SQL-driven pipeline, ready for BI tools such as Power BI, Tableau, and Looker
