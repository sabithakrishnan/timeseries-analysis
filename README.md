# Time Series Analysis & Forecasting Showcase

This repository showcases various time series analysis and forecasting techniques applied to the **UCI Air Quality Dataset**. The goal of this project is to build, evaluate, and compare multiple models across different paradigms to find the most accurate forecasting approach.

## 📂 Project Structure

```text
├── ML Algorithms/                     # Machine learning models (Random Forest, LGBM, XGBoost)
├── neural network algorithms/         # Deep learning models (CNN, LSTM, Transformer)
├── statistical modelling algorithms/  # Statistical models (ARIMA, SARIMA, ETS, Prophet)
└── README.md                          # Project documentation
```

## 📊 Project Status & Methodology
Models are developed incrementally. The algorithms are categorized into three distinct approaches:
1. **Statistical Modeling**: ARIMA, SARIMA, ETS, and Prophet.
2. **Machine Learning**: LightGBM (LGBM), XGBoost, and Random Forest.
3. **Deep Learning (Neural Networks)**: CNN, LSTM, and Transformers.

For every model implemented, this repository includes:
* Full training and inference workflows.
* Static and interactive forecasting graphs.
* Detailed evaluation metric analysis ($R^2$, Adjusted $R^2$, RMSE, and MAE).

## 📊 Model Performance Comparison

| Model Category | Algorithm | $R^2$ Score | Adjusted $R^2$ | RMSE | MAE |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Statistical** | ARIMA | -0.0262 | -0.0290 | 1.4025 | 1.0320 |
| **Statistical** | SARIMA | -1.1094 | -1.1117 | 2.0108 | 1.4818 |
| **Statistical** | ETS | 0.4954 | 0.4915 | 0.4305 | 0.4751 |
| **Statistical** | Prophet | 0.3809 | 0.3793 | 0.5281 | 0.5432 |
| **Machine Learning** | LGBM | **0.9433** | **0.9431** | 2.0052 | 1.0000 |
| **Machine Learning** | XGBoost | 0.8071 | 0.8065 | 0.3680 | 0.3960 |
| **Machine Learning** | Random Forest | 0.9243 | 0.9229 | **0.0652** | **0.1900** |
| **Deep Learning** | CNN | 0.8092 | 0.8091 | 2.8089 | 1.7172 |
| **Deep Learning** | **LSTM** | 0.8141 | 0.8139 | **0.0482** | **0.0350** |
| **Deep Learning** | Transformer | 0.4961 | 0.4947 | 0.6628 | 0.5073 |

## 📈 Key Findings & Insights
* **Best Overall Performer**: **LSTM** delivered the most consistent and accurate results. It maintained extremely low error metrics (RMSE: 0.0482, MAE: 0.0350) alongside a strong variance explanation ($R^2$ of 0.8141), proving its strength in capturing long-term sequential dependencies.
* **Strong Baseline**: **Random Forest** proved to be the second-best model overall, handling non-linear relationships very effectively with a high $R^2$ (0.9243) and low errors (RMSE: 0.0652).
* **Statistical Model Failure**: Traditional forecasting models like **ARIMA and SARIMA** performed very poorly on this dataset, yielding negative $R^2$ values. This indicates they struggled significantly with the scale, noise, or complexity of the air quality data.
* **LGBM Discrepancy Note**: While **LGBM** achieved the highest overall $R^2$ score (0.9433), it exhibits unusually high error metrics (RMSE: 2.0052). This divergence between directional fit and scale error is an interesting data point currently under review.

## 🛠️ Datasets & Technologies
* **Dataset**: [UCI Air Quality Dataset](https://uci.edu)
* **Libraries**: `scikit-learn`, `tensorflow`/`pytorch`, `statsmodels`, `xgboost`, `lightgbm`, `prophet`, `pandas`, `matplotlib`

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.x installed. Clone this repository:
```bash
git clone https://github.com
cd timeseries-analysis
```

### Installation

```bash
pip install -r requirements.txt
```
