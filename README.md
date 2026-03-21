
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

# Key Concepts Learned

* Salesforce Objects
* Field Mapping
* Data Loader
* CSV Files
* Batch Migration
* Real-Time Integration
* Migration Challenges

---

# Day 3 – Datamatter Gravity 

## 1. What is Datamatter Gravity?

Datamatter Gravity is a **data migration platform developed by Datamatter Technologies**.
It is used to move data from **source systems (ERP, databases, files, CRM)** to **target systems like Salesforce or cloud platforms**.

Example migration flow:

```
Source System
     ↓
Datamatter Gravity
     ↓
Salesforce / Cloud Database
```

Gravity automates the migration process and reduces manual work such as scripting, data cleaning, and validation.

---

# 2. Problems in Data Migration

Common challenges in migration:

* Different systems store data differently
* Field names do not match
* Data quality issues (duplicates, missing values)
* Complex relationships between tables
* Large datasets

Gravity solves these problems using automation tools.

---

# 3. Key Capabilities of Gravity

### Intelligent Data Processing

Gravity helps prepare data before migration.

**AI-powered mapping**

* Automatically suggests mapping between source fields and target fields.

Example:

| Source     | Target     |
| ---------- | ---------- |
| cust_name  | First Name |
| cust_email | Email      |

---

### Data Quality Management

Gravity helps clean and standardize data before migration.

Examples of fixes:

* remove duplicate records
* fix incorrect formatting
* validate required fields
* normalize values

---

### Data Transformation

Transforms source data to match target structure.

Example:

```
FullName → First Name + Last Name
```

---

# 4. Migration Lifecycle (ETL)

Gravity manages the full **ETL process**.

**Extract**

* Data is extracted from source systems such as databases, ERP systems, or files.

**Transform**

* Data is cleaned, formatted, and converted to match the target system.

**Load**

* Processed data is loaded into the target system such as Salesforce.

**Validate**

* Ensures data accuracy and integrity after migration.

---

# 5. Enterprise Features

### Environment Management

Migration is tested across different environments:

```
DEV → QA → UAT → PROD
```

---

### Pipeline Orchestration

Migration steps are organized as a **pipeline workflow**.

Example pipeline:

```
Extract → Clean → Transform → Map → Validate → Load
```

---

### Audit Trail

Gravity records migration activities such as:

* migration start
* records processed
* errors detected
* migration completion

---

### Error Handling

Gravity detects and manages migration errors such as:

* missing fields
* invalid formats
* relationship issues

Failed records can be reviewed and reprocessed.

---

# 6. Core Components

### Migration Workspace

Central interface used to manage migration projects.

---

### Pipeline Tabs

Each tab represents a stage of migration.

Important tabs:

* **Summary** – project overview and files
* **Extract** – explore source data
* **Relationship** – manage dependencies between objects
* **Filter** – select required data
* **Cleanup** – fix data quality issues
* **Transform** – modify data format
* **Mapping** – map source fields to target fields
* **Validation** – check migration readiness
* **Load** – execute migration
* **Error Handling** – review and fix failed records
* **Pipeline** – manage overall migration workflow

---

# 7. Supported Systems

**Source systems**

* ERP systems
* CRM platforms
* Databases (SQL Server, Oracle, MySQL, PostgreSQL)
* File systems (CSV, Excel, XML)

**Target systems**

* Salesforce
* Microsoft Dynamics
* Cloud databases
* Data warehouses
* Custom applications via APIs

---

# 8. Typical Migration Workflow

```
Source System
     ↓
Extract Data
     ↓
Clean / Transform Data
     ↓
Field Mapping
     ↓
Validation
     ↓
Load to Target System
```

---

# Concepts Learned Today

* Datamatter Gravity platform
* Data migration challenges
* AI-powered field mapping
* Data quality management
* Data transformation
* ETL lifecycle (Extract, Transform, Load, Validate)
* Migration pipelines
* Environment management (DEV, QA, UAT, PROD)
* Audit trail and error handling
* Migration workspace
* Pipeline tabs and their functions
* Supported source and target systems
* Typical data migration workflow

---

# Internship Diary – Day 4

## Objective
The objective of the fourth day was to migrate **Customer object data** from the source dataset to Salesforce using the Datamatter Gravity platform and understand the mapping process between source fields and Salesforce fields.

---

## Work Done

### 1. Customer Data Migration Attempt
On this day, I worked on migrating the **Customer object dataset** into Salesforce. The migration pipeline included reviewing metadata, transformation rules, and especially the **mapping stage**, where each source field must be mapped to a corresponding Salesforce field.

---

### 2. Issue with Field Mapping
During the mapping process, we encountered a problem where some fields were being mapped incorrectly. The system automatically suggested mappings that linked certain source fields to unrelated Salesforce fields. 

After analyzing the issue, we identified that this was actually a **bug in the mapping suggestion system**, which was incorrectly recommending target fields for some attributes.

This required manually reviewing and correcting the field mappings.

---

### 3. Mistake Identified During Migration
Another issue occurred due to a mistake from my side. I had included the **customer_id** field from the source dataset in the migration mapping.

However, Salesforce automatically generates a **unique system ID** for each record when data is inserted. Because of this, the `customer_id` field should not be migrated as a system identifier.

Including this field caused confusion during the migration process. Once we understood this behavior, we removed the `customer_id` field from the mapping configuration.

---

## Key Learnings

- Salesforce automatically generates record **IDs**, so they should not be migrated from external datasets.
- Careful review of **field mapping** is necessary before executing data migration.
- Automated mapping suggestions may not always be correct and should be validated manually.
- Understanding the **target system’s data model** is important for successful data migration.

---

## Outcome
By the end of the day, the issue with incorrect mapping was identified and the migration configuration was updated by removing the unnecessary `customer_id` field. This helped improve my understanding of how Salesforce handles record identifiers and how to properly configure migration pipelines.

---
# Internship Diary – Day 5

## Objective
The objective of the fifth day was to extend the migration process by attempting to migrate another object, **Order**, into Salesforce using the Datamatter Gravity platform.

---

## Work Done

### 1. Attempt to Add Order Object
On this day, I tried to configure and migrate a new object called **Order** to Salesforce. The goal was to understand how multiple objects can be migrated and how relationships between objects can be handled during migration.

---

### 2. Authentication Error During Connection
While attempting to connect Datamatter Gravity with Salesforce, I encountered an error during the connection process:
- Error Code: 424 (Authentication Failed)

This error prevented the system from establishing communication with Salesforce, and therefore the migration process could not proceed further.

---

### 3. Troubleshooting Steps
Initially, I was using **Amit Sir’s Salesforce credentials** to perform the connection. When the authentication issue occurred, I tried several troubleshooting steps.

First, I attempted to create my **own Salesforce account** and tried connecting again using my credentials. However, the same authentication error still occurred.

To resolve this issue, I discussed the problem with **Abhishek Sir and Vaishnavi Ma'am**. They suggested several modifications during the Salesforce setup process, including reviewing the connected app configuration, OAuth settings, and authentication parameters.

Following their suggestions, I carefully rechecked the setup and attempted the connection again.

---

### 4. Additional Troubleshooting
Even after implementing the suggestions from **Abhishek Sir**, I continued troubleshooting the issue by reviewing documentation and also consulting **ChatGPT** for possible configuration fixes.

Despite trying multiple solutions throughout the day, the authentication error persisted and the connection could not be successfully established.

---

## Key Learnings

- Understood how **Salesforce setup and connected app configuration** works.
- Learned about **OAuth authentication and API connection setup** in Salesforce.
- Gained practical experience in troubleshooting **authentication and integration errors**.
- Became more familiar with the **Salesforce setup environment and configuration process**.

---

## Outcome
Although the migration was not successfully completed due to the authentication error (424), the day was productive in terms of learning. I gained a better understanding of Salesforce setup.

---

# Internship Diary – Day 6

## Objective
The objective of the sixth day was to resolve the authentication issue encountered while connecting Datamatter Gravity with Salesforce and continue the work on migrating the **Order object**.

---

## Work Done

### 1. Authentication Error (Error 424)
At the beginning of the day, I was still facing the same authentication problem while connecting the system. The error message displayed was:
- Error 424 – Authentication Failed

This prevented Datamatter Gravity from establishing a connection with Salesforce.

---

### 2. Troubleshooting with Abhishek Sir
To resolve this issue, I discussed the problem with **Abhishek Sir**. He carefully analyzed the configuration and helped troubleshoot the issue step by step. 

Before this discussion, I had created an **External Client App** in Salesforce. However, it turned out that for this integration I actually needed to create a **Connected App** instead.

Following this realization, I created the Connected App using the correct path in Salesforce:
Setup → Connected Apps → Manage Connected Apps → New Connected App

After configuring the Connected App, I attempted the connection again, but the same authentication error was still occurring.

---

### 3. Identifying the Missing Configuration
Based on Abhishek Sir’s suggestion, I then connected with **Ankit Sir** to further analyze the problem. He reviewed the Salesforce setup configuration and identified the exact issue.

The missing configuration was in the Salesforce settings:

After configuring the Connected App, I attempted the connection again, but the same authentication error was still occurring.

---

### 4. Progress on Order Object Migration
Once the connection issue was resolved, I proceeded with the next task of adding another object for migration, which was the **Order object**. 

During this stage, I configured the object and worked on the **field mapping process**. The fields were mapped correctly today, and the migration setup for the Order object is currently **in progress**.

---

## Key Learnings

- Learned the difference between **External Client App and Connected App** in Salesforce integrations.
- Understood how **OAuth authentication settings** impact API integrations.
- Identified that enabling **OAuth Username-Password Flow** is necessary for certain authentication methods.
- Gained practical experience troubleshooting **integration and authentication errors** in Salesforce.
- Improved understanding of **object mapping during data migration**.

---

## Outcome
By the end of the day, the authentication issue that had been occurring for multiple days was successfully resolved. I was able to establish a connection with Salesforce and proceed with configuring the **Order object migration**, which is currently ongoing.

---

# 📘 Internship Learning – Day 7

## 🎯 Objective

Today, I worked on migrating multiple objects and understanding relationships between them in Salesforce using Datamatter.

---

## 🔧 Work Done

Today, I experimented with different objects such as **Customer (Contact)** and **Order** to understand how data migration works with relationships.

While working on this, I faced multiple errors during the process:

* Incorrect field mapping (AI mapped fields wrongly like mapping external ID to Salesforce ID)
* Metadata issues (fields not visible until refresh)
* Data format issues (date vs datetime mismatch)

To resolve these issues, I learned to:
* Create **custom fields** in Salesforce (like `Customer_External_Id__c`)
* Mark fields as **External ID** for proper mapping
* Refresh metadata to sync fields

---

## ❗ Major Issue Faced

While trying to migrate the **orders.csv (Order object)**, I encountered the error:

```text
REQUIRED_FIELD_MISSING: Select an account
```

---

## 🔍 Root Cause Analysis

After analyzing the issue, I understood the actual reason:

👉 Salesforce requires **Account as a mandatory parent object**

* A **Contact (Customer)** must be linked to an Account
* An **Order** must also be linked to an Account

---

## 🧠 Key Concept Learned

```text
Salesforce Relationship Structure:
Account → Contact (Customer) → Order
```

👉 This means:

* We cannot directly create Orders without Account
* Proper **data hierarchy and order of migration** is required

---

## 🚫 Mistake Made

* Tried migrating **Order object without proper Account linkage**
* Did not follow correct migration sequence

---

## ✅ Correct Approach

```text
1. Create Account data  
2. Load Account into Salesforce  
3. Load Customer (Contact) linked to Account  
4. Load Orders linked to Customer (and Account)
```

---

## 📚 Key Learnings

* Salesforce enforces **strict parent-child relationships**
* **Account is mandatory** for Contact and Order
* External IDs are essential for linking data
* Migration must follow **correct sequence**
* Errors like `REQUIRED_FIELD_MISSING` indicate missing relationships
* Proper data modeling is crucial before migration

---

## 🚀 Outcome

Although I was not able to successfully complete the Order migration today, I gained a clear understanding of:

* Salesforce data hierarchy
* Importance of relationships
* Correct migration order
* Handling real-world migration errors

---


