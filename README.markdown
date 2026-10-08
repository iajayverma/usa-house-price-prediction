# USA Housing Price Prediction

## Overview
This project demonstrates a basic machine learning workflow for predicting housing prices using a sample dataset from Kaggle. The dataset contains features related to housing areas in the USA, and the goal is to train and evaluate multiple regression models to predict the `Price` of houses.

The analysis includes data preprocessing (handling missing values, scaling), model training, evaluation using metrics like MSE, R2, MAE, and RMSE, and visualizations such as scatter plots and residual distributions. Models compared include Linear Regression, Decision Tree Regressor, Random Forest Regressor, and Gradient Boosting Regressor.

## Dataset
The dataset used is `USA_Housing.csv`, which includes the following columns:
- `Avg. Area Income`: Average income of residents in the area.
- `Avg. Area House Age`: Average age of houses in the area.
- `Avg. Area Number of Rooms`: Average number of rooms in houses.
- `Avg. Area Number of Bedrooms`: Average number of bedrooms in houses.
- `Area Population`: Population of the area.
- `Price`: Target variable - the price of the house (to predict).
- `Address`: Address of the house (dropped during preprocessing as it's not numerical).

This is a synthetic dataset commonly used for regression practice. It can be downloaded from [Kaggle](https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset) or similar sources.

## Requirements
- Python 3.x
- Libraries: 
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn (sklearn)

Install dependencies using:
```
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Usage
1. Place the `USA_Housing.csv` file in the same directory as the script.
2. Run the Python script:
   ```
   python usa_housing_data.py
   ```
   
The script will:
- Load and preprocess the data (handle missing values, drop unnecessary columns, scale features).
- Split the data into training (70%) and testing (30%) sets.
- Train four regression models.
- Generate predictions and evaluate performance.
- Output metrics (MSE, R2, MAE, RMSE) for each model.
- Display visualizations (scatter plots of predictions vs actual, residual distributions).
- Rank models based on MSE (lower is better) and R2 (higher is better).

## Models Trained
- **Linear Regression**: A simple linear model assuming a linear relationship between features and target.
- **Decision Tree Regressor**: A tree-based model that splits data based on feature thresholds.
- **Random Forest Regressor**: An ensemble of decision trees for improved generalization.
- **Gradient Boosting Regressor**: An ensemble method that builds models sequentially to correct errors.

## Results
The script computes and prints evaluation metrics for each model on the test set. Example output structure:
```
Linear Regressor
==============================
MSE: <value>
R2: <value>
MAE: <value>
RMSE: <value>
==============================

... (similar for other models)
```

Model rankings are provided based on MSE (lower values indicate better performance) and R2 (higher values indicate better fit).

Visualizations help assess model fit:
- Scatter plots: Compare predicted vs actual prices (ideal line shown for reference).
- Residual distributions: Check for normality of errors.

Based on typical runs with this dataset:
- Random Forest and Gradient Boosting often perform best due to handling non-linear relationships.
- Linear Regression provides a baseline but may underperform if relationships are complex.

## Contributing
Feel free to fork this repository and submit pull requests for improvements, such as hyperparameter tuning or additional models.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.