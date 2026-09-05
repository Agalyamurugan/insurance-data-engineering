# insurance-data-engineering

# Insurance OLTP to Databricks OLAP Data Engineering

## 📌 Project Overview

The **Insurance Data Engineering Project** is an end-to-end data engineering solution that transforms operational insurance data from an **AWS RDS MySQL OLTP database** into clean, structured, and analytics-ready data using **Databricks and PySpark**.

The project follows a **Medallion Architecture** consisting of:

- 🥉 Bronze Layer – Raw Data
- 🥈 Silver Layer – Cleaned and Standardized Data
- 🥇 Gold Layer – Business-Ready Analytical Data

The final data can be used for insurance analytics, reporting, dashboards, and business decision-making.

---

## 🎯 Project Objective

The main objective of this project is to build an end-to-end insurance data engineering pipeline that converts raw OLTP data into clean and business-ready analytical data.

The project helps the insurance company analyze:

- Customer behavior
- Policy performance
- Premium payments
- Claims
- Agent performance
- Policy renewals
- Revenue and profitability
- Historical business trends

---

## 🏢 Business Problem

Insurance companies generate large amounts of operational data from customers, policies, premium payments, claims, agents, and renewals.

The OLTP database is designed mainly for daily operational activities. Directly running complex analytical queries on the OLTP database can:

- Affect operational performance
- Require complex joins
- Make historical analysis difficult
- Increase query processing time
- Make reporting and analytics difficult

Therefore, a separate analytical data platform is required.

This project builds a scalable analytical pipeline using **Databricks**.

---

## 🏗️ Project Architecture

```text
                 AWS RDS MySQL
                     │
                     │ JDBC
                     ▼
              ┌───────────────┐
              │ Bronze Layer  │
              │   Raw Data    │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Silver Layer  │
              │ Cleaned Data  │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │  Gold Layer   │
              │ Business Data │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │   Analytics   │
              │   Dashboard   │
              └───────────────┘
