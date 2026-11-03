# SQL-Data-Cleaning-and-EDA-Project

### SQL Data Cleaning and Exploratory Data Analysis (EDA) Project

A comprehensive SQL-based data engineering project focused on transforming a heavily flawed, messy global layoff raw dataset into a pristine, structured relational schema. This project showcases advanced SQL techniques to solve data integrity issues, followed by structural Exploratory Data Analysis (EDA) to uncover operational business insights. 

### 📌 Project Overview

Raw real-world datasets are rarely analysis-ready. They frequently contain missing values, structural irregularities, duplicate inputs, and inconsistent string formatting. This project systematically cleanses the data layer before applying advanced analytical querying to make the database optimized for executive reporting. 

### 🛠️ Tech Stack & SQL Skills Demonstrated

* *Database Engine:* MySQL / PostgreSQL (Choose your dialect)
* *Data Cleansing:* Common Table Expressions (CTEs), ROW_NUMBER() Partitioning, String Trimming & Formatting (TRIM, LOWER, REPLACE), Data Type Conversions.
* *Exploratory Analytics:* Window Functions (DENSE_RANK, SUM() OVER), Advanced Aggregations (GROUP BY, HAVING), Relational Database Self-Joins, Date/Time Multi-Dimensional Analysis.

### 🧼 Phase 1: Data Cleaning Pipeline

The data cleaning process was executed systematically across four core stages to enforce strict data integrity: 

### 1. Duplicate Removal

* *Problem:* Multiple identical records inflated row metrics.
* *Solution:* Leveraged the ROW_NUMBER() window function partitioned across all key attributes within a CTE to isolate and purge duplicate records safely.

### 2. Standardization & Text Normalization

* *Problem:* Inconsistent spelling, trailing whitespaces, and messy string data prevented accurate categorical groupings.
* *Solution:* Cleaned text fields using TRIM() functions and standardized categorical names to uniform definitions across the country and company profiles.

### 3. Null Value Imputation

* *Problem:* Missing industry fields left critical gaps in analytical dimensions.
* *Solution:* Wrote database self-joins to match records with identical properties, programmatically populating missing cell properties from existing verified historical references.

### 4. Schema Optimization

* *Problem:* Date fields and metrics were stored as unindexed raw text strings.
* *Solution:* Converted and cast text data into structural DATE formats to enable high-performance timeseries analytics.

### 📈 Phase 2: Exploratory Data Analysis (EDA) Key Insights

Once data integrity reached 100%, advanced diagnostic queries were executed to extract hidden operational business trends: 

* *Macro Timeline Trends:* Calculated rolling total layoffs month-over-month utilizing structured window frameworks to track workforce fluctuations globally.
* *Industry Volatilities:* Isolated which business domains sustained the most significant organizational updates over specific calendar years.
* *Geographical Distribution:* Ranked cities and countries by aggregate operational impacts using DENSE_RANK() variations.

### 📂 Repository File Layout

* /Data Cleaning and exploratory data analysis Pr... — The complete SQL script containing the documented, step-by-step query pipeline from staging to final analysis.
* /README.md — Portfolio documentation overview for technical hiring managers.

### ⚙️ How to Review or Run This Script

1. Clone or download the script file from this repository.
2. Open your preferred SQL database management tool (e.g., MySQL Workbench, pgAdmin, DBeaver).
3. Import your raw dataset into a staging table environment.
4. Execute Phase 1 scripts sequentially to observe the data transformation pipeline.
