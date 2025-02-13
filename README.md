## 1. Introduction

The 17 Sustainable Development Goals (SDGs) set by the United Nations (UN) focus on addressing global challenges, including poverty, economic growth, and climate change. Goal 8 specifically targets economic growth and decent jobs for all. Cryptocurrencies and blockchain technology offer transformative potential to support these goals, particularly in promoting financial inclusion, enhancing economic empowerment, reducing transaction costs, and fostering entrepreneurship in underserved communities.

This study explores how machine learning can be leveraged to predict cryptocurrency prices, focusing on volatility and external factors such as government regulations. Using an open-source, low-code Python library called **PyCaret**, the study evaluates various machine learning regression models to predict the closing prices of the top five cryptocurrencies: Bitcoin, Ethereum, Tether, Binance Coin, and Ripple. 

## 2. Literature Review

Cryptocurrency markets display distinct characteristics such as high volatility and continuous trading, making them challenging to predict. Various methodologies, including random forest, artificial neural networks, and support vector machines (SVM), have been explored for forecasting. Sentiment analysis and external economic factors also play a significant role in the accuracy of these predictions.

This study compares the effectiveness of popular machine learning regression models in predicting cryptocurrency prices, focusing on data-driven decisions and profitability improvement.

## 3. Data Collection

### 3.1. Data Sources

Data for this study was collected using the `yfinance` Python library, which provides historical and real-time financial data. The datasets include:

- **Top 5 Cryptocurrencies (BTC, ETH, USDT, BNB, XRP)**: Data includes Open, High, Low, Close, and Volume.
- **Indian Market Indices**: BSE Sensex, Nifty 50, Nifty Midcap 150, Nifty 100.
- **Top 5 Commodities**: Gold, Silver, Crude Oil, Natural Gas, Aluminum.
- **Top 5 Economies of the World**: Exchange rates for the US, UK, Japan, Germany.

### 3.2. Timeframe

Data was collected from September 2014 to November 2024 with a daily frequency.

| Dataset | Number of Records | From | To |
|---------|-------------------|------|-----|
| Bitcoin (BTC-INR) | 3709 | September 17, 2014 | November 12, 2024 |
| Ethereum (ETH-INR) | 2558 | November 11, 2017 | November 12, 2024 |
| Binance Coin (BNB-INR) | 2558 | November 11, 2017 | November 12, 2024 |
| Tether USDT (USDT-INR) | 2558 | November 11, 2017 | November 12, 2024 |
| Ripple (XRP-INR) | 2558 | November 11, 2017 | November 12, 2024 |
| Commodities | 3991 | September 17, 2014 | November 12, 2024 |
| Market Indices | 3904 | September 17, 2014 | November 12, 2024 |

## 4. Data Pre-Processing

The data was merged using an outer join based on date, resulting in 5199 records. Null values were removed, and the final dataset, containing 1670 records, was split into 1336 records for training and 336 records for testing. Robust scaling was applied for standardization to address skewness and kurtosis in the data.

## 5. Feature Selection

Feature selection was conducted based on the correlation coefficient. Features with correlation values between 0.7 and 0.9 were selected for further analysis.

## 6. Data Analysis and Model Building

The **PyCaret** Python library was used for data analysis and model building. PyCaret streamlines the entire machine learning workflow, from feature engineering and preprocessing to model evaluation and deployment. Key machine learning models used in this study include:

- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Gradient Boosting Regressor**
- **Light Gradient Boosting Machine (LightGBM)**
- **Random Forest Regressor**
- **XGBoost**
- **K Neighbors Regressor**

Each model was evaluated based on its ability to predict the closing prices of cryptocurrencies, and hyperparameters were tuned for optimal performance.

## 7. Technology Used

- **Python**: The primary programming language used for data analysis, preprocessing, and machine learning model development.
- **PyCaret**: An open-source, low-code machine learning library that simplifies the process of model building, evaluation, and deployment.
- **yfinance**: A Python library used to collect historical financial data from Yahoo Finance.
- **Pandas**: For data manipulation and preprocessing.
- **NumPy**: For numerical operations.
- **Matplotlib/Seaborn**: For data visualization, including the correlation heatmap.


## 8. Conclusion

In conclusion, this research investigates a range of regression models to predict cryptocurrency closing prices, specifically for BTC, ETH, BNB, and USDT. Models like Linear Regression (LR), Bayesian Ridge (BR), and Lasso Least Angle Regression (LLAR) demonstrated high accuracy and efficiency, particularly with BTC and ETH, and maintained low prediction error.

On the other hand, complex models like LightGBM, Extra Trees (ET), and Random Forest (RF) show slightly higher RMSE values and increased computation times, making them less suitable for real-time applications despite their predictive power.

Models like Dummy Regressor, Elastic Net, and Orthogonal Matching Pursuit (OMP) exhibited high error rates, making them impractical for precise forecasting.

To conclude, simple models are more effective in predicting the prices of cryptocurrencies. They also offer a balance of computational efficiency and high accuracy.

## 🌍 Explore More Projects  
For more exciting machine learning and AI projects, visit **[The iVision](https://theivision.wordpress.com/)** and stay updated with the latest innovations and research! 🚀  

---
