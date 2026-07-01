End-to-End E-commerce Data Engineering Pipeline
Project Overview

This project simulates a real-world data engineering workflow using the Olist Brazilian E-commerce dataset. The objective was to transform raw transactional data into an analytics-ready reporting layer using PostgreSQL and SQL best practices.

Instead of querying raw transactional tables directly, reusable SQL views were created to separate business logic from the source data. This approach mirrors how reporting layers are commonly designed in modern data warehouse environments.

Business Problem

An e-commerce company stores millions of transactional records inside PostgreSQL.

Business users need reliable datasets for reporting and analytics without querying raw operational tables.

The objective of this project was to build a reporting layer that delivers clean, consistent, and reusable datasets for downstream analytics.

Project Architecture

Kaggle Olist Dataset (CSV)

↓

PostgreSQL Raw Tables

↓

Data Validation & Quality Checks

↓

SQL Transformations

↓

Reporting Views

↓

Analytics-Ready Data

Dataset

Source: Olist Brazilian E-commerce Public Dataset (Kaggle)

Tables used:
Customers
Orders
Order Items
Products
Payments

Tech Stack
PostgreSQL
SQL
Git
GitHub
Database Design

The database was designed using relational modeling principles.

Relationships include:

Customers → Orders
Orders → Order Items
Products → Order Items
Orders → Payments

Primary and foreign keys were defined to maintain referential integrity.

Data Engineering Workflow

1. Database Design
Created relational tables
Selected appropriate data types
Defined primary keys

2. Data Ingestion
Imported CSV files into PostgreSQL
Verified row counts
Validated successful imports

3. Data Quality
Performed validation checks including:
Null value detection
Duplicate records
Missing foreign keys
Referential integrity

4. SQL Transformations
Business logic was implemented using:
JOINs
Aggregations
CASE statements
Common Table Expressions (CTEs)
Window Functions

5. Reporting Layer
Reusable SQL views were created for analytics, including:
vw_monthly_sales
vw_customer_revenue
vw_product_performance

These views simplify reporting while keeping business logic centralized.


Skills Demonstrated
Relational Database Design
PostgreSQL
SQL
Data Validation
Data Cleaning
Data Modeling
SQL Views
Window Functions
Reporting Layer Design
GitHub Project Documentation


Future Improvements
Automate ingestion using Python
Build ETL pipelines
Deploy PostgreSQL on AWS RDS
Containerize with Docker
Orchestrate workflows using Apache Airflow

Thank you for reviewing this project. Feedback and suggestions are always welcome.
