# Inventory Management Data Pipeline

## Overview

This project is an end-to-end Inventory Management Data Pipeline built using Databricks Lakehouse architecture. The pipeline processes inventory data from multiple operational systems in both real-time and batch modes using PySpark, Delta Lake, and Medallion Architecture.

The system provides:

* Real-time inventory visibility
* Inventory analytics and KPI monitoring
* Low stock alert generation
* Historical inventory tracking
* Scalable and fault-tolerant data processing

---

# Tech Stack

* Databricks
* PySpark
* Delta Lake
* AWS S3
* Delta Live Tables (DLT)
* Unity Catalog
* Structured Streaming

---

# Architecture

The project follows Medallion Architecture:

## Bronze Layer

* Stores raw inventory events
* Supports schema evolution
* Append-only Delta tables
* Retains ingestion metadata

## Silver Layer

* Cleans and validates data
* Removes duplicate records
* Applies business rules
* Handles late-arriving events

## Gold Layer

* Creates business KPIs
* Inventory balance tracking
* Daily inventory snapshots
* Low stock alerts
* Historical trend analysis

---

# Data Flow

Operational Systems (ERP / POS / WMS / IoT)
↓
Streaming & Batch Ingestion
↓
Bronze Layer
↓
Silver Layer
↓
Gold Layer
↓
Dashboards & Analytics

---

# Key Features

* Real-time and batch data ingestion
* Exactly-once processing
* Fault tolerance using checkpoints
* Delta Lake ACID transactions
* Time travel and audit tracking
* Inventory KPI generation
* Near real-time stock monitoring
* Scalable Spark processing

---

# KPIs Generated

* Current Inventory Balance
* Daily Inventory Snapshot
* Low Stock Alerts
* Historical Inventory Trends
* Inventory Movement Analysis

---

---

# Sample Pipeline Features

## Data Validation

* Quantity > 0 validation
* Duplicate removal using event_id
* Schema consistency checks

## Security & Governance

* Unity Catalog integration
* Role-based access control
* Audit tracking

---

# Future Enhancements

* Demand Forecasting
* Safety Stock Optimization
* SCD Type-2 Tracking
* Automated Data Quality Scoring

---

# Conclusion

This project demonstrates how modern data engineering technologies like Databricks, PySpark, Delta Lake, and Medallion Architecture can be used to build scalable, reliable, and real-time inventory analytics pipelines for enterprise-level inventory management systems.
