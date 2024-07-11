
# CAR INSURANCE CLAIM PREDICTION

### Abstract
The project aims to create a predictive model that predicts a policyholder filing an insurance claim within six months. This model could revolutionize insurance companies' resource management, risk assessment, and claims processing workflows. The model uses a comprehensive dataset of policyholder attributes, allowing for more accurate premium rate adjustments, improved claims processing efficiency, and effective risk mitigation strategies. The model will use Logistic Regression, Linear Discriminant Analysis, and Random Forest Classification for modeling binary outcomes and handling complex interactions. The insights will provide data-driven strategies, increased operational efficiency, and customer satisfaction.

### Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Dataflow and Architecture](#dataflow-and-architecture)
- [Data Cleaning](#data-cleaning)
- [Data Exploration](#data-exploration)
- [Data Preprocessing](#data-preprocessing)
- [Predictive Modeling](#predictive-modeling)
- [Findings](#findings)
- [Conclusion](#conclusion)
- [Future Works](#future-works)
- [References](#references)
- [Requirements](#requirements)
- [Usage](#usage)

### Introduction
The goal of this project is to create a simple tool that can be used to determine a customer's likelihood of filing a claim on their auto insurance during the next six months. This covers fundamental information such as age, place of residence, length of time they've had insurance, and kind of vehicle they drive, with a particular emphasis on the safety features of these vehicles. Our primary objective is to give insurance companies a more comprehensive view of possible claims. This project has two advantages: better risk management for insurance companies and more individualized insurance policies for clients.

### Dataset
This dataset was sourced from Kaggle and contains information on 58,592 policyholders with 44 attributes, including policy, tenure, car and policyholder age, area cluster, car specifications, safety features, and more. The target variable is “is_claim” indicating whether a policyholder will file a claim in the next 6 months or not.

### Dataflow and Architecture
The data flow diagram below provides a visual representation of the data utilized in this project. Data loading involves importing data into an analysis environment, followed by data cleaning, data exploration, data preprocessing, predictive modeling, and findings.

### Data Cleaning
The data cleaning process involved meticulous checking for null values and simplifying the dataset by removing statistically insignificant variables, thereby enhancing the robustness and efficiency of subsequent analysis.

### Data Exploration
1. **What is the distribution of the target variable?**
2. **Does the preference for fuel type change with the age of the car and the age of the policyholder?**
3. **Is there a trend indicating that policyholders of certain ages prefer cars with a specific transmission type?**
4. **Which transmission type is most common among different age groups of policyholders?**
5. **What is the average age of policyholders within each area cluster?**
6. **How does the age of cars with different transmission types vary across different fuel types?**
7. **Are certain age groups of policyholders with specific transmission types more likely to file claims?**
8. **How does the NCAP rating of cars driven by different age groups of policyholders vary with transmission type?**
9. **Does car height correlate with transmission and fuel type preferences?**
10. **Is there a relationship between car width and the likelihood of a claim being filed, and does this differ by fuel type?**

### Data Preprocessing
Data preprocessing is a critical step in the analytical modeling process. It involves transforming raw data into an understandable format for further processing and analysis.

- **Handling Class Imbalance:** Synthetic Minority Over-sampling Technique (SMOTE) was applied to balance the dataset.
- **Separating Numerical and Categorical Variables:** True numerical columns are treated for statistical modeling, and categorical columns, even those encoded as numbers, are handled appropriately.
- **Feature Selection and Reduction of Multicollinearity:** Label encoding for some columns, conversion of specific categorical variables into dummy variables, and elimination of irrelevant features.
- **Data Splitting:** The processed dataset was split into a training set (75%) and a test set (25%).

### Predictive Modeling
Predictive modeling is integral to our Car Insurance Claim Prediction project.

- **Logistic Regression:** Utilized as the baseline model with L2 regularization and cross-validation.
- **Linear Discriminant Analysis:** Applied after verifying the assumption of normality and equal variance across classes.
- **Random Forest Regression:** An ensemble method aggregating decisions from multiple decision trees. Conducted a grid search to find the optimal combination of hyperparameters.

### Findings
The performance summary shows that the Random Forest Regression model outperforms with an accuracy of 69.14%, precision of 70.82%, recall of 65.11%, F1 score of 67.85%, and ROC AUC of 0.755. This suggests that the Random Forest model is more effective for the project's prediction task.

![image](https://github.com/Junaid-M0hammed/Analyzing-Loan-Default-Rates-Insights-and-Predictive-Modeling-in-R/assets/159192661/0384fa0d-ef70-408b-8ce6-0fc5989483fd)


### Conclusion
The project successfully developed a robust predictive model for forecasting insurance claims over a six-month period. Rigorous data preprocessing, including SMOTE for class balance and careful encoding of categorical variables, laid a solid foundation. The Random Forest model is recommended for deployment due to its adeptness in navigating claim prediction nuances.

### Future Works
Future work should focus on refining the Random Forest model through more nuanced hyperparameter tuning and exploring additional ensemble techniques. Efforts to interpret the model's decision-making process could provide actionable insights for business strategy.

### References
- Chugh, V. Logistic Regression in R Tutorial. Datacamp.
- Najnin, I. Car Insurance Claim Prediction. Kaggle.
- Random Forests. Datacamp.
- Zach. Linear Discriminant Analysis in R (Step-by-Step). Statology.

### Requirements
The project is implemented in R and requires the following packages:
- dplyr
- ggplot2
- caret
- randomForest
- smote
- MASS
