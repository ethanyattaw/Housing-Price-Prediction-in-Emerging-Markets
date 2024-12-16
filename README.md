# Housing-Price-Prediction-in-Emerging-Markets
Comparison of ML Methods for Predicting Housing Prices in India

## Introduction

Housing price prediction is a well-researched problem in developed markets, but it remains underexplored in emerging markets like India, despite rapid urbanization and growing housing sectors. This project aims to fill this research gap by assessing the applicability of machine learning (ML) methods for housing price prediction in Delhi, India. The dual objectives are:
1. To evaluate whether ML models can achieve accurate predictions in an emerging market context.
2. To compare the performance of five ML methods: Linear Regression (LR), Random Forest (RF), XGBoost, LightGBM, and Stacked Generalization.

## Description of the Code

The code implements a comprehensive machine learning pipeline for housing price prediction:
- **Data Preprocessing**:
  - Handles missing values, drops irrelevant features, and creates a duplicate dataset which normalizes the `price` column using logarithmic transformation.
- **Model Training**:
  - Trains five models: LR, RF, XGBoost, LightGBM, and Stacked Generalization.
  - Hyperparameter tuning is applied where necessary.
- **Evaluation**:
  - Evaluates models using metrics such as RMSE, RMSLE, and R².
  - Compares model performance on the original dataset and a transformed dataset with logarithmic price normalization.
- **Feature Importance**:
  - Provides insights into the most influential features for each model.
- **Visualization**:
  - Includes residual plots, actual vs. predicted price comparisons, and feature importance graphs.

## Results Summary

The performance of the five models is summarized below:

| **Method**       | **RMSLE** | **R²**   | **Log Price RMSE** | **Log Price R²** |
|-------------------|-----------|----------|---------------------|------------------|
| **Linear Regression** | 0.6587   | 0.749    | 0.3215              | 0.724            |
| **Random Forest**     | 0.2127   | 0.892    | 0.2014              | 0.892            |
| **XGBoost**           | 0.1595   | 0.930    | 0.1549              | 0.936            |
| **LightGBM**          | 0.1704   | 0.916    | 0.1541              | 0.937            |
| **Stacked Gen.**      | 0.1566   | 0.927    | 0.1485              | 0.941            |

These results are consistent with findings in the literature:
- **Comparison to Prior Studies**:
  - Spain Study: Best R² of 0.9192 and best RMSE (log price) of 0.1818 using Gradient Boosting.
  - Beijing Study: Best RMSLE of 0.1635 using Stacked Generalization.
  - This study’s best results (R² = 0.941, RMSE (log price) = 0.1485, RMSLE = 0.1566) align closely, demonstrating the feasibility of housing price prediction in an emerging market.

- **Model Comparisons**:
  - **Stacked Generalization** achieved the best overall performance but required the longest computational time.
  - **XGBoost** and **LightGBM** offered similar accuracy with faster runtimes, making them more computationally efficient.
  - **Random Forest** performed moderately well, outperforming Linear Regression but falling behind gradient boosting methods.
  - **Linear Regression** had the lowest accuracy but was the most computationally efficient.

These findings confirm that ML models can accurately predict housing prices in an emerging market when applied to well-structured data.

## Implications

- **Utility of Housing Price Prediction**:
  - Enables real estate investors to identify high-value opportunities and trends.
  - Helps homebuyers make informed decisions and helps developers price projects competitively.
  - Assists policymakers and urban planners in addressing housing affordability and infrastructure needs.

- **Value of Data Collection**:
  - Demonstrates that robust data collection in emerging markets is critical for ML applicability and accuracy.
  - Highlights the potential for improved predictions in underrepresented regions with better datasets.

- **Expanding ML Use Cases**:
  - Validates the adaptability of ML methods across diverse markets and datasets.
  - Encourages further exploration of ML applications in other underrepresented domains and regions.
 
## Acknowledgements

1. **Dataset**:  
   Goel, Y. (2021, November 23). Housing price dataset of Delhi(India). *Kaggle*.  
   [https://www.kaggle.com/datasets/goelyash/housing-price-dataset-of-delhiindia/data](https://www.kaggle.com/datasets/goelyash/housing-price-dataset-of-delhiindia/data)  

2. **Spain Study**:  
   Mora-Garcia, R. -T., Cespedes-Lopez, M. -F., & Perez-Sanchez, V. R. (2022). Housing Price Prediction Using Machine Learning Algorithms in COVID-19 Times. *Land, 11*(11), 2100.  
   [https://doi.org/10.3390/land11112100](https://doi.org/10.3390/land11112100)  

3. **Beijing Study**:  
   Truong, Q., Nguyen, M., Dang, H., & Mei, B. (2020). Housing price prediction via improved machine learning techniques. *Procedia Computer Science, 174*, 433-442.  
   [https://doi.org/10.1016/j.procs.2020.06.111](https://doi.org/10.1016/j.procs.2020.06.111)  
