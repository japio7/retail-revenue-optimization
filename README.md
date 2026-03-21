# 📊 Retail Revenue Optimization

---

## 🔍 Overview
This project applies machine learning to optimize retail pricing strategy and maximize revenue by identifying price–demand relationships.

By modeling how demand responds to price changes, this project demonstrates how data-driven pricing decisions can improve business performance.

---

## 🎯 Business Problem
Retailers must balance price and demand:
- Increasing price raises revenue per unit but reduces demand
- Decreasing price increases demand but lowers revenue per unit

The challenge is to find the **optimal price point that maximizes total revenue**.

---

## 🧠 Approach

### 1. Data Preparation
- Cleaned and structured transactional retail data
- Handled missing values and ensured consistency

### 2. Feature Engineering
Created features to capture demand patterns:
- Lag demand (`lag_1_units`)
- Rolling averages (`rolling_3_units`)
- Price change percentage
- Seasonal features (month, year)
- Product-level encoding (StockCode)

---

### 3. Modeling
- Model: Random Forest Regressor  
- Target: Units Sold  

**Performance:**
- MAE: 367.73  
- R²: 0.73  

---

### 4. Price Simulation
Demand was simulated across a range of prices using the trained model.

Revenue was calculated as:
- Revenue = Price × Predicted Demand


---

## 📈 Key Results

- **Optimal Price:** $2.53  
- **Predicted Demand:** ~1651 units  
- **Maximum Revenue:** ~$4,176  

---

## 📊 Visualization

![Revenue Curve](images/revenue_optimization_curve.png)

---

## 💡 Key Insights

- Demand exhibits a non-linear relationship with price
- Revenue increases with price up to a peak, then declines as demand drops
- A small number of features (price and recent demand) drive most of the predictive power
- Many engineered features contribute minimal additional value

---

## ⚡ Business Impact

This approach enables:
- Data-driven pricing strategies
- Revenue optimization through simulation
- Scenario analysis before implementing pricing changes

---

## ⚠️ Limitations

- No cost data available → profit optimization not included
- Model assumes historical demand patterns persist
- Analysis is limited to single-product optimization

---

## 🚀 Future Improvements

- Incorporate cost data for profit optimization
- Use advanced models (XGBoost / LightGBM)
- Expand to multi-product pricing strategies
- Deploy as a real-time pricing tool

---

## 📂 Project Structure
```

retail-revenue-optimization/
│
├── README.md
├── requirements.txt
├── Retail Revenue Optimization Report
│
├── models/
│   └── demand_model.pkl
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modeling.ipynb
│   └── 04_price_simulation.ipynb
│
├── data/
│   ├── raw
│   │   └── OnlineRetail.xlsx
│   └── processed
│       ├── agg_data.csv
│       └── model_data.csv
│
└── images/
    ├── revenue_optimization_curve.png
    └── top_10_feature_importance.png

```


---

## ▶️ How to Run

1. Clone the repository:
- git clone https://github.com/japio7/Reports/retail-pricing-optimization.git
---

2. Install dependencies:
- pip install -r requirements.txt
___

3. Run notebooks in order:
- 01_data_cleaning
- 02_feature_engineering
- 03_modeling
- 04_price_simulation

---

## 🛠️ Tech Stack

- Python
- Pandas / NumPy
- Scikit-learn
- Matplotlib
- Joblib

---

## 👤 Author

**Jared Pino**  
Master’s in Data Science  

GitHub: https://github.com/japio7

