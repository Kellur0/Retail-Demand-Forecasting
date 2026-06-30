# Retail Demand Forecasting Using Time Series Analysis

## Project Overview

Accurate demand forecasting is essential for inventory management, supply chain optimization, and strategic business planning in retail. This project demonstrates a complete time series forecasting workflow using a publicly available retail sales dataset.

The project includes:

- Data acquisition
- Data preprocessing
- Exploratory analysis
- Time series forecasting
- Model evaluation
- Future demand prediction
- Visualization of actual and forecasted sales

---

## Objective

The objective of this project is to build a prototype forecasting model capable of predicting future retail demand using historical sales data.

---

## Dataset

**Source:** Federal Reserve Economic Data (FRED)

Dataset:
> Advance Retail Sales: Retail and Food Services (RSAFS)

Link:
https://fred.stlouisfed.org/series/RSAFS

Characteristics:

- Monthly observations
- United States retail sales
- Long historical time series
- No significant missing values
- Suitable for classical forecasting models

---

## Project Workflow

### 1. Data Collection

The dataset was downloaded directly from FRED using Python.

---

### 2. Data Preprocessing

The preprocessing stage included:

- Converting dates into DateTime format
- Setting the date column as the time index
- Sorting observations chronologically
- Checking for missing values
- Handling missing values if present
- Visual inspection for unusual spikes or outliers

---

### 3. Model Selection

The forecasting model used in this project is:

**ARIMA (AutoRegressive Integrated Moving Average)**

Reasons for selection:

- Widely used benchmark forecasting model
- Suitable for univariate time series
- Easy to interpret
- Effective for retail demand forecasting

Model configuration:

ARIMA(5,1,0)

---

### 4. Train-Test Split

The dataset was divided into:

- Training set: 80%
- Testing set: 20%

The model was trained only on historical observations before generating predictions for the test period.

---

### 5. Model Evaluation

The forecasting performance was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

### Interpretation

**MAE**

Measures the average forecasting error.

Lower MAE indicates better prediction accuracy.

---

**RMSE**

Measures forecasting error while penalizing larger mistakes.

Lower RMSE indicates stronger forecasting performance.

---

## Results

The ARIMA model successfully captured the overall retail sales trend and generated reasonable forecasts for the testing period.

### Key observations

- The model followed the long-term upward trend in retail sales.
- Forecasts remained stable during normal periods.
- Larger prediction errors occurred during sudden economic shocks or unusually high demand periods.
- The model provides a solid baseline for retail demand forecasting.

Although ARIMA performs well on historical patterns, it may struggle with abrupt structural changes that cannot be inferred from past observations alone.

---

## Forecasting

After evaluation, the trained model generated future retail demand forecasts for the next 12 months.

The notebook visualizes:

- Historical retail sales
- Test observations
- Predicted values
- Future forecasts

These visualizations allow easy comparison between actual demand and projected demand.

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn

---

## Repository Structure

```
Retail-Demand-Forecasting/
│
├── README.md
├── retail_demand_forecasting.ipynb
├── requirements.txt
└── images/
    └── forecast_plot.png
```

---

## How to Run

1. Clone the repository

```
git clone https://github.com/yourusername/Retail-Demand-Forecasting.git
```

2. Navigate to the project directory

```
cd Retail-Demand-Forecasting
```

3. Install dependencies

```
pip install -r requirements.txt
```

4. Launch Jupyter Notebook

```
jupyter notebook
```

5. Open

```
retail_demand_forecasting.ipynb
```

Run all cells to reproduce the preprocessing, model training, evaluation, and forecasts.

---

## Future Improvements

Potential enhancements include:

- Seasonal ARIMA (SARIMA)
- Facebook Prophet
- Holt-Winters Exponential Smoothing
- LSTM Deep Learning models
- Hyperparameter optimization
- Holiday and promotional effects
- External economic indicators
- Automatic anomaly detection

---

## Conclusion

This project demonstrates an end-to-end retail demand forecasting pipeline using a classical ARIMA model. The workflow covers data preparation, model training, evaluation, and future forecasting, providing a reproducible baseline solution for retail demand prediction. While ARIMA offers reliable performance for trend-based forecasting, future work can incorporate seasonal models and machine learning approaches to improve accuracy under more complex demand patterns.

---

## Author

**Keerthanaa Ellur**

Retail Demand Forecasting Project

---

## License

This project is intended for educational and research purposes.
