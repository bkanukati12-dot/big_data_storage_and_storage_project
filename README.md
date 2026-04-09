# Big_data_storage_and_storage_project



# Traffic Accident Risk Analysis Using Databricks and PySpark

## Project Overview
This project focuses on analyzing traffic accident risk using a big data pipeline built with Databricks and PySpark. The main objective is to identify important patterns and risk factors that influence traffic accidents and generate insights that can support better road safety decisions.

As cities grow and traffic density increases, understanding accident-related factors becomes increasingly important. Through this project, we designed a structured data engineering and analytics workflow to clean, transform, and analyze traffic accident data in a scalable way.

---

## Project Scenario
To simulate a realistic urban traffic analysis scenario, we created a synthetic dataset representing common traffic conditions and accident-related factors. Instead of relying on real-world data, the project uses a simulated dataset that includes multiple related tables to model a real traffic system.

The dataset consists of the following interconnected tables:

- **Accidents (Fact Table)** – stores core accident details such as severity, date, time, and references to related tables
- **Locations** – contains city, road type, and speed limit information
- **Weather** – includes weather condition, visibility, and temperature details
- **Vehicles** – contains driver-related information such as age, gender, and vehicle type
- **Violations** – stores traffic violations associated with accidents

To better reflect real-world data engineering challenges, the dataset intentionally includes:
- Missing values
- Inconsistent text formats
- Incorrect data types
- Invalid values

This allowed us to apply practical cleaning and transformation techniques using PySpark.

---

## Project Objectives
The key goals of this project are:

- Build a structured big data pipeline using **Medallion Architecture**
- Clean and standardize raw traffic accident data
- Analyze accident trends and contributing risk factors
- Generate business-ready insights from aggregated data
- Visualize findings through a Databricks dashboard

---

## Architecture Used: Medallion Architecture
This project follows the **Medallion Architecture** with three layers:

### 1. Bronze Layer (Raw Data)
The Bronze layer stores the raw generated data in Delta tables. This layer contains the original data with missing values, inconsistencies, and errors, without applying transformations.

### 2. Silver Layer (Cleaned Data)
The Silver layer performs data cleaning and standardization, including:
- Handling missing values
- Standardizing text formats
- Converting incorrect data types
- Removing or correcting invalid values

This layer ensures the data is reliable and ready for analysis.

### 3. Gold Layer (Aggregated Data)
The Gold layer contains business-ready data created through joins and aggregations on the cleaned datasets. This layer is optimized for analysis and dashboard visualization.

Key analytical outputs include:
- Accident counts by city and road type
- Severity analysis by weather condition
- Violation trends
- Time-based accident patterns

---

## Exploratory Data Analysis (EDA)
EDA was performed on the cleaned Silver layer data to identify major traffic accident patterns.

Some of the important observations include:

- Certain cities show higher accident frequency, indicating possible accident hotspots
- Most accidents fall under moderate severity levels
- Rain and snow are associated with higher accident severity
- Accident frequency increases during evening hours

These findings were used to guide the Gold layer analysis and dashboard visualizations.

---

## Key Insights
The project identified several important insights:

- **Accident Hotspots:** Some cities and highways experience higher accident frequency
- **Weather Impact:** Poor weather conditions increase accident likelihood and severity
- **Violation Impact:** Speeding and signal violations are major contributing factors
- **Driver Risk Patterns:** Younger drivers appear more frequently in accident records
- **Peak Accident Periods:** Evening hours show increased accident occurrence

These insights can help support targeted road safety improvements and data-driven decision making.

---

## Dashboard Visualization
A Databricks dashboard was created using the Gold layer outputs to visually communicate the analysis results.

The dashboard includes:
- Bar charts for accident distribution by city
- Line charts for time-based accident trends
- Pie charts for violation analysis
- Comparative visualizations for weather conditions and driver risk patterns

---

## Technologies Used
- **Databricks**
- **PySpark**
- **Delta Tables**
- **Medallion Architecture**
- **Databricks Dashboard Visualization**
