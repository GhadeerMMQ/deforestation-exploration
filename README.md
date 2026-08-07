# 🌳 Global Deforestation Analysis (1990–2016)

## Overview

This project analyzes global deforestation trends between 1990 and 2016 using SQL. By querying data from the World Bank, the analysis examines changes in forest area at the global, regional, and country levels to identify areas experiencing significant forest loss as well as countries that have successfully increased forest coverage.

The project demonstrates the use of SQL for data preparation, analytical querying, and extracting meaningful insights from a real-world environmental dataset.

---

## Problem Statement

ForestQuery aims to better understand global deforestation by answering questions such as:

* How has the world's forest area changed over time?
* Which regions have experienced the greatest forest loss?
* Which countries have successfully increased forest area?
* Which countries should be prioritized for conservation efforts?

---

## Dataset

The analysis uses three datasets provided by the World Bank:

* **Forest Area** – Forest area (sq km) by country and year
* **Land Area** – Total land area by country and year
* **Regions** – Country regions and income groups

The datasets cover the years **1990 through 2016**.

---

## Tools & Technologies

* PostgreSQL
* SQL
* Views
* Common Table Expressions (CTEs)
* JOINs
* Aggregate Functions
* CASE Statements

---

## Project Workflow

### 1. Data Preparation

A SQL view named `forestation` was created by joining the three datasets. The view also calculates the percentage of each country's land covered by forests, providing a single source for all subsequent analyses.

### 2. Global Analysis

The global forest area was compared between 1990 and 2016 to determine the total loss in forest coverage and calculate the percentage change over time.

### 3. Regional Analysis

Forest coverage was analyzed across world regions to compare forest percentages in 1990 and 2016 and identify regions with increasing or decreasing forestation.

### 4. Country-Level Analysis

Countries were ranked based on:

* Largest increase in forest area
* Largest decrease in forest area
* Largest percentage loss
* Forest coverage quartiles

This analysis highlights both successful conservation efforts and countries facing the greatest deforestation challenges.

### 5. Recommendations

The findings were summarized to identify regions and countries where conservation efforts could have the greatest impact and to highlight successful reforestation examples that may serve as models for future initiatives.

---

## Key Findings

* Global forest area decreased from **41.28 million km²** in 1990 to **39.96 million km²** in 2016, representing a loss of approximately **1.32 million km² (3.2%)**.

* **Latin America & Caribbean** had the highest forest coverage in both years but also experienced the largest decline, while **Middle East & North Africa** remained the least forested region.

* **China** recorded the largest increase in forest area during the study period, demonstrating the impact of large-scale reforestation efforts.

* **Brazil** experienced the greatest absolute forest loss, while **Togo** recorded the largest percentage decrease in forest area.

* Most countries fell within the **0–25% forest coverage** quartile in 2016, with only nine countries exceeding 75% forest coverage.

---

## SQL Concepts Demonstrated

* Creating Views
* INNER JOINs
* Common Table Expressions (CTEs)
* Aggregate Functions (`SUM`, `COUNT`)
* Conditional Logic (`CASE`)
* Calculated Columns
* Percentage Calculations
* Data Grouping and Ranking
* Multi-table Analysis

---

## Repository Structure

```text
.
├── report.pdf
├── queries.sql
├── README.md
```

---

## How to Run

1. Create a PostgreSQL database.
2. Import the provided datasets.
3. Execute the SQL script to create the `forestation` view.
4. Run the analytical queries to reproduce the results presented in the report.

---

## Future Improvements

* Develop an interactive dashboard to explore deforestation trends by country and region.
* Incorporate more recent World Bank data to extend the analysis beyond 2016.
* Analyze additional environmental indicators to better understand the factors influencing deforestation.

---

## Author

**Ghadeer Almuqbil**

Physics graduate transitioning into Data Analytics with an interest in using SQL and data analysis to solve real-world problems and generate actionable insights.
