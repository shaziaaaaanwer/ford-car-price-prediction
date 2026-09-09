# Ford Car Price Prediction

A machine learning regression project that predicts the price of Ford cars based on features such as model, year, mileage, transmission, fuel type, tax, MPG, and engine size.

## Project Overview

The goal of this project is to build a machine learning model that can predict the price of a Ford car from its available specifications.

The project covers the complete machine learning workflow:

- Data cleaning
- Exploratory Data Analysis (EDA)
- Feature preprocessing
- Train/test splitting
- Linear Regression baseline
- Random Forest Regression
- Hyperparameter tuning
- Model evaluation
- Feature importance analysis
- Price prediction for new cars
- Model saving and loading

## Dataset

The dataset contains information about Ford cars, including:

- Model
- Year
- Price
- Transmission
- Mileage
- Fuel Type
- Tax
- MPG
- Engine Size

The dataset was obtained from Kaggle.

## Data Cleaning

The following cleaning steps were performed:

- Removed duplicate rows
- Removed an invalid year value
- Removed records with zero engine size
- Removed leading/trailing whitespace from categorical values
- Verified that there were no missing values

After cleaning, the dataset contained 17,760 records.

## Exploratory Data Analysis

EDA was performed to understand the relationships between car features and price.

Some important observations included:

- Newer cars generally have higher prices.
- Cars with higher mileage generally have lower prices.
- Engine size has a relationship with price, although the relationship is not completely linear.
- Year and mileage showed a strong negative correlation.

## Machine Learning

### Preprocessing

Categorical features were converted into numerical features using One-Hot Encoding.

A `ColumnTransformer` and `Pipeline` were used to combine preprocessing and model training.

### Models

Two regression models were tested:

1. Linear Regression
2. Random Forest Regression

Linear Regression was used as a baseline model, while Random Forest was used to capture more complex relationships between the features and car prices.

### Hyperparameter Tuning

Random Forest hyperparameters were tuned using `RandomizedSearchCV` with 5-fold cross-validation.

The tuning process explored parameters including:

- Number of estimators
- Maximum tree depth
- Minimum samples required for splitting
- Minimum samples required at a leaf

## Model Evaluation

The models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

The Random Forest model performed substantially better than the Linear Regression baseline.

## Feature Importance

Feature importance was analyzed to understand which variables contributed most to the model's predictions.

The analysis showed that features such as car year, engine size, mileage, and car model played important roles in predicting price.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

## Project Structure

```text
ford-car-price-prediction/
│
├── ford_car_price_prediction.ipynb
├── ford_car_price_model.pkl
├── README.md
├── requirements.txt
└── .gitignore
```
## Future Improvements

Possible improvements to this project include:

- Deploying the model as a web application
- Testing additional regression algorithms
- Performing more extensive feature engineering
- Adding more visualizations
- Improving model interpretability
