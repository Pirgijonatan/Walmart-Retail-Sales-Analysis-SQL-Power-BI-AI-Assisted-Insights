# Walmart-Retail-Sales-Analysis-SQL-Power-BI-AI-Assisted-Insights

## Dataset

This project uses the Walmart Retail Dataset sourced from Kaggle:

**Source:** [Walmart Retail Dataset — Kaggle](https://www.kaggle.com/datasets/manjeetsingh/retaildataset)

The dataset contains retail sales information used for analyzing store performance, sales trends, department performance, holiday effects, and external factors.

### Dataset Files
- `sales data-set.csv` — Weekly sales data by store and department
- `Features data set.csv` — External factors such as temperature, fuel price, CPI, unemployment, markdowns, and holidays
- `stores data-set.csv` — Store information including store type and size

## Project Overview

This project analyzes Walmart retail sales data to understand store performance, sales trends, department performance, and the relationship between store size and sales.

The analysis was done using SQL for data exploration and Power BI for visualization. The results were then used to create an interactive dashboard and identify several business insights from the dataset.

## Tools Used

- **SQLite** — data exploration and SQL analysis
- **Power BI** — data visualization and dashboard
- **GitHub** — project documentation and portfolio

- ## Data Preparation

Before starting the analysis, the dataset was imported into SQLite and checked to understand its structure and data quality.

The preparation included:

- Checking the number of rows and columns in each dataset
- Checking for missing values
- Checking the date format
- Checking the sales period
- Reviewing the available stores and departments
- Preparing the datasets for SQL analysis and further visualization in Power BI

<img width="1461" height="892" alt="image" src="https://github.com/user-attachments/assets/dd85b7a7-7bc5-4c29-bd82-7058407780d6" />


## SQL Analysis

SQL was used to explore the dataset and calculate several metrics related to store and sales performance.

Some of the analysis included:

- Identifying the top-performing stores based on total sales
- Comparing sales across different store types
- Comparing store size with total sales
- Calculating sales relative to store size
- Analyzing sales trends over time
- Comparing holiday and regular-week sales
- Analyzing department performance


### Example Query

```sql
SELECT 
s.Store,
st.size,
SUM(s.Weekly_Sales ) AS total_penjualan
FROM sales_data_set as s
JOIN stores_data_set as st
 ON s.Store = st.Store 
 GROUP by 
 s.Store,
 st.size
 ORDER BY total_penjualan DESC 
 limit 10;
```


<img width="1917" height="1088" alt="Screenshot 2026-09-25 091152" src="https://github.com/user-attachments/assets/50799b2b-b5d6-49b0-b23b-e04797b27807" />


## Power BI Dashboard

The analyzed data was visualized using Power BI to explore store performance, sales trends, department performance, holiday sales, and external factors.

### Store Performance

This section focuses on store size, sales, and sales performance relative to store size.

 <img width="1332" height="647" alt="image" src="https://github.com/user-attachments/assets/0f5468ec-10df-480f-aae8-159a6c72f5a3" />


### Sales and Department Performance

This section shows sales trends over time and the departments with the highest and lowest sales.

 <img width="1378" height="686" alt="image" src="https://github.com/user-attachments/assets/e0491392-472b-4005-858d-c7185900810e" />


### Holiday vs Regular Weeks

This section compares transaction volume, total sales, and average sales between regular and holiday weeks.

 <img width="1372" height="348" alt="image" src="https://github.com/user-attachments/assets/1adba8cc-d2d2-41a8-8f49-c56891b4ee3b" />


### External Factors

This section visualizes fuel prices and the Consumer Price Index (CPI) over time.

 <img width="1338" height="631" alt="image" src="https://github.com/user-attachments/assets/d2cb3f36-f881-4903-b430-fbbe10390365" />


## Key Insights

Several insights were identified from the analysis:

- **Store 20** recorded the highest total sales among the stores analyzed.
- **Store 43** showed the highest sales relative to its store size, indicating strong sales efficiency compared to other stores.
- **Department 92** had the highest total sales among the departments.
- **Holiday weeks** had a higher average sales value than regular weeks, although regular weeks contributed a much larger share of total sales.
- Sales performance varied considerably between stores, showing that store size alone does not fully explain sales performance.


## AI-Assisted Analysis

AI was used as an analytical assistant to generate additional insights and possible interpretations from the analyzed data.

The analysis and dashboard were created independently using SQL and Power BI. AI-generated insights were then reviewed and checked against the data before being included in the project.

### Langflow Pipeline

Langflow was used to build the workflow for generating AI-assisted insights from the analyzed data.

<img width="1200" height="915" alt="image" src="https://github.com/user-attachments/assets/28cb1f5b-62c3-49d0-acfb-4c1604f01e13" />

## Conclusion

This project provided an opportunity to explore retail sales data using SQL and Power BI.

The analysis helped identify differences in store performance, department sales, sales trends, and holiday-week performance. The Power BI dashboard was then created to present these findings in a more accessible way.

AI was used as an additional analytical assistant to explore further insights, while the final results were reviewed against the dataset.
