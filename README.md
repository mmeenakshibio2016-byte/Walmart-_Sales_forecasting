# Walmart-_Sales_forecasting
# Walmart Sales Forecasting & Inventory Optimization
This project uses **Time-Series Analysis (SARIMA)** to predict weekly sales across 45 Walmart stores for the next 12 weeks, addressing the "Bullwhip Effect" in retail supply chains.

## 📊 Project Overview
- **Objective:** Reduce inventory mismatch and improve forecasting accuracy.
- **Key Discovery:** Identified a 50% reduction in MAE by accounting for 52-week seasonality.
- **Top Performers:** Predictive modeling identified Stores 20, 4, 14, 13, and 2 as high-priority locations.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, Statsmodels (SARIMA), Matplotlib, Seaborn
- **Environment:** Google Colab
- Table of Contents
- Problem Statement:
Retail organizations often face challenges in managing the inventory levels with fluctuating customer demand. Inaccurate demand estimation leads to either excess inventory or stock shortages, resulting in increased holding costs, lost sales opportunities, and operational inefficiencies. One of the Tech giant is Walmart. The core problem addressed in this capstone project is the ineffective management of inventory caused by a mismatch between demand and supply, which negatively impacts the financial and operational performance of the organization. This project focuses on analyzing historical sales data to understand demand behaviour and develop forecasting models to support better inventory planning.
________________________________________
 Project Objective
The objectives of this capstone project are:
•	To analyse historical weekly sales data and identify demand patterns
•	To study the impact of external factors such as unemployment rate, temperature, and Consumer Price Index on sales
•	To detect seasonality and trends in sales data
•	To build predictive models for predicting future forecasting weekly sales
•	To provide insights that support effective inventory management decisions
________________________________________
 Data Description
The dataset used in this project consists of 6,435 records with 8 attributes, representing weekly sales data across multiple retail stores. Each observation corresponds to a store–week combination.
Key attributes include:
•	Store identifier
•	Date
•	Weekly Sales (target variable)
•	Holiday indicator
•	Temperature
•	Fuel Price
•	Consumer Price Index (CPI)
•	Unemployment Rate
The dataset exhibits time-dependent characteristics, seasonal patterns, and sensitivity to macroeconomic factors, making it suitable for time-series analysis and forecasting. There are 45 outlets in the Walmart stores.
________________________________________


Data Pre-processing Steps and Inspiration
Data preprocessing was carried out to ensure accuracy and reliability of the analysis. First step the libraries of python were imported and the dataset was loaded into google colab.
Before establishing a forecasting model ,it is extremely significant to compile high quality time -Series data and clean the same to Vacant inconsistencies. Preprocessing makes the model learn based on an orderly dataset.
Key Actions in Data Collection & Preprocessing:
Key Actions: Data Collection & Preprocessing
Managing time series data (like Walmart's weekly sales) requires specific steps to ensure the model doesn't "learn" from noise or gaps.
•	Loading Data: Usually involves importing large datasets from CSV files and converting the date column into a datetime object to set it as the index.
•	Handling Missing Values:
o	Forward/Backward Fill: Best for small gaps where the value is unlikely to change drastically.
o	Interpolation: Ideal for sales data, as it assumes a linear or polynomial trend between two known points.
•	Removing Outliers: In a Walmart context, it's vital to distinguish between an anomaly (a data error) and a peak (like Black Friday). Use IQR or Z-scores to find genuine errors while keeping seasonal spikes.

a. Weekly Sales and Unemployment Rate Analysis
Overall, there is a very weak negative correlation between weekly sales and the unemployment rate (-0.1062). This indicates that increases in unemployment are associated with a slight decrease in weekly sales, though the relationship is not strong at an aggregate level.
However, store-level analysis reveals significant variation. Stores such as Store 38 (-0.785) and Store 44 (-0.780) show a strong negative correlation, suggesting that their sales are highly sensitive to changes in unemployment. In contrast, Store 36 (0.834) and Store 35 (0.484) exhibit a positive correlation, indicating that their sales may be influenced by different customer demographics or economic dynamics.
 
 
The histogram and KDE plot show the distribution of weekly sales. It appears that the majority of weekly sales are concentrated in the lower range, with a long tail extending towards higher sales values, indicating a right-skewed distribution. This is typical for sales data, where a few items or periods account for a large portion of sales, while many others have lower sales.

b. Seasonal Trends in Weekly Sales
Weekly sales display a clear seasonal pattern, with peaks typically observed during March, April, and July, and noticeable declines in December, followed by lower sales in January and February. These fluctuations may be attributed to seasonal consumer behaviour, holiday spending cycles, and post-holiday slowdowns.
 


c. Temperature and Weekly Sales
The correlation between weekly sales and temperature is very weak (-0.0638), indicating that temperature has negligible influence on sales performance across stores.  


d. Consumer Price Index (CPI) and Weekly Sales
The overall correlation between weekly sales and CPI is -0.0726, suggesting a minimal negative relationship. While CPI does not significantly impact overall sales, certain stores show stronger sensitivity.
For instance, Store 36 (-0.915) and Store 35 (-0.424) are negatively affected by rising CPI, whereas Store 38 (0.813) and Store 44 (0.740) exhibit a positive correlation, indicating varied pricing sensitivity across locations.
 
e. Top Performing Stores
Based on total weekly sales, the top five performing stores are:
•	Store 20: $301,397,792.46
•	Store 4: $299,543,995.58
•	Store 14: $288,999,911.33
•	Store 13: $286,517,709.68
•	Store 2: $275,382,440.98

f. Worst Performing Store and Sales Disparity
The lowest-performing store is Store 33, with total weekly sales of $37,160,221.96.
The difference between the highest-performing store (Store 20) and the lowest-performing store (Store 33) is $264,237,570.50, highlighting a substantial disparity in sales performance across stores.


## 📈 Key Visualization

[Insert Screenshot of your Sales Forecast Plot here]
<img width="1920" height="1080" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/666a27db-d9c6-41f4-a42c-2fab5886153f" />

