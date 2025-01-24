# Regression Models on California Housing Dataset  

This project demonstrates the implementation and comparison of various regression algorithms using the California Housing dataset from the sklearn library. The objective is to predict house prices and evaluate the performance of each algorithm using metrics such as **Mean Squared Error (MSE)**, **Mean Absolute Error (MAE)**, and **R-squared (R²)** scores.  

---

## Table of Contents
- [Introduction](#introduction)  
- [Dataset](#dataset)  
- [Preprocessing](#preprocessing)  
- [Regression Algorithms](#regression-algorithms)  
- [Model Comparison](#model-comparison)  
- [Conclusion](#conclusion)  

---

## **Introduction**  
The aim of this project is to apply and evaluate the following regression models:  

1. **Linear Regression**  
2. **Decision Tree Regressor**  
3. **Random Forest Regressor**  
4. **Gradient Boosting Regressor**  
5. **Support Vector Regressor (SVR)**
6. **AdaBoost Regressor**
7. **MLP Regressor** 

Each model is assessed based on its ability to predict housing prices accurately, and the results are compared using standard regression metrics.  

---

## **Dataset**  
The **California Housing dataset** from sklearn contains housing information, including median house prices, across California districts.  

- **Target:** Median house price (in 100,000s).  
- **Features:** Includes metrics like median income, house age, population, and proximity to the ocean.  

---

## **Preprocessing**  

1. **Loading the Data:**  
   Dataset loaded using `fetch_california_housing` from sklearn.  

2. **Handling Missing Values:**  
   Ensured no missing values existed.  

3. **Duplicate Rows:**  
   Checked and removed duplicates (if any).  

4. **Removing Outliers:**  
   Applied the IQR method to remove outliers.  

5. **Feature Scaling:**  
   Used `StandardScaler` to standardize features to ensure uniform input for models sensitive to scale.  

6. **Train-Test Split:**  
   Divided the data into training and testing sets (80% training, 20% testing).  

---

## **Regression Algorithms**  
The following regression models were implemented:  

1. **Linear Regression**  
   - A simple linear approach that models the relationship between input features and the target variable by fitting a straight line.  

2. **Decision Tree Regressor**  
   - A non-linear model that partitions the data into regions based on feature thresholds, creating a tree-like decision structure.  

3. **Random Forest Regressor**  
   - An ensemble model that builds multiple decision trees and averages their predictions to improve accuracy and reduce overfitting.  

4. **Gradient Boosting Regressor**  
   - An advanced ensemble technique that builds decision trees sequentially, optimizing for residual errors at each step.  

5. **Support Vector Regressor (SVR)**  
   - A regression model that finds a hyperplane within a margin of tolerance to minimize error, effective for both linear and non-linear data.  

6. **AdaBoost Regressor**  
   - An ensemble method that builds multiple weak learners (typically decision trees) sequentially. Each subsequent learner focuses on the residual errors of the previous one to improve overall performance.  

7. **MLP Regressor**  
   - A multi-layer perceptron (neural network) model that uses backpropagation to optimize weights and minimize error. It is effective for capturing complex non-linear relationships in data.  
---

## **Model Comparison**  
The models were evaluated using the following metrics:  

- **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted values.  
- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.  
- **R-squared (R²):** Explains the proportion of variance captured by the model.  

### **Results:**  
- The **Random Forest Regressor** performed the best with an **R² of 0.82** and the lowest MAE.  
- The **AdaBoostRegressor** showed the lowest performance with an **R² of 0.58**, likely due to overfitting.  

---

## **Conclusion**  
This project highlights the importance of model selection in regression tasks and showcases the effectiveness of ensemble methods like **Random Forest Regressor** for housing price prediction.  
