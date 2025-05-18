# POWER BI BUSINESS INSIGHTS DASHBOARD PROJECT

---

## Project Overview
This Power BI project follows a complete data analysis workflow; importing, cleaning, modeling, and visualizing business data to uncover actionable insights. It showcases strong skills in data transformation, DAX calculations, and interactive reporting to support informed decision-making.

---

## Data Preparation & ETL Process
This project follows a complete **ETL (Extract, Transform, Load) pipeline** to ensure clean, structured data for analysis in Power BI.

### Data Extraction - Loading Raw Data into Power Query
- **Imported CSV files & folder-based data** into query editor
- **Combined multiple files** into structured tables

### Data Transformation - Cleaning the Data
- **Removed erorrs and empty rows** to ensure data accuracy
- **Eliminated duplicates and handled missing values** to maintain data integrity
- **Standardized column names & data types** for consistency across tables
- **Applied transformation steps**, including splitting/merging columns, formatting values, and extracting needed information
- **Created many new calculated columns** to enhance analysis
-  **Built a Calendar Table** with calculated columns (Week, Month, Year, Start of Year, Start of Quarter) for time-based analysis

### Data Loading - Loading Data to BI Front-end
- **Loaded cleaned and transformed data** from Power Query into Power BI
- **Ensured data structure compatibility** for smooth report building

---

## Data Modeling
After loading the cleaned dataset to Power BI fronend, a well built data model was ceated using **snowflake schema**. Steps included are:

- **Established relationships between tables** using Primary & Foreign Keys
- **Defined one-to-many relationships** for correct data aggregations
- **Kept cross filter direction to single** to avoid circular dependencies and ambiguous joins
- **Used snowflake schema** to ensure efficient query performance
- **Hid specific columns** to prevent incorrect filtering in dashboards

---

## DAX Measures
DAX (Data Analysis Expressions) was used to create custom calculations for dynamic reporting and accurate business analysis. To keep all measures organized, a separate table  'Measure Table' was created to store them in one place, making them to find and manage easily.

### Key DAX Measures
- **Total Orders** - Calculates the total number of orders placed
- **Weekend Orders** - Calculates the number of orders made on Saturday & Sunday
- **% of All Orders** - Measures how a specific subset of orders contributes to total order
- **Revenue Target** - Compares current revenue with the predefined target
- **Return Rate** - Calculates the percentage of returned orders compared to total orders
- **Previous Month Profit** - Gets the total profit from the last month
- **Average Revenue Per Customer** - Calculates the average revenue generated per individual customer
- **90 Days Rolling Profit** - Calculates total profit over the last 90 days, updating dynamically as new data comes in
  - = CALCULATE([Total Profit], DATESINPERIOD('Calendar Lookup'[Date], MAX('Calendar Lookup'[Date]), -90, DAY))
  
---

## Data Visualization




