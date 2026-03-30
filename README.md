# Demand Forecasting Engine
### Retail & Energy Time-Series Analysis

This repository contains a comprehensive **Demand Forecasting Engine** that utilizes statistical, additive, and deep learning models to predict future demand in two distinct sectors: Retail and Energy. The project focuses on handling complex seasonality, holiday spikes, and non-linear trends.

---

## ## Problem Solved
Forecasting demand is often complicated by overlapping patterns like weekly cycles, yearly temperature changes, and sudden event-driven spikes. This engine solves these challenges by:
* **Modeling Multi-Layer Seasonality**: Captures weekly (shopping habits) and yearly (energy/seasonal) trends.
* **Handling Holiday Volatility**: Specifically accounts for massive demand spikes during Black Friday and Christmas, as well as post-holiday lulls.
* **Model Benchmarking**: Provides a comparative framework to determine if statistical models (ARIMA), additive models (Prophet), or neural networks (LSTM) offer the highest accuracy for a specific dataset.

---

## ## Technical Stack
* **Languages**: Python
* **Forecasting Models**: 
    * **ARIMA (5,1,2)**: Statistical baseline for linear trends.
    * **Prophet**: Multiplicative seasonality model optimized for holiday effects.
    * **LSTM (PyTorch)**: A 2-layer Recurrent Neural Network for capturing deep sequential dependencies.
* **Data Science Libraries**: Pandas, NumPy, Scikit-Learn, Statsmodels.
* **Visualization**: Matplotlib with custom styling for professional dashboards.

---

## ## Key Features
### 1. Synthetic Data Generation
The engine simulates realistic datasets for two industries:
* **Retail**: Features a linear upward trend ($800 \to 1200$ units), weekly seasonality (weekend peaks), and significant holiday-related volatility.
* **Energy**: Features a milder growth trend ($450 \to 520$ kWh) driven by temperature-based cosine seasonality.

### 2. Multi-Horizon Forecasting
The system is configured to provide a **30-day forecast horizon**. It evaluates performance using:
* **MAE** (Mean Absolute Error)
* **RMSE** (Root Mean Squared Error)
* **MAPE** (Mean Absolute Percentage Error)

### 3. Automated Reporting
* **EDA Dashboard**: Generates `demand_eda.png` showing time series decomposition and seasonal averages.
* **Model Comparison**: Generates `demand_results.png` which overlays predictions from all models against actual data.
* **Structured Export**: Outputs a `demand_data.json` file for easy integration into web-based BI dashboards.

---

## ## Getting Started
1.  Open the `demand_forecasting_engine.ipynb` in Google Colab or a local Jupyter environment.
2.  Install dependencies:
    ```bash
    pip install prophet scikit-learn torch pandas numpy matplotlib statsmodels
    ```
3.  Run all cells to generate the synthetic data, train the models, and export the results.

---
**Author:** Sara Iqbal | MSc Data Science
