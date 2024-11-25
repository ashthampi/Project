# Project
Rental Price

Model Performance

The provided script evaluates the performance of five regression models on the same dataset using key metrics: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R² Score. Here’s a comparison of the models:

Linear Regression:

RMSE: 0.2446
MAE: 0.1651
R²: 0.7276
Good baseline model but relatively lower R² compared to others.

Decision Tree:

RMSE: 0.0225
MAE: 0.0039
R²: 0.9977
Outstanding fit to the data with near-perfect R², but potential for overfitting.

Random Forest:

RMSE: 0.0921
MAE: 0.0655
R²: 0.9614
Excellent balance between accuracy and generalization, likely less prone to overfitting than the Decision Tree.

Support Vector Regressor (SVR):

RMSE: 0.1851
MAE: 0.1307
R²: 0.8440
Good generalization, though slightly less accurate than Random Forest and Decision Tree.

XGBoost:

RMSE: 0.1960
MAE: 0.1493
R²: 0.8251
Strong model but slightly underperforms compared to Random Forest and Decision Tree.

Decision Tree has the best fit, indicated by the lowest RMSE and MAE, and the highest R². However, its near-perfect performance suggests it may overfit, especially in terms of training data.
Random Forest provides excellent performance with a more generalized approach, making it a likely choice for robust predictions. SVR and XGBoost offer good results but fall behind Random Forest and Decision Tree in accuracy.
Linear Regression, while the simplest, shows decent results, making it a good starting point.



Train and Test Accuracy Evaluation

we evaluated five regression models' performance on training and testing datasets. Metrics include RMSE (Root Mean Squared Error) and R² (coefficient of determination). Here's the summary of the results:

Model Performance

Linear Regression:

Train RMSE: 0.3219 
Test RMSE: 1.54e+14 (Extremely high error)
Train R²: 0.5312 
Test R²: -1.11e+29 (Severely negative, indicating a failure to generalize)
Linear Regression struggles with this dataset, showing a massive generalization issue during testing.

Decision Tree:

Train RMSE: 0.0218 
Test RMSE: 0.2980
Train R²: 0.9979 
Test R²: 0.5853
The Decision Tree performs very well on the training data, but the lower test R² suggests overfitting and reduced generalization ability.

Random Forest:

Train RMSE: 0.0945 
Test RMSE: 0.2393
Train R²: 0.9596 
Test R²: 0.7325
Strong performance on both training and testing datasets, striking a good balance between accuracy and generalization.

Support Vector Regressor (SVR):

Train RMSE: 0.1856 
Test RMSE: 0.3052
Train R²: 0.8442 
Test R²: 0.5649
SVR shows reasonable accuracy but underperforms compared to Random Forest, especially on the test set.

XGBoost:

Train RMSE: 0.1959 
Test RMSE: 0.2322
Train R²: 0.8264 
Test R²: 0.7481
Observation: XGBoost performs well and slightly outperforms Random Forest on the test set, making it a strong contender.

Summary 
Random Forest and XGBoost are the best performers, achieving good generalization (high test R² and low RMSE).
Decision Tree fits the training data exceptionally well but exhibits signs of overfitting on the test data.
Support Vector Regressor shows moderate performance but lags behind Random Forest and XGBoost in generalization.
Linear Regression fails on the test set, suggesting either data-related issues (e.g., non-linearity) or numerical instability.

CONCLUSION

The project successfully developed a machine learning pipeline to predict apartment rental prices using the "Apartment for Rent Classified" dataset. Key steps included data preprocessing, feature engineering, feature selection, model training, and hyperparameter tuning. Random Forest emerged as the best-performing model with well-optimized hyperparameters, providing a good balance between training and testing accuracy. The process emphasized the importance of handling missing values, encoding categorical features, and normalizing data for robust model performance. While the results are promising, incorporating additional features and exploring advanced modeling techniques can further enhance prediction accuracy.
