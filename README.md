# Enterprise Transaction & Fraud Analytics Platform

## Project Overview

This project demonstrates the design and implementation of an enterprise-grade Transaction & Fraud Analytics Platform using modern Data Engineering technologies.

The platform processes over 6 million financial transaction records and implements a Medallion Architecture (Bronze, Silver, and Gold layers) using Databricks, PySpark, SQL, and Delta Lake.

---

## Business Problem

Financial institutions process millions of transactions daily and require scalable data platforms to:

- Monitor transaction activity
- Detect fraudulent transactions
- Track transaction trends
- Generate business KPIs
- Support operational and analytical reporting

This project simulates a real-world enterprise data platform for transaction and fraud analytics.

---

## Dataset

Source Dataset:

PaySim Synthetic Financial Dataset

Dataset Characteristics:

- 6.3+ million transaction records
- Multiple transaction types
- Fraud indicators
- Account balance information
- Large-scale data suitable for Spark processing

---

## Technology Stack

- SQL
- PySpark
- Databricks
- Delta Lake
- GitHub

---

## Architecture

The project follows the Medallion Architecture pattern.

```text
Source CSV
    ↓
Bronze Layer
    ↓
Silver Layer
    ↓
Gold Layer
    ↓
Business Analytics
