## Life Expectancy Prediction

### Project Overview

This project aims to predict **life expectancy** based on a wide range of health, economic, and social factors collected by the World Health Organization (WHO). By analyzing features such as adult mortality, infant deaths, GDP, schooling, and various health expenditures, the goal is to develop a regression model that can accurately forecast life expectancy. This is a critical task for public health policy and economic development planning.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Life Expectancy WHO](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who)
  * **Size**: 2938 entries, 22 columns (initial). The dataset has a significant number of missing values.
  * **Key Features**:
      * `Adult Mortality`, `Alcohol`, `Hepatitis B`, `Measles`, `BMI`, `under-five deaths`, `Polio`, `Total expenditure`, `Diphtheria`, `HIV/AIDS`, `GDP`, `Population`, `thinness 1-19 years`, `Income composition of resources`, `Schooling`.
  * **Approach**:
      * **Data Cleaning**: Dropped columns with a high number of missing values (`thinness 5-9 years`, `BMI`, `infant deaths`). The remaining rows with missing values were dropped.
      * **Exploratory Data Analysis**: The code checks basic statistics, null values, duplicates, and unique values.
      * **Label Encoding**: Applied to categorical columns (`Country`, `Status`).
      * **Regression Task**: The target variable is `Life expectancy`.
      * **Models Used**:
          * A suite of regression models were trained, including Linear Regression, Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN).
  * **Best R² Score**:
      * **0.947** with Random Forest Regressor.
      * **0.941** with Bagging Regressor.
      * **0.940** with XGBoost Regressor.
      * The scatter plots and R² scores for the top models show a strong relationship between the actual and predicted life expectancy, indicating good predictive performance.

-----

### Purpose and Applications

  * Enable public health organizations to **forecast life expectancy trends** based on key indicators.
  * Support policymakers in identifying the most critical factors to target for improving public health.
  * Assist in resource allocation for healthcare and education programs.
  * Provide a foundational model for analyzing the complex interconnections between health, social, and economic variables.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Life-Expectancy-Prediction-Using-ML.git
cd Life-Expectancy-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Exploring more robust strategies for handling the missing data instead of simply dropping rows.
  * Performing comprehensive hyperparameter tuning and cross-validation for the top-performing regression models.
  * Investigating alternative feature engineering techniques, such as creating new features from existing health and economic data.
  * Adding explainability (e.g., SHAP or LIME) to understand which factors are the most significant drivers of life expectancy.
