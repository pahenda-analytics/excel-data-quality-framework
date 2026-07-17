# Project 1 – Excel Data Cleaning & Validation
     
          Raw CSV
             │
             ▼
    Data Quality Audit
             │
             ▼
   Power Query Cleaning
             │
             ▼
   Feature Engineering
             │
             ▼
   Validation & QA
             │
             ▼
   Analysis-Ready Dataset
             │
             ▼
      Power BI Dashboard

## Overview

This project demonstrates an end-to-end data cleaning, validation and reporting workflow using Microsoft Excel Power Query. The objective was to transform a large retail e-commerce dataset into an analysis-ready dataset while documenting every stage of the cleaning process through a structured data audit.

Unlike a simple cleaning exercise, this project focuses on preserving business integrity by validating data quality issues before applying transformations and verifying that business metrics remain consistent after cleaning.

The cleaned dataset was then exported to Power BI for dashboard development in Project 2.

---

## Project Objectives

* Import and profile a large retail transaction dataset (743,486 records)
* Perform structured data quality assessment
* Clean and standardise data using Power Query
* Preserve legitimate business transactions while resolving data quality issues
* Engineer additional analytical fields
* Produce a fully validated, analysis-ready dataset
* Document the transformation process through a reusable data audit framework

---

## Dataset

**Dataset:** E-Commerce Sales, Customer & Churn (2009–2011)

The dataset contains transactional sales data together with customer demographics, marketing information and profitability measures between 2009 and 2011.

Key fields include:

* Invoice
* Customer ID
* Stock Code
* Product Description
* Quantity
* Revenue
* Profit
* Country
* Customer Demographics
* Marketing Channel

---

## Data Quality Assessment

Before any transformations were applied, the raw dataset was profiled to assess overall data quality.

The audit examined:

* Dataset dimensions
* Date range
* Missing values
* Duplicate records
* Unique customers
* Unique products
* Revenue integrity
* Profit integrity
* Returns
* Customer identifiers

A reusable audit framework was created to compare raw and cleaned datasets and verify that transformations did not unintentionally alter business metrics.

---

## Data Cleaning Process

Power Query was used to perform all transformations.

Cleaning steps included:

* Importing and assigning appropriate data types
* Removing completely blank records
* Removing exact duplicate rows
* Trimming leading and trailing whitespace
* Removing hidden and non-printable characters
* Standardising text fields
* Validating numeric fields
* Preserving negative revenue and profit values representing product returns
* Preserving transactions with missing Customer IDs after determining these represented legitimate guest purchases rather than invalid records

---

## Feature Engineering

Additional analytical fields were created to improve reporting and downstream analysis:

* Revenue Band
* Customer Type (Registered / Guest)
* Return Flag
* Invoice Month
* Invoice Year

These derived fields simplify filtering, segmentation and reporting within Power BI.

---

## Data Validation

Following transformation, the cleaned dataset was compared against the raw dataset using a structured validation process.

Validation checks included:

* Row count reconciliation
* Column count reconciliation
* Date range validation
* Duplicate invoice assessment
* Missing value analysis
* Revenue reconciliation
* Profit reconciliation
* Return transaction validation
* Customer classification validation

This process confirmed that business-critical metrics were preserved while improving overall data quality.

---

## Key Findings

The audit identified several important business observations:

* Transactions containing missing Customer IDs represented legitimate guest purchases rather than invalid data.
* Negative revenue and profit values represented customer returns and were intentionally retained.
* No material transaction records required removal after business validation.
* Data quality improvements were achieved through standardisation and feature engineering rather than deleting valid business records.

---

## Deliverables

The repository contains:

```
project-01-excel-data-cleaning/
│
├── data/
│   ├── raw_ecommerce_data.csv
│   └── cleaned_ecommerce_data.xlsx
│
├── excel/
│   └── Excel_Data_Cleaning_Workbook.xlsx
│
├── powerbi/
│   └── Project1_Dashboard.pbix
│
├── screenshots/
│
├── README.md
```

The Excel workbook includes:

* README worksheet
* Raw data sample
* Data Audit
* Cleaned dataset
* Power Query transformations

---

## Skills Demonstrated

### Microsoft Excel

* Structured Tables
* Data Validation
* Named Ranges
* Audit Reporting

### Power Query

* ETL workflow
* Data profiling
* Data cleansing
* Feature engineering
* Data validation
* Query dependency management

### Data Quality

* Missing value assessment
* Duplicate detection
* Business rule validation
* Reconciliation of financial metrics
* Data integrity checks

### Business Intelligence

* Preparing analysis-ready datasets
* Designing reusable audit frameworks
* Documenting transformation logic
* Supporting downstream Power BI reporting

---

## Project Outcome

This project established a repeatable Excel-based ETL and data validation framework that can be applied to future datasets. Rather than focusing solely on cleaning data, the project demonstrates an analytical approach to understanding business context, preserving valid transactions and validating that transformations maintain the integrity of key business metrics.

The cleaned dataset produced here forms the foundation for **Project 2 – SQL Sales Analysis**, where the same data is transformed using SQL and visualised in Power BI.
