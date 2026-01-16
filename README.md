# Stock Price Forecasting with ARIMA, GARCH, and ARIMA-GARCH

## 1. Project Overview

With the rapid advancement of AI and data-driven technologies across industries such as agriculture, marketing, and healthcare, stock market prediction has become an increasingly important and popular research topic. Due to the inherent volatility of financial markets—driven by multiple unpredictable factors—accurate stock price forecasting is critical for informed investment decision-making.

This project focuses on **time series forecasting** using traditional statistical models and a hybrid approach to analyze their effectiveness in predicting stock prices. In particular, it evaluates and compares the performance of:

* **ARIMA (Autoregressive Integrated Moving Average)**
* **GARCH (Generalized Autoregressive Conditional Heteroskedasticity)**
* **Hybrid ARIMA–GARCH model**

The goal is to assess whether the hybrid model can overcome the limitations of traditional models and improve forecasting accuracy, especially in volatile financial environments.

## 2. Objectives

* Implement and train ARIMA, GARCH, and ARIMA-GARCH models for stock price forecasting
* Compare model performance using multiple evaluation metrics
* Analyze whether hybrid models outperform traditional statistical models
* Visualize forecasting results and evaluation metrics for clearer interpretation

## 3. Dataset

* **Data Source:** Yahoo Finance
* **Time Period:** January 1, 2018 – December 31, 2023
* **Asset Types:**

  * Common stocks
  * Exchange-Traded Funds (ETFs)
  * Cryptocurrency

Using multiple asset categories helps reduce potential bias caused by differences in market behavior.

## 4. Methodology

### 4.1 Research Workflow

The project follows a structured workflow to ensure reliable and reproducible results:

1. Background research and literature review
2. Environment setup and library installation
3. Data collection and preprocessing
4. Model selection and training
5. Forecasting and evaluation
6. Visualization and comparative analysis

### 4.2 Implementation Environment

* **Platform:** Google Colab
* **Programming Language:** Python
* **Key Libraries:**

  * `yfinance` – financial data retrieval
  * `arch` – GARCH modeling
  * `statsmodels` – ARIMA modeling
  * `seaborn` & `matplotlib` – data visualization

---

### 4.3 Model Training and Forecasting

* **Models Used:**

  * ARIMA (linear trend modeling)
  * GARCH (volatility modeling)
  * ARIMA-GARCH (hybrid approach)

Each model is initialized with appropriate parameters and trained iteratively using historical price data before generating forecasts.

## 5. Evaluation Metrics

To assess forecasting accuracy, four commonly used metrics are applied:

* **RMSE (Root Mean Square Error)**
* **MAPE (Mean Absolute Percentage Error)**
* **MAE (Mean Absolute Error)**
* **R² (Coefficient of Determination)**

Each metric highlights different aspects of model performance, such as error magnitude, relative accuracy, and goodness of fit.

## 6. Visualization

Data visualization is used to enhance interpretability and communication of results:
* Line Charts: Compare actual stock prices with model predictions
* Bar Charts: Compare evaluation metrics across models

All visualizations are generated using the `seaborn` library.

## 7. Results & Key Findings

* Traditional statistical models (**ARIMA and GARCH**) consistently produced more accurate forecasts than the hybrid **ARIMA-GARCH** model.
* The hybrid model did **not** significantly improve long-term forecasting accuracy.
* ARIMA and GARCH demonstrated stronger stability and reliability across different asset types.

## 8. Conclusion

This project evaluated the effectiveness of three time series forecasting models—**ARIMA**, **GARCH**, and **ARIMA-GARCH**—for stock price prediction using historical financial data. Each model was trained iteratively and assessed using multiple evaluation metrics to compare forecasting accuracy and robustness.

Contrary to the initial assumption that the hybrid **ARIMA-GARCH** model would outperform traditional statistical models, the experimental results showed that **ARIMA consistently achieved the best performance**, followed by **GARCH**. The hybrid model did not demonstrate a significant improvement, particularly in long-term forecasting scenarios.

These findings highlight that **model complexity does not necessarily lead to better performance**, especially when applied to noisy and highly volatile financial time series.

## 9. Key Findings

* **ARIMA** delivered the most accurate and stable forecasts across multiple asset types
* **GARCH** performed well in modeling volatility but ranked second overall
* **ARIMA-GARCH** was more suitable for short-term forecasting and struggled with long-term predictions
* Evaluation metrics (RMSE, MAE, MAPE, R²) consistently favored traditional statistical models over the hybrid approach

## 10. Model Limitations & Observations

Several factors were identified that influenced model performance:

### Overfitting

Time series models can overfit when excessive noise is captured instead of meaningful patterns. Overtraining and excessive iterations increased this risk, particularly in longer forecasting horizons.

### Data Rescaling

For GARCH-based models, improper data scaling negatively affected model stability. Enabling `rescale=True` significantly improved convergence and performance, highlighting the importance of correct model specification.

### Model Characteristics

While the ARIMA-GARCH model can capture both trend and volatility, error accumulation over time reduced its effectiveness in long-term forecasting. This limitation explains its weaker performance compared to ARIMA and GARCH.

## 11. Learning Outcomes

This project provided both technical and analytical growth through hands-on experimentation:

### Time Series & Forecasting Fundamentals

* Gained a solid understanding of time series concepts, volatility modeling, and statistical forecasting methods
* Developed the ability to interpret forecasting results using multiple evaluation metrics

### Python & Tooling

* Transitioned from Java to Python for data science and financial modeling
* Learned to use key libraries such as `yfinance`, `statsmodels`, `arch`, and `seaborn`

### Model Training & Evaluation

* Trained and tuned multiple forecasting models
* Implemented iterative forecasting pipelines using real-world financial data
* Visualized predictions and evaluation metrics for clearer comparison

### Problem-Solving & Debugging

* Addressed challenges such as overfitting, model instability, and rescaling issues
* Improved forecasting accuracy through literature review and experimentation

### Critical Thinking

* Learned to question initial assumptions and rely on data-driven conclusions
* Recognized that hybrid or more complex models are not always superior

## 12. Future Work

Several extensions could further enhance this project:

### Advanced Models for Long-Term Forecasting

* Explore deep learning–based approaches such as **LSTM**, **GRU**, or **Transformer models**
* Compare statistical and neural models under identical evaluation frameworks

### Overfitting Prevention

* Apply rolling-window validation and regularization techniques
* Experiment with alternative train-test splitting strategies

### Cross-Market Analysis

* Investigate why cryptocurrency (e.g., Bitcoin) forecasts performed significantly worse than equities
* Extend analysis to other financial markets such as real estate or commodities

## 13. Final Remarks

Although the hybrid ARIMA-GARCH model did not outperform traditional approaches as initially expected, this project successfully delivered valuable insights into time series forecasting for financial markets. The findings emphasize the importance of **model interpretability, proper configuration, and empirical evaluation**.

Overall, this project demonstrates strong analytical reasoning, practical implementation skills, and a data-driven mindset—providing a solid foundation for future work in **data science, quantitative finance, and machine learning**.
