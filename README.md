# 🚲 Bike Sharing Demand Prediction

## 📌 Introduction
Bike-sharing systems provide an efficient and eco-friendly mode of transportation in urban areas. Accurately predicting bike rental demand is crucial for optimizing fleet management and enhancing user experience. This project aims to develop a predictive model to forecast the total count of bike rentals based on historical rental data and various environmental and temporal factors.

## 🎯 Aim
The objective of this project is to predict the total number of bikes rented (count) per hour using machine learning techniques. The dataset includes various factors such as weather conditions, seasonality, and user type, which influence rental demand. By leveraging this data, we aim to build a robust model that can generalize well to unseen test data.

## 📂 Dataset Description
The dataset contains hourly bike rental data spanning two years. The training set consists of the first 19 days of each month, while the test set includes the 20th to the end of each month. The goal is to predict the hourly rental counts for the test set using only information available before the rental period.

### 🏷 Data Fields:
- **datetime 📆** – Timestamp of rental record (hourly format)
- **season 🍂** – Season indicator (1: Spring, 2: Summer, 3: Fall, 4: Winter)
- **holiday 🎉** – Whether the day is a holiday (0: No, 1: Yes)
- **workingday 💼** – Whether the day is a working day (0: No, 1: Yes)
- **weather ☁️** – Weather condition categories:
    - 1: Clear, Few clouds, Partly cloudy
    - 2: Mist, Cloudy, Broken clouds
    - 3: Light Snow, Light Rain, Thunderstorm
    - 4: Heavy Rain, Snow, Fog
- **temp 🌡** – Temperature in Celsius
- **atemp 🌡** – "Feels like" temperature in Celsius
- **humidity 💧** – Relative humidity percentage
- **windspeed 🍃** – Wind speed
- **casual 🚴** – Number of non-registered user rentals
- **registered 🏅** – Number of registered user rentals
- **count 🔢** – Total number of bike rentals (Target variable)

## 🏁 Conclusion

### 🔍 Summary of Model Performance
In this project, we aimed to predict the hourly bike rental demand using various machine learning and deep learning models. We evaluated the models using R² Score, Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE). The results show that XGBoost Regressor performed the best among all models, achieving:

- **R² Score**: 0.9282
- **RMSE**: 41.60
- **MAE**: 28.40

Other models such as Random Forest and Gradient Boosting also showed competitive performance, but were slightly less accurate. Traditional regression models like Ridge, Linear Regression, Lasso, and ElasticNet had lower R² scores, indicating they might not be well-suited for capturing complex relationships in the data.

### 🤖 Deep Learning Performance
Additionally, we implemented a deep learning model, which achieved:

- **R² Score**: 0.8916
- **MSE**: 51.13

This suggests that deep learning was able to capture underlying patterns well but did not outperform XGBoost in this case.

## 📌 Key Takeaways
- **XGBoost Regressor** achieved the highest accuracy, making it the best model for predicting bike rental demand.
- Deep learning performed well, but did not surpass ensemble methods like XGBoost and Random Forest.
- **Feature engineering** and **hyperparameter tuning** played a crucial role in improving model performance.
- Future improvements could include trying advanced neural network architectures or fine-tuning hyperparameters further.

Based on these findings, **XGBoost** is recommended as the final model for deployment. 🚀

## 📝 Kaggle Notebook
For a detailed exploration and code implementation, visit the original [Kaggle Notebook](https://www.kaggle.com/code/senasudemir/bike-sharing-demand-prediction?scriptVersionId=222401587).
