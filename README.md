# 📦 Demand Forecasting & Inventory Optimization

A comprehensive Python project that predicts product-level demand using time series and machine learning models, while optimizing inventory policies to minimize stockouts and reduce costs.

---

## 🚀 Features

✅ **Demand Forecasting**
- SARIMAX-based forecasts for daily product demand
- Interactive Streamlit dashboard to tune model parameters

✅ **Inventory Optimization**
- Calculates reorder point, safety stock, and order quantity using the Newsvendor model
- Simulates inventory policies and stockout scenarios

✅ **Multi-Product Forecasting**
- Automatically loops through multiple SKUs (`Product_ID`)
- Visualizes individual demand forecasts

✅ **Feature Engineering**
- Extracts calendar-based features: day of week, month, weekend/weekday
- Assigns category tags like `Perishable` or `Non-Perishable` (mock classification)

✅ **Machine Learning Integration**
- Implements Random Forest regression using lag-based features to predict demand
- Compares traditional time series forecasting with ML predictions

✅ **Forecast Accuracy Metrics**
- Computes RMSE, MAE, and MAPE for each product forecast

✅ **Inventory Simulation**
- Simulates reorder policy impact (e.g. stockouts, overstock days)
- Visualizes inventory levels over time

✅ **Streamlit App**
- Upload your dataset, visualize trends, tune parameters, and get live forecasts

---

## 📁 Dataset Format

The CSV input file should have the following structure:

```csv
Date,Product_ID,Demand,Inventory
2024-01-01,A1001,120,500
2024-01-01,A1002,130,450
...
```

---

## 🛠️ Requirements

- Python 3.8+
- `pandas`, `numpy`, `matplotlib`, `plotly`, `statsmodels`, `scikit-learn`
- `streamlit` (for web app)

Install all dependencies:

```bash
pip install -r requirements.txt
```

---

## 📊 Run Forecast Script

To run the base forecasting logic and inventory simulation:

```bash
python demand_forecasting_and_inventory_optimization.py
```

---

## 🌐 Run Streamlit Web App

For interactive forecasting:

```bash
streamlit run demand_forecasting_and_inventory_optimization.py
```

You can:
- Upload your dataset
- Tune SARIMAX parameters
- View forecast plots and predicted values

---

## 📈 Sample Output

### Forecast Plot for Product A1001
![Forecast Plot](https://github.com/your-username/your-repo-name/assets/forecast_plot.png)

### Inventory Simulation
- Policy A Stockouts: 4  
- Policy B Stockouts: 1  
- Overstock Days: 5

---

## 📌 Roadmap & Future Work

- Incorporate real-time weather/holiday APIs as exogenous inputs
- Add clustering for product segmentation
- Export PDF reports summarizing forecast + inventory strategy
- Add database integration for large-scale SKU handling

