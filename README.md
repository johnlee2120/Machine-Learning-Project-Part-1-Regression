
## Machine Learning Project: Regression

## Executive Summary 

- Built and evaluated multiple regression models to predict car prices (~200 observations, 25 features)
- Best overall model: **Linear Regression (with Lasso Regularization) (R² = 0.80, RMSE = 3711.17)** with strong generalization
- Regularization significantly improved performance compared to polynomial models, reducing overfitting
- Key drivers of price: **engine size, curb weight, and brand category**
- Business impact: Enables more accurate vehicle pricing, improved margin optimization, and better identification of mispriced vehicles

<br><br><br>

## Techniques Used

- **Models:** Linear Regression, Polynomial Regression, Ridge, Lasso, Elastic Net, SGD Regression
- **Feature Engineering & Processing:** One-Hot Encoding, Log Transformation, Custom Feature Creation (brand_category)
- **Evaluation:** RMSE, R² Score, Residual Analysis, Predicted vs Actual Comparison
- **Validation & Tuning:** Train/Test Split, Cross Validation, Polynomial Degree Tuning
- **Regularization:** L1 (Lasso), L2 (Ridge), Elastic Net

<br><br><br>

## Detailed Sections

**Objective:** 

Predict car prices using structured automotive data and evaluate multiple regression approaches

**Dataset:** 

- ~200+ observations, 25 features
- Mix of categorical and numerical features
- Target: Price

**Data Processing:**

- Handled categorical variables via one-hot encoding
- Feature engineering (i.e. creating brand_category based on average prices)
- Log transformation applied to reduce skew 
- Train test split (70/30)

**Modeling:**

- Linear regression
- Polynomial regression (degree tuning)
- Regularization:
  - Ridge
  - Lasso
  - Elastic Net
- SGD-based regression

**Model evaluation:**

- Metrics
  - RMSE
  - R² Score
- Cross validation (3-fold, 5-fold)
- Residual analysis + diagnostic plots

**Results:**

- Best Model - Linear Regression with Lasso Regularization
- R²: 0.80 (highest)
- RMSE: 3711.17 (lowest)
- Regularization improved generalization vs polynomial overfitting

**Key Insights:**

- Engine size and curb weight are strong predictors
- Polynomial features caused severe overfitting without regularization
- Scaling is critical for SGD performance

<br><br><br>


## Business Impact & Recommendations

- Price vehicles more accurately using key features such as engine size and curb weight, improving pricing consistency and competitiveness
- Use the model to identify underpriced or overpriced vehicles, enabling better margin optimization
- Apply log-transformed models (with Lasso regularization) in production to ensure stable predictions and avoid overfitting seen in polynomial models
- Prioritize simpler, regularized models over complex polynomial models to maintain generalization on new data
- Ensure proper feature scaling for gradient based models (SGD) to maintain reliable performance in real world deployment


<br><br><br>

## Images:

<p align="center">
  <img src="Images/predicted%20vs%20actual.png" width="450"/>
</p>

<p align="center">
  <em><strong>Predicted vs Actual prices using Lasso Regression (strong linear fit)</strong></em>
</p>

<br><br><br>

<p align="center">
  <img src="Images/before%20and%20after%20log.png" width="600"/>
</p>

<p align="center">
  <em><strong>Before and after log transforming the "engine size" feature</strong></em>
</p>

<br><br><br>

<p align="center">
  <img src="Images/model%20comparisons.png" width="300"/>
</p>

<p align="center">
  <em><strong>Model comparisons (Lasso is strongest)</strong></em>
</p>

