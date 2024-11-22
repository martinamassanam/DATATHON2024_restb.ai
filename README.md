# AUTOMATED VALIDATION MODEL - DATATHON 2024 - restb.ai CHALLENGE

## Introduction

This project aims to assist real estate agents by providing a data-driven approach to property pricing. Using property characteristics and historical data, we developed a machine learning model to accurately estimate property prices.

The dataset provided was based on real data collected in Illinois last year. We were given data from the last 8 months and tasked with predicting property prices for the next 2 months.

## Data Preprocessing
### Data Augmentation

We incorporated additional information about Median Household Income, enhancing the dataset with socioeconomic insights that could influence property prices.

### Data Cleaning

The dataset underwent rigorous cleaning to handle missing values and ensure data consistency.

#### Categorical Features

**One-Hot Encoding:** Due to the large number of categorical attributes, we applied one-hot encoding to convert them into numerical format. After encoding, we calculated the correlation of each feature with the target variable (Close Price). Only features with a correlation greater than 0.2 were retained for modeling.

#### Numerical Features

**Missing Value Imputation:**
For numerical features, we applied different methods for handling missing values:
* Mean Imputation: For attributes whose values could be derived from other columns.
* KNN Imputation: For attributes with a strong dependency on other features and significant impact on the target.

**Outlier Removal:**
To handle outliers, we used the Interquartile Range (IQR) method: Data points outside the 10th percentile and 90th percentile ranges were removed.

## Modeling  
We applied both linear and non-linear models to evaluate the dataset's predictive capabilities. Each model was tested with different parameters to identify the optimal configuration and achieve the best possible results.

### Linear Models  
- **Linear Regression**  
- **Lasso Regression**  
- **Ridge Regression**  

### Non-Linear Models  
- **K-Nearest Neighbors (KNN)**  
- **Regression Trees**  
- **Extra Trees Regressor**  
- **Random Forest**  
- **Gradient Boosting Regressor**  

### Best Model  
After evaluating all models on the test set, the **Gradient Boosting Regressor** outperformed others in terms of **Mean Absolute Error (MAE)** and **Mean Squared Error (MSE)**. 

## Contributors

- Project Team: Martina Massana, Maria Sans, Alba Ungueti, Raquel Jolis  
- Special Thanks: AED, FME, RestbAI, and all other collaborators who supported this Datathon




