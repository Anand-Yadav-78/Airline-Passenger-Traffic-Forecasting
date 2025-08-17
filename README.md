# **Airline-Passenger-Traffic-Forecasting**

This repository contains an end-to-end time series forecasting project focused on predicting monthly airline passenger traffic. The primary goal is to build a robust and accurate SARIMA (Seasonal AutoRegressive Integrated Moving Average) model that captures both long-term growth trends and seasonal patterns in air travel data.
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **📋 Problem Statement**
Effective management in the aviation industry hinges on accurate demand forecasting. Airlines and airports need reliable predictions of passenger traffic to optimize capacity planning, resource allocation, and overall business strategy. This project addresses this challenge by moving beyond simple historical averages to build a statistical model that can accurately forecast future passenger numbers by learning from past seasonal variations and growth trends.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
# **📊 Data Summary**
The analysis is based on a univariate time series dataset containing monthly airline passenger counts over several years.

Variables:

Month: The time period of observation (monthly frequency).

Passengers: The total number of airline passengers recorded for that month.

Nature of Data: The dataset exhibits a clear upward trend over time, coupled with strong and consistent annual seasonality, making it a classic use case for time series forecasting models.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
# **🛠️ Methodology & Techniques**
To ensure the model is both accurate and statistically sound, a systematic time series methodology was employed.

Data Preprocessing: The raw data was loaded, cleaned, and the Month column was converted to a datetime index to structure the data for time series analysis.

Exploratory Data Analysis (EDA): A comprehensive EDA was performed to understand the data's underlying structure. Key techniques included:

Time Series Decomposition: Separating the data into its trend, seasonality, and residual components.

Rolling Statistics: Plotting the rolling mean and standard deviation to visually assess the trend and volatility.

Stationarity Check: The Augmented Dickey-Fuller (ADF) test was used to statistically test for stationarity. Differencing was applied to the series to make it stationary, a critical requirement for ARIMA-based models.

Model Selection & Training: A SARIMA (p, d, q)(P, D, Q, m) model was chosen to effectively handle both the non-seasonal and seasonal patterns. The optimal model parameters were determined using the auto_arima function.

Model Evaluation & Diagnostics: The model's performance was rigorously evaluated on a hold-out test set.

Accuracy Metrics: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE).

Residual Analysis: The model's residuals were checked to ensure they behaved like white noise, using ACF/PACF plots and the Ljung-Box test.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
# **🚀 Tools and Libraries**
This project was built using Python and the following core data science libraries:

Pandas: For data manipulation and time series indexing.

NumPy: For numerical operations.

Statsmodels: For statistical modeling, including the SARIMA implementation and diagnostic tests (ADF, Ljung-Box).

pmdarima: For the auto_arima function to automate hyperparameter tuning.

Matplotlib: For data visualization and plotting forecasts.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
# **💡 Inference and Conclusion**
The SARIMA model successfully captured the complex patterns in the data, yielding a highly accurate forecast with a Mean Absolute Percentage Error (MAPE) of just 2.87%.

The key insights derived from the analysis are:

Strong Growth Trajectory: The model confirms a consistent upward trend in passenger traffic, projecting an 8-10% annual growth rate through 2026.

Pronounced Seasonality: Clear travel peaks were identified and forecasted for May-June (summer holidays) and December-January (year-end festivities).

Model Robustness: The residual analysis confirmed that the model's errors are random and unpredictable (white noise), indicating that all systematic patterns in the data have been successfully extracted.

Final Conclusion: 
This project demonstrates the effectiveness of the SARIMA model for forecasting airline passenger demand. The resulting predictions are accurate enough to be a reliable tool for airline operators and airport authorities. By leveraging these forecasts, stakeholders can make informed, data-driven decisions regarding fleet management, route expansion, staffing levels, and long-term infrastructure investments, ultimately leading to more efficient and profitable operations.
