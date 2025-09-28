# ESG and Profitability Prediction

This project investigates whether **Environmental, Social, and Governance (ESG)** and sustainability factors can be used to predict company profitability without relying on direct financial indicators such as Profit Margin, Revenue, or Market Capitalization. The study was conducted as part of the course *Application of Data Science in Finance*.  

## Problem Statement
The central problem is to determine whether ESG and sustainability factors can predict profitability independently of financial variables that directly determine profit. Including such variables leads to **data leakage**, which produces artificially high accuracy and invalidates the results.  

## Objectives
- Evaluate whether ESG and sustainability features alone can predict profitability.  
- Compare the performance of **Decision Tree, Logistic Regression, and Random Forest** models.  
- Assess models using advanced evaluation metrics such as **Log Loss, McFadden’s R², Brier Score, and the KS statistic**.  
- Apply **probability calibration** to ensure that probability estimates are reliable for financial applications.  

## Dataset
The dataset includes:  
- **Financial metrics**: Profit Margin, Revenue, Market Capitalization, Growth Rate  
- **ESG scores**: Environmental, Social, Governance, Overall  
- **Categorical attributes**: Industry, Region, Year  

The target variable, **Profitability**, was defined by categorizing Profit Margin into three groups:  
- Low (< 5%)  
- Medium (5–10%)  
- High (≥ 10%)  

## Methodology
The analysis followed the **CRISP-DM framework**, progressing through:  
1. Business Understanding  
2. Data Understanding  
3. Data Preparation  
4. Modeling (Decision Tree, Logistic Regression, Random Forest)  
5. Evaluation (Accuracy, Log Loss, ROC AUC, KS Statistic, Calibration)  
6. Insights and Application  

## Key Steps
- Addressed missing values by imputing Growth Rate using industry-specific medians.  
- Prevented **data leakage** by excluding Profit Margin, Revenue, and Market Capitalization from predictors.  
- Balanced the profitability classes using **SMOTE** and class weighting.  
- Applied **Platt scaling** and **isotonic regression** for probability calibration.  

## Results
- **Decision Tree**: 57% accuracy, interpretable but prone to overfitting.  
- **Logistic Regression**: 55% accuracy, provided interpretability through coefficients.  
- **Random Forest (uncalibrated)**: 65% accuracy, strong classification but poorly calibrated probabilities.  
- **Random Forest (calibrated)**:  
  - 86% accuracy  
  - ROC AUC: 0.96  
  - KS Statistic: 0.80  
  - Log Loss: 0.39  

## Conclusion
The study confirms that ESG and sustainability factors, when modeled appropriately, can provide reliable insights into profitability. Although ESG is not the sole determinant, **Environmental and Governance scores consistently emerged as significant predictors**. The project also highlights the importance of preventing data leakage and applying probability calibration to produce models that are both accurate and reliable for financial decision-making.  

## Repository Structure
├── ESG - FD0003363.ipynb # Jupyter Notebook with full analysis
├── Report_FD0003363.pdf # Final project report
├── ESG Data Final Presentation.pptx # Project presentation slides
└── README.md # Project overview (this file)


## Author
Pavithra Lakshmi Venugopal  
Data Science Student, Hochschule Fulda
