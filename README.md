# Smart Water Monitoring System 🌍💧

This repository contains the solution for the **HackerEarth World Water Day Challenge**, focused on predicting water consumption using various machine learning models. The objective was to develop an efficient predictive model based on given dataset features.

![image](https://github.com/user-attachments/assets/afc26b72-8842-46b4-a801-29a29c9dfea3)


## Dataset Features
- **Residents**
- **Apartment_Type**
- **Temperature**
- **Humidity**
- **Water_Price**
- **Period_Consumption_Index**
- **Income_Level**
- **Guests**
- **Amenities**
- **Appliance_Usage**
- **Water_Consumption** (Target variable)

## Data Preprocessing
- Categorical missing values filled with 'missing'.
- Temperature imputed using the mean of 3 previous and 3 future non-NaN values.
- Normalization and feature scaling applied where required.

## Model Performance

| Model                 | Hyperparameters                                     | Score     |
|-----------------------|-------------------------------------------------|----------|
| Linear Regression     | -                                             | 38.39208 |
| Ridge Regression      | {'alpha': 1.1}                              | 38.39396 |
| Lasso Regression      | {'alpha': 0.001}                           | 38.39240 |
| Decision Tree        | {'min_samples_split': 8, 'min_samples_leaf': 9, 'max_depth': 18} | 72.16152 |
| Random Forest        | {'n_estimators': 200, 'min_samples_split': 2, 'max_depth': 20} | 77.82399 |
| Support Vector Machine | {'kernel': 'linear', 'epsilon': 0.112, 'C': 8.1113} | 36.87689 |
| Elastic Net          | {'l1_ratio': 0.6667, 'alpha': 0.0414}       | 38.39250 |
| Huber Regression     | {'epsilon': 1.9273, 'alpha': 0.0516}        | 33.08052 |
| Bayesian Ridge       | {'n_iter': 300, 'alpha_2': 3.5e-06, 'alpha_1': 1e-05} | 38.39763 |
| Poisson Regressor    | {'max_iter': 500, 'alpha': 0.6768}          | 38.45018 |
| Quantile Regressor   | -                                             | -        |
| MLP (Neural Net)     | {'hidden_layer_sizes': (50, 50), 'alpha': 0.0162, 'activation': 'relu'} | 57.91662 |
| ADA Boost            | {'n_estimators': 50, 'learning_rate': 0.49, 'estimator__max_depth': 4} | 68.12962 |
| Gradient Boosting    | {'n_estimators': 100, 'max_depth': 5, 'learning_rate': 0.2} | 83.25269 |
| XGBoost             | {'n_estimators': 100, 'max_depth': 5, 'learning_rate': 0.2} | 82.59506 |
| LightGBM            | {'n_estimators': 100, 'max_depth': 5, 'learning_rate': 0.2} | 82.95723 |
| CatBoost            | {'learning_rate': 0.31, 'iterations': 300, 'depth': 6} | 83.91909 |
| KNN Regressor       | {'weights': 'distance', 'n_neighbors': 19}  | 47.91746 |

### Ensemble Methods

| Model Combination  | Method  | Score     |
|--------------------|---------|----------|
| CatBoost, GBR, LGBM | Vote    | 83.90627 |
| CatBoost, GBR, LGBM | Stack (Linear) | 84.05251 |
| Top 10 Models      | Stacking / RF  | 83.6511  |
| Top 5 Models      | Stacking / RF  | 83.47601 |
| Top 10 Models      | Stacking / MLP | 83.89934 |

## Final Result
- **Rank**: 93
- **Score**: 84.05251
- **Participant**: Diwakar Sehgal


## Conclusion
The best performing model was the **Stacked (Linear) Ensemble** of CatBoost, GBR, and LGBM, achieving an **84.05251 score**. Future improvements could include hyperparameter tuning, feature engineering, and alternative ensemble strategies.

