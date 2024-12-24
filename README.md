# Suicide-Rate-Factors-Analysis
This project delves into the intricate relationship between various factors and suicide mortality rates, aiming to uncover meaningful insights through a comprehensive data-driven approach. By utilizing advanced data preprocessing techniques, exploratory visualizations, and machine learning models, this analysis seeks to identify significant predictors of suicide rates. The project not only showcases technical proficiency but also emphasizes the critical thinking required to interpret and act upon complex datasets.
#Project Overview

This project aims to identify the significant factors affecting suicide mortality rates through data analysis and modeling. By leveraging visualizations and machine learning models, we extract actionable insights and develop a comprehensive understanding of the data.

#Dataset

The dataset for this project was curated by combining multiple datasets from World Bank Data repositories. These datasets include various socioeconomic and demographic features, such as age, gender, GDP, and population statistics, alongside corresponding suicide rates. This integration of diverse data sources ensures a comprehensive analysis of the factors influencing suicide mortality rates.
WORLD BANK-> https://data.worldbank.org/

#Steps Performed

#Data Preprocessing

Backward Elimination:

Performed to systematically remove less significant variables from the model, starting with the least significant based on p-values.

Benefit: Ensures a more parsimonious model by retaining only the most impactful predictors, thereby reducing complexity and potential overfitting.

Removing High VIF Values:

Checked for multicollinearity by calculating Variance Inflation Factors (VIF) for each variable and eliminated variables with high VIF values.

Benefit: Helps prevent redundancy among predictors and ensures the stability and reliability of the regression coefficients.

Checking for Non-Normality:

Used visual methods such as histograms, Q-Q plots, and Shapiro-Wilk tests to assess the distribution of variables.

Benefit: Identifies deviations from normality, which is crucial for certain statistical models and tests that assume normality.

Removing Variables with High P-Values:

Iteratively excluded variables with high p-values (>0.05), indicating a lack of statistical significance.

Benefit: Improves model precision by focusing on predictors that significantly contribute to explaining the target variable.





#Decision Tree Analysis
A decision tree model was implemented to understand the hierarchical relationships between various factors and suicide mortality rates. The model uses a tree-like structure where each internal node represents a decision rule, each branch represents an outcome of that rule, and each leaf node represents a prediction.
Optimal Decision Tree Implementation
The model was optimized by:
Finding the ideal tree depth to prevent overfitting
Using pruning techniques to improve generalization
Minimizing the Gini impurity to ensure pure leaf nodes
Implementing cross-validation to validate model performance
Key Findings
The optimized decision tree revealed three critical decision paths:
Primary Split: Immunization rates (HepB3) emerged as the root node with a threshold of 91.5%, indicating its fundamental importance in classifying suicide mortality rates.
Secondary Factors: For countries with higher immunization rates, tariff rates became the next most important factor, with critical thresholds at 1.715% and 4.91%.
Economic Indicators: The final branches consider gross capital formation and government consumption expenditure, suggesting their moderating role in suicide mortality rates.


#Advanced Model Analysis: Bagging, Random Forest, Gradient Boosting
After implementing multiple ensemble methods (bagging, random forest, and gradient boosting), the gradient boosting model emerged as the most effective approach, demonstrating superior predictive performance. Here's a detailed analysis of the model insights:
Variable Importance Analysis
The variable importance plot revealed the following key predictors:
Immunization (HepB3): Most influential factor, indicating the strong relationship between public health infrastructure and suicide rates
Tariff Rates: Second most important predictor, suggesting economic policy impacts
Economic Indicators: Including gross capital formation and government expenditure
SHAP (SHapley Additive exPlanations) Analysis
The SHAP analysis provided deeper insights into feature contributions:
Revealed complex interactions between health indicators and economic factors
Showed how immunization rates have both direct and indirect effects on suicide rates
Demonstrated non-linear relationships between economic indicators and the target variable
Partial Dependency Plots
These plots revealed important non-linear relationships:
Immunization Rate:
Shows a negative correlation with suicide rates
Critical threshold at 91.5% immunization coverage
Economic Indicators:
Non-linear relationship with tariff rates
Complex interactions with government expenditure
Health Metrics:
Clear relationship between health infrastructure and suicide rates
Important thresholds for public health interventions
