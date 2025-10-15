# 🛒 Walmart Sales Analysis & Forecasting  


---

## 📘 Project Overview  
This project performs a comprehensive **time-series analysis** on Walmart’s weekly sales data to identify key factors influencing sales performance and to implement basic **forecasting models** predicting future trends.  

---

## 📊 Data Sources  
The analysis utilizes three primary datasets merged using common identifiers (`Store`, `Date`, `IsHoliday`):

| File | Description |
|------|--------------|
| **train.csv** | Weekly sales data, including `Store`, `Dept`, `Date`, `Weekly_Sales`, and an `IsHoliday` flag. |
| **features.csv** | External and internal features like `Temperature`, `Fuel_Price`, `CPI`, `Unemployment`, and `MarkDown` promotions. |
| **stores.csv** | Static store information, including `Type` and `Size`. |

---

## 🔍 Analysis & Key Findings  

### 1️⃣ Total Weekly Sales Trend  
- **Seasonality:** Significant spikes in sales occur towards the end of each year due to holidays (Thanksgiving, Christmas).  
- **Trend:** Overall sales appear stable or slightly decreasing across 2010–2012.  

📈 _The time-series plot clearly highlights these seasonal patterns._

---

### 2️⃣ Impact of Holidays  
Comparing average weekly sales between holiday and non-holiday weeks:  

| IsHoliday | Average Weekly Sales (Approx.) |
|------------|-------------------------------|
| True | **$1,125,503** |
| False | **$1,041,257** |

✅ **Conclusion:** Average weekly sales are significantly higher during holiday periods.  

---

### 3️⃣ Sales by Store Characteristics  

#### 🔸 Store Type Breakdown  
Sales performance by store type shows a clear hierarchy:  
- **Type A**: Highest total weekly sales.  
- **Type B**: Second-highest.  
- **Type C**: Lowest.  

#### 🔸 Store Size Impact  
Stores were segmented into size groups to assess performance correlation:  

| Size Group | Average Weekly Sales (Approx.) |
|-------------|-------------------------------|
| Large | **$20,912** |
| Medium | **$13,045** |
| Small | **$8,169** |

📊 **Conclusion:** Larger stores consistently generate higher average weekly sales.  

---

## ⏱️ Simple Forecasting  

Basic time-series models applied to the total weekly sales data:

- **Moving Averages:**  
  - 24-week Rolling Mean.  
  - Exponentially Weighted Moving Average (EWMA, α=0.2).  

- **Exponential Smoothing (Holt-Winters):**  
  - Additive trend (`trend="add"`) used to forecast the next 50 weeks.  
  - The model predicts a **gradual, slight decline** in total weekly sales during 2013.  

---

## 🧠 Technologies Used  

| Tool / Library | Purpose |
|-----------------|----------|
| **Python** | Core language for data analysis |
| **Pandas** | Data manipulation & transformation |
| **NumPy** | Numerical operations |
| **Matplotlib / Seaborn** | Static data visualization |
| **Plotly** | Interactive visualizations |
| **Statsmodels** | Time series modeling & forecasting |

---

## 📈 Summary  
This project demonstrates how data-driven analysis can uncover insights about sales behavior, seasonality, and store characteristics.  
It also applies fundamental forecasting models to project short-term sales trends — a foundation for future advanced predictive modeling.

---

### 🧾 Author  
**Kerels Samir**  
  

---

