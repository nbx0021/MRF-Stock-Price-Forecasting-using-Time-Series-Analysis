# **MRF Stock Price Forecasting using Time Series Analysis**

## **📌 Project Overview**
Stock market predictions are crucial for investment decisions. This project focuses on **MRF stock price forecasting** using **Time Series Analysis** techniques like **ARIMA and SARIMA**. The goal is to analyze historical data, identify patterns, and build a reliable predictive model.

## **🔍 Key Steps in Analysis**
### **1️⃣ Data Preprocessing & Visualization**
- Loaded MRF stock price data.
- Handled missing values and formatted date columns.
- Visualized stock price trends over time.

### **2️⃣ Stationarity Check & Data Transformation**
- Used **ADF Test** to check stationarity.
- Applied **differencing & Box-Cox transformation** to make data stationary.
- Visualized **ACF & PACF plots** to identify AR and MA terms.

### **3️⃣ Model Selection (Auto-ARIMA & Manual Tuning)**
- Used **Auto-ARIMA** to select the best **(p,d,q) and (P,D,Q,S)** values.
- Built and compared **ARIMA and SARIMA** models.

### **4️⃣ Model Evaluation**
- Evaluated models using:
  - **AIC & BIC (Model Selection Criteria)**
  - **RMSE (Root Mean Square Error)**
  - **MAPE (Mean Absolute Percentage Error)**
- Checked residuals for normality and randomness.

### **5️⃣ Forecasting & Interpretation**
- Forecasted future stock prices using the best model.
- Visualized predictions with confidence intervals.

## **📊 Final Results**
| Model  | AIC | BIC | RMSE | MAPE |
|--------|------------|------------|------------|------------|
| ARIMA  | 37408.56   | 37419.96   | 1365.61    | 1.21%      |
| SARIMA | 37413.95   | 37436.75   | 1468.13    | 1.31%      |

**Conclusion:** ARIMA performed better than SARIMA, indicating that seasonal components had minimal impact on MRF stock price movements.

## **📂 Repository Structure**
```
├── data
│   ├── mrf_stock_prices.csv  # Raw dataset
├── notebooks
│   ├── mrf_stock_forecasting.ipynb  # Jupyter Notebook with full analysis
├── images
│   ├── stock_trend.png  # Stock price trend visualization
│   ├── acf_pacf.png  # ACF & PACF plots
│   ├── forecast_plot.png  # Final forecast results
├── README.md  # Project documentation
```

## **🔧 How to Run the Project?**
### **📌 Prerequisites**
- Python 3.8+
- Jupyter Notebook
- Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn statsmodels pmdarima
```

### **📌 Run the Jupyter Notebook**
1. Open the notebook: `MRF stock prices analysis.ipynb`
2. Run all the cells step by step.
3. Analyze the model performance and forecast results.

## **🛠️ Future Improvements**
- 📌 Use **LSTM (Deep Learning) for forecasting**.
- 📌 Include **external economic indicators** (inflation, interest rates) for better predictions.
- 📌 Deploy model using **Flask/Django for real-time predictions**.



