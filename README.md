# Time Series Analysis of GDP and Imports  
### Central African Republic (1960–2017)

## 📊 Project Overview
This project analyzes the relationship between GDP and Imports (% of GDP) in the Central African Republic using time series methods.

The dataset spans from 1960 to 2017 and focuses on understanding:
- Long-term economic trends  
- Stationarity and transformations  
- Forecasting future values  
- The dynamic relationship between GDP and Imports  

---

## 📁 Dataset
- Source: The Global Economy  
- Observations: 58 years (1960–2017)  
- Variables used:
  - GDP (current USD)
  - Imports (% of GDP)

---

## 🔍 Methods

### 1. Exploratory Data Analysis (EDA)
- Histograms and boxplots  
- Time series visualization  
- No missing values or significant outliers detected  

### 2. Stationarity & Transformation
- GDP shows heteroscedasticity → log transformation applied  
- Imports variance is stable → no transformation needed  
- Augmented Dickey-Fuller (ADF) test used  

### 3. Differencing
- Both series require first-order differencing (d = 1)  
- Final stationary series:
  - diff(log(GDP))
  - diff(Imports)

### 4. Model Selection
- GDP → ARIMA(0,1,0) with drift  
- Imports → ARIMA(2,1,0)  
- Model selection based on:
  - AIC / BIC  
  - Statistical significance  
  - Ljung-Box test  

### 5. Cross-Correlation (CCF)
- Relationship between GDP and Imports is **lagged**, not simultaneous  
- Imports may influence GDP in the long run  

---

## 📈 Results

### GDP
- Shows steady upward growth  
- Forecast (2018–2027):  
  - From ~2.05B to ~3.22B USD  
- Increasing uncertainty over time  

### Imports (% of GDP)
- Remains relatively stable (~31–33%)  
- No strong upward or downward trend  

---

## 🔮 Forecasting
- ARIMA models used for 10-year forecasts  
- Confidence intervals widen over time (expected in time series models)

---

## 🧠 Key Insights
- GDP requires log transformation for stability  
- Imports are already stable in variance  
- Economic relationship is lagged (not immediate)  
- Simple models perform better than complex ones  

---

## 🛠️ Tools & Libraries
- R  
- forecast  
- astsa  
- tseries  
- ggplot2  
- MASS  

---

## 📎 Files
- `time-series-gdp-imports-analysis.pdf` → Full report  
- (Optional) R script / dataset if included  

---

## 👩‍💻 Author
Yajiao Liu  
UC Davis  

---

## ⭐ Notes
This project demonstrates skills in:
- Time series analysis  
- ARIMA modeling  
- Statistical testing  
- Data visualization  
