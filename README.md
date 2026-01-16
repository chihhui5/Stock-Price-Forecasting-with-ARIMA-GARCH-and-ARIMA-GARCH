# 📈 Stock Price Forecasting: ARIMA vs. GARCH vs. Hybrid Models

## 1. Project Overview

In the volatile world of finance, accurate stock price prediction is a cornerstone of informed decision-making. This project explores **time series forecasting** by comparing traditional statistical models with a hybrid approach.

We implement and evaluate three distinct models to see if increasing model complexity (Hybridization) truly leads to better market predictions:

* **ARIMA**: Captures linear trends and dependencies.
* **GARCH**: Specifically designed to model volatility clustering.
* **ARIMA-GARCH**: A hybrid approach aiming to capture both mean returns and variance.

## 2. Key Features & Objectives

* **Multi-Asset Analysis**: Includes Common Stocks, ETFs, and Cryptocurrencies to reduce sector bias.
* **Hybrid Modeling**: Evaluation of whether combining trend and volatility models yields superior results.
* **Iterative Training**: Models are updated and trained iteratively for robust forecasting.
* **Comprehensive Evaluation**: Performance is measured using four key statistical metrics.

## 3. Tech Stack & Tools

* **Language**: Python (Primary platform: Google Colab)
* **Data Source**: `yfinance` (Yahoo Finance API)
* **Modeling**: `statsmodels` (ARIMA), `arch` (GARCH)
* **Visualization**: `seaborn`, `matplotlib`
* **Data Handling**: `pandas`, `numpy`

## 4. Methodology

The research follows a structured pipeline to ensure reproducibility:

1. **Data Acquisition**: Extracting 5 years of historical data (2018–2023).
2. **Preprocessing**: Handling missing values and data rescaling for GARCH stability.
3. **Model Selection**: Parameter tuning for ARIMA  and GARCH .
4. **Forecasting**: Generating predictions and comparing them against test data.
5. **Visualization**: Plotting results to identify patterns and error distributions.

<img width="986" height="800" alt="image" src="https://github.com/user-attachments/assets/0a6986e0-a017-40e3-8a29-0aa0fbacb749" />


## 5. Evaluation Metrics

We use the following metrics to provide a 360-degree view of model performance:

| Metric | Description |
| --- | --- |
| **RMSE** | Root Mean Square Error |
| **MAE** | Mean Absolute Error |
| **MAPE** | Mean Absolute Percentage Error |
| **R²** | Coefficient of Determination |

## 6. Key Findings & Results

Contrary to the initial hypothesis, the results provided a significant insight: **Model complexity does not always equate to better performance.**

* 🏆 **Winner: ARIMA**. Consistently delivered the most stable and accurate forecasts across various assets.
* 🥈 **Runner-up: GARCH**. Excellent at capturing volatility but slightly less accurate in price point prediction.
* 🥉 **Hybrid ARIMA-GARCH**. While theoretically superior, it struggled with "error accumulation," making it less effective for long-term forecasting compared to simpler models.

<img width="939" height="570" alt="image" src="https://github.com/user-attachments/assets/6bf7bcd2-1eda-41b9-a47d-57c50cb9a4ca" />
<img width="939" height="515" alt="image" src="https://github.com/user-attachments/assets/718dd7c1-54f9-4de7-9a20-faf6927e12a1" />
<img width="940" height="513" alt="image" src="https://github.com/user-attachments/assets/ea341adc-8460-4e8f-8a23-d12cf5978ca4" />


### Why did the Hybrid model struggle?

1. **Overfitting**: The hybrid model tended to capture market noise rather than the underlying signal.
2. **Volatility Sensitivity**: In highly volatile markets (like Crypto), the error from the volatility component often skewed the price prediction.

## 7. Model Limitations & Observations

* **Data Rescaling**: We found that enabling `rescale=True` is critical for GARCH convergence.
* **Time Horizon**: All models performed significantly better on short-term horizons; long-term predictions (e.g., >30 days) showed rapid decay in accuracy.
* **Asset Differences**: Cryptocurrency proved much harder to forecast than traditional ETFs due to its inherent non-linear volatility.

## 8. Future Work

* **Deep Learning**: Implement **LSTM (Long Short-Term Memory)** and **Transformer** models to compare against these statistical methods.
* **Feature Engineering**: Incorporate external factors like sentiment analysis from news or macroeconomic indicators.
* **Validation**: Apply rolling-window cross-validation to further mitigate overfitting.

## 9. Conclusion

This project demonstrates that in financial forecasting, **interpretable and simpler models like ARIMA can often outperform complex hybrid structures.** It highlights the importance of data-driven decision-making and the need to rigorously test assumptions about model complexity.
