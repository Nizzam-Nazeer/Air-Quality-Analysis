## **Air Quality Analysis**
## Overview  
This analysis focuses on developing a machine learning regression model to predict Nitrogen Oxides (NOx) concentrations using data from a gas multisensor device. Accurate prediction of NOx levels can contribute to better public health measures and environmental management, as air pollution from NOx significantly affects human health, ecosystems, and climate.


## Workflow

1. **Data Collection:**
   - Collected the dataset "AirQualityUCI.csv," which includes hourly air quality readings from a gas sensor array.

2. **Data Preprocessing:**
   - Replaced missing values (represented as `-200`) with `NaN` and imputed missing values using the mean of the respective columns.
   - Managed outliers using Winsorization to minimize their effect on the model's performance.

3. **Exploratory Data Analysis (EDA):**
   - Visualized the data distribution to identify patterns, trends, and anomalies.
   - Created a correlation matrix heatmap to assess relationships between different features and the target variable (NOx).

4. **Feature Selection:**
   - Used **SelectKBest** with the F-test to identify the most relevant features affecting NOx predictions, reducing dimensionality and improving model efficiency.

5. **Model Training and Evaluation:**
   - Split the dataset into **training (80%)** and **testing (20%)** sets for validation.
   - Scaled features using **StandardScaler** to ensure uniformity in data.
   - Trained various regression models:
     - **Linear Regression**
     - **Random Forest Regressor**
     - **Gradient Boosting Regressor**
     - **Support Vector Regressor (SVR)**
     - **Multi-Layer Perceptron (MLP) Regressor**
   - Evaluated model performance using metrics such as **Mean Squared Error (MSE)**, **Root Mean Squared Error (RMSE)**, **Mean Absolute Error (MAE)**, and **R² Score**.

6. **Hyperparameter Tuning:**
   - Used **GridSearchCV** to optimize the hyperparameters of the **Random Forest Regressor**, improving its predictive performance.

7. **Model Deployment:**
   - Created a robust pipeline that combines preprocessing and model predictions.
   - Saved the trained model using **joblib** for future applications.

8. **Prediction:**
   - The final model was tested on unseen data to evaluate its performance in real-world scenarios.

## Results

- **Model Performance:**  
  The **Random Forest Regressor** emerged as the best-performing model, achieving the highest R² score and the lowest RMSE among all evaluated models. This suggests that the model can predict NOx levels accurately within acceptable tolerances, making it suitable for air quality management applications.

- **Feature Importance:**  
  The analysis identified the most important features influencing NOx concentrations, which could help inform future environmental research and policymaking decisions.


## Conclusion

This analysis successfully developed a machine learning regression model capable of accurately predicting Nitrogen Oxides (NOx) concentrations using multisensor data. The project addressed challenges related to data quality, feature selection, and model optimization. The resulting model can be applied for real-time NOx concentration predictions, contributing to improved public health initiatives and enhanced environmental monitoring.


