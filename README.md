# UFO Sightings Data Warehouse Project

## Overview

This project aims to implement a simple medallion-style data pipeline for UFO sightings data using **PySpark**, **Spark SQL**, and **Delta Lake**.

The repository is organized to support a layered data architecture:

- **Setup layer**: prepares the catalog and database
- **Bronze layer**: ingests raw source data with minimal modification
- **Silver layer**: applies cleansing, standardization, enrichment, and business-ready transformations

The goal of the project is to create a clean analytical dataset that can be queried directly or used to feed a dashboard.

---

## Project Objectives

This repository demonstrates how to:

- Create a data warehouse database for the project
- Ingest raw UFO sightings data from Kaggle into Delta tables
- Preserve raw data integrity in the Bronze layer
- Build a transformed Silver layer for analytics
- Support dashboard reporting with SQL queries
- Use MERGE logic for incremental loads and updates

---

## Business Questions Proposed

1) Which countries and regions have the highest sighting concentration?
2)  How has sighting frequency evolved over the decades?
3) What are the most common UFO shapes — do they vary by region?
4) At what time of day do most sightings occur — does this differ by season?
5) What is the average and maximum encounter duration by shape and country?
6) Is there a correlation between season and sighting frequency — USA vs World?
7) Which year/month combination had the most sightings worldwide?

## Repository Structure

```text
.
├── 00_setup/
│   └── 00_setup.sql or 00_setup notebook
├── 01_bronze/
│   └── bronze_ufo_sightings.py
├── 02_silver/
│   └── silver_ufo_sightings.py
├── sql/
│   └── dashboard_queries.sql
├── README.md
