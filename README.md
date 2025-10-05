# 🛢️ Natural Gas Price Forecasting using SARIMA

## 📘 Project Overview
This project focuses on **forecasting natural gas prices** using **Time Series Analysis** techniques — specifically the **SARIMA (Seasonal ARIMA)** model.  
The goal is to predict future price trends to support **energy traders, analysts, and policymakers** in making data-driven decisions.

By analyzing historical monthly price data, the model forecasts the next 12 months of prices and provides an easy way to **estimate prices for any specific date** (daily granularity through interpolation).

---

## 📈 Key Features
- 📊 Time series forecasting using **SARIMA (Seasonal ARIMA)**  
- 🧹 Automated data cleaning and preprocessing with **pandas**  
- 📅 **Daily price interpolation** from monthly forecasts  
- ⚙️ Interactive function to estimate prices for any given date  
- 📉 Visualization of **historical vs forecasted prices** using **matplotlib**  
- ✅ End-to-end pipeline from raw data to prediction  

---

## 🧠 Project Workflow

### 1️⃣ Data Preparation
- Loaded historical natural gas prices (`Nat_Gas.csv`)
- Converted the “Dates” column into datetime format
- Set “Dates” as the index to enable time-series operations

### 2️⃣ Model Development
- Chose **SARIMA** to capture both trend and seasonal components
- Model parameters: `order=(1,1,1)` and `seasonal_order=(1,1,0,12)`
- Trained the model using the `statsmodels` library

### 3️⃣ Forecasting
- Forecasted prices for the next **12 months**
- Combined historical and forecasted data into a single time series

### 4️⃣ Visualization
- Plotted historical (actual) vs forecasted prices using **matplotlib**
- Highlighted expected trends for upcoming months

### 5️⃣ Daily Interpolation
- Converted monthly data to daily frequency using time-based interpolation
- Enabled fine-grained, continuous price estimates

### 6️⃣ Price Estimation Function
- Built a user-defined function:
  ```python
  estimate_gas_price("YYYY-MM-DD")
