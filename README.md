
---

# Data Engineering Internship Learning Log

## Intern Information

**Name:** Pavan S
**Role:** Python Developer Intern
**Organization:** Datamatter Technologies
**Focus Area:** Data Migration & Data Engineering
**Start Date:** 12 March 2026

---

# Daily Learning Tracker

## Day 1 – Introduction to Data and Data Migration

**Date:** 10 March 2026

Today I started learning the basic concepts related to **data and data migration**. Data refers to information stored in digital form such as databases, Excel sheets, CSV files, APIs, or cloud storage. For example, a table containing names, emails, and phone numbers is considered data.

I learned that **data migration** is the process of moving data from one system to another. This is commonly done when companies move their data from older systems to newer platforms such as **Salesforce**.

Companies perform data migration for several reasons such as:

* Upgrading systems
* Moving infrastructure to the cloud
* Merging with other organizations
* Improving performance
* Replacing outdated applications with new ones

Another important concept I learned is **ETL**, which stands for:

* **Extract**
* **Transform**
* **Load**

This is the common workflow used in **data migration and data pipelines**.

### ETL Process

**Extract**
Data is collected from the source system such as databases, Excel files, APIs, or CRM systems.

**Transform**
The data is cleaned and prepared by removing duplicates, fixing incorrect formats, correcting missing values, and standardizing the data.

**Load**
The cleaned data is inserted into the target system such as a database, data warehouse, or Salesforce.

I also learned about **Salesforce**, which is a **cloud-based CRM platform** used by companies to manage customers, leads, sales opportunities, and support cases.

**CRM** stands for **Customer Relationship Management**, which is a system used to store and manage customer information and interactions.

---

### Skills / Understanding Gained

* Basic understanding of data storage formats
* Understanding how data moves between systems
* Introduction to Salesforce and CRM systems

---

# Day 2 – Salesforce Data Migration Concepts and SQL Transformations

**Date:** 13 March 2026

Today I continued learning about **Salesforce data migration concepts** and tools used for moving data into Salesforce systems.

Salesforce stores business information in **objects** such as:

* Accounts
* Contacts
* Leads
* Opportunities
* Cases

These objects work similarly to **tables in a database** and help companies manage customers, sales processes, and support activities.

I learned that during migration it is important to perform **field mapping**, which means matching fields from the source system to the correct fields in Salesforce.

Example:

```
Excel Column → Salesforce Field
Name → First Name
Email → Email
Company → Account
```

---

## Salesforce Migration Tools

Common tools used for Salesforce data migration such as:

* **Salesforce Data Import Wizard**
* **Salesforce Data Loader**
* **ETL Tools**

  * MuleSoft
  * Talend
  * Informatica

**Data Loader** is commonly used to:

* Import data
* Export data
* Update records
* Delete records

It usually works with **CSV files**, which store tabular data in rows and columns.

---

## Batch vs Real-Time Data Migration

### Batch Migration

Data is moved in groups at scheduled times.

Example:

* Daily uploads
* Nightly data transfers

### Real-Time Integration

Data moves immediately when an event occurs.

Example:

A user submits a website form → A lead is instantly created in Salesforce.

---

---

## Challenges in Data Migration

Common challenges include:

* Duplicate records
* Incorrect data formats
* Missing data
* Incorrect field mappings

I also understood that **migration order is important** because Salesforce objects have relationships.

Example:

```
Account → Contact
```

Accounts must be created first because **contacts belong to accounts**.

---

---

# SQL Concepts Learned

Along with Salesforce migration concepts, I also studied **SQL techniques used for data transformations and calculations**.

---

## 1. WITH Clause (Common Table Expression)

SQL cannot reference a column alias in the same `SELECT` statement where it is defined.

The **WITH clause** helps break complex queries into smaller steps.

Example:

```sql
WITH step_1 AS (
    SELECT *,
           (col_a * col_b) - col_c AS intermediate
    FROM table_name
)
SELECT *,
       SAFE_DIVIDE(100 * intermediate, col_a * col_b) AS ratio
FROM step_1;
```

---

## 2. Scalar Subqueries

Aggregate functions such as `SUM()` combine rows and return a single value.

A **scalar subquery** calculates the aggregate separately and returns one value that each row can use.

Example:

```sql
SELECT *,
       col_a - (SELECT AGG_FUNC(col_a) FROM table_name) AS result
FROM table_name;
```

---

## 3. Percent of Total Calculation

This technique shows how much each value contributes to the total.

Example:

```sql
SELECT *,
       100 * col_a / (SELECT SUM(col_a) FROM table_name) AS col_a_pot
FROM table_name;
```

---

## 4. Rounding Functions

The `ROUND()` function controls decimal places in calculations.

Example:

```sql
SELECT *,
       ROUND(100 * col_a / col_b, 2) AS percentage
FROM table_name;
```

This improves readability of numerical results.

---

# Key Concepts Learned

* Salesforce Objects
* Field Mapping
* Data Loader
* CSV Files
* Batch Migration
* Real-Time Integration
* Migration Challenges
* WITH Clause (CTE)
* Scalar Subqueries
* Percent of Total Calculations
* Rounding Functions in SQL
* Data Transformation Using SQL

---
