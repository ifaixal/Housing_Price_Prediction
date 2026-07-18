# Ames Housing Price Prediction

A machine learning project that predicts residential house prices using the Ames Housing Dataset. This project follows a complete supervised machine learning workflow, from data preprocessing and exploratory data analysis (EDA) to model training, evaluation, and comparison.

---

## Project Overview

The objective of this project is to build regression models capable of predicting a house's sale price based on its physical characteristics and location.

The project emphasizes understanding the machine learning workflow rather than simply obtaining the highest predictive accuracy.

---

## Dataset

- **Dataset:** Ames Housing Dataset
- **Problem Type:** Supervised Learning
- **Task:** Regression
- **Target Variable:** `SalePrice`

The dataset contains numerous numerical and categorical features describing residential properties in Ames, Iowa.

---

## Machine Learning Workflow

### 1. Data Cleaning

- Identified missing values
- Treated missing categorical values
- Treated missing numerical values
- Preserved meaningful missing values (e.g., "No Garage", "No Pool") instead of blindly imputing them

---

### 2. Exploratory Data Analysis (EDA)

Performed extensive EDA to better understand the dataset.

#### Univariate Analysis

- Distribution of numerical features
- Distribution of categorical features
- Target variable (`SalePrice`) distribution
- Skewness analysis
- Outlier detection

#### Bivariate Analysis

- Numerical features vs. SalePrice
- Categorical features vs. SalePrice

#### Correlation Analysis

Identified the strongest predictors of house price, including:

- OverallQual
- GrLivArea
- GarageCars
- GarageArea
- TotalBsmtSF
- YearBuilt
- YearRemodAdd
- 1stFlrSF
- FullBath
- MasVnrArea
- OpenPorchSF

Outliers were investigated but not removed indiscriminately, since unusual observations are not necessarily data errors.

---

### 3. Feature Engineering

- Categorical encoding
- Numerical preprocessing
- Feature scaling where appropriate

---

### 4. Model Training

The following regression models were implemented:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- Gradient Boosting Regressor

---

### 5. Model Evaluation

Models were evaluated using:

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- 5-Fold Cross Validation

---

## Results

| Model | Test RMSE | Test MAE |
|--------|----------:|---------:|
| Lasso Regression | **0.2699** | 0.1868 |
| Ridge Regression | 0.2714 | 0.1867 |
| Gradient Boosting | 0.2778 | 0.1947 |
| Random Forest | 0.2980 | 0.2062 |
| Linear Regression | 0.3113 | 0.1844 |

### Cross Validation (Average RMSE)

| Model | CV RMSE |
|--------|--------:|
| **Lasso Regression** | **0.3038** |
| Gradient Boosting | 0.3073 |
| Ridge Regression | 0.3112 |
| Random Forest | 0.3404 |
| Linear Regression | 0.3619 |

Among the evaluated models, **Lasso Regression** achieved the best overall performance.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## Project Structure

```
├──── AmesHousing.csv
│
├──── Python.ipynb
│
├──── Data Dictoinary.txt
│
├── README.md
```

---

## Key Learnings

This project provided practical experience with:

- Handling missing values
- Performing exploratory data analysis
- Understanding feature relationships
- Detecting and interpreting outliers
- Building multiple regression models
- Cross-validation
- Hyperparameter tuning
- Comparing model performance using regression metrics

---

## Future Improvements

Possible extensions include:

- Feature selection techniques
- Pipeline implementation using `Pipeline`
- Advanced feature engineering
- XGBoost
- LightGBM
- CatBoost
- SHAP-based model interpretability
- Model deployment with Flask or FastAPI
- Verification of Data leakage

---

## References

- Dean De Cock, *Ames Housing Dataset*
- Scikit-learn Documentation