## Project 1: Gradient Boosting Regressor
![image](https://miro.medium.com/v2/resize:fit:640/format:webp/1*NLI9QFoWDltdXJf3_rwbbw.png)

### Data Preprocessing

1. **Data Import**: The dataset is imported from `BostonHousing.csv`.
2. **Initial Data Analysis**: The dataset is examined using functions such as `head()`, `info()`, and `describe()` to get an understanding of its structure and basic statistics.
3. **Data Cleaning**: Missing values and duplicates are removed using `isnull().sum()` and `duplicated().sum()`. The column `rm`, which contains missing values, is removed using `dropna(axis=1, inplace=True)`.

### Data Visualization

To better understand the relationships between the variables, the data is visualized using heatmaps and pair plots. These visualizations help in identifying key features that are most relevant to predicting housing prices.

- **Heatmaps** are used to display the correlation matrix, showing relationships between features.
- **Pair plots** provide a more detailed view of relationships between pairs of variables.

### Model Building

1. **Splitting the Data**: The dataset is split into training and test sets using `train_test_split` from Scikit-learn.
2. **Training the Model**: A **Gradient Boosting Regressor** model is built with parameters `max_depth=2`, `n_estimators=3`, and `learning_rate=1.0`.
3. **Prediction**: The model is used to predict housing prices on the test set.
4. **Evaluation**: The model's performance is evaluated using the following metrics:
   - **Mean Absolute Error (MAE)**
   - **Mean Squared Error (MSE)**
   - **R-squared (R²)**

### Results of the Initial Model

- **Mean Absolute Error**: 4.82
- **Mean Squared Error**: 57.83
- **R-squared**: 0.17

### Feature Importance

The importance of the features in the Gradient Boosting model is visualized using a bar chart. This chart shows the relative significance of each feature in predicting housing prices.

### Hyperparameter Optimization

To improve the performance of the model, hyperparameter tuning is conducted using **GridSearchCV** to find the best values for `n_estimators` and `learning_rate`. 

1. **Best Parameters Found**:
   - `learning_rate=0.05`
   - `n_estimators=150`
2. **Retraining the Model**: The Gradient Boosting Regressor is retrained using these optimized parameters.
3. **Re-evaluation**: The model's performance is re-evaluated with the optimized parameters.

### Results of the Optimized Model

- **Mean Absolute Error**: 4.82
- **Mean Squared Error**: 57.83
- **R-squared**: 0.17

Despite hyperparameter tuning, the results of the model did not show significant improvement.
