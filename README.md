## Business problem Overview
The notebook begins by exploring the application_train.csv file, which contains key demographic information about the applicants, such as age, income, along with their credit history and other significant documents. Throughout the notebook, extensive data cleaning is performed to ensure the dataset is in optimal shape for analysis. Furthermore, the notebook focuses on identifying the most important predictors that influence the likelihood of defaulting. By carefully removing unnecessary rows and columns, the analysis reduces noise and enhances the model's overall efficiency.

## Table of Contents:
1. Objectives
2. Data Description: Exploring Target Variable
4. Data Cleaning and Wrangling
5. Correlation Heatmap
6. Modelling
7. Challend=ges
8. Conclusion

## Objectives
Understand the target variable (TARGET):
Identify important predictors using statistics and visualizations.
Create and train a Logistic Regression model
Check the score of the model by using: accuracy, confusion matrix, and a ROC/AUC score.

## Data Cleaning and Wrangling
- Null values exceeding 60% had their columns dropped.
- Null values that were < 60% of the entire dataset were imputed with the median for numerical columns and with mode for categorical columns
- Some columns like the EXT SOURCE, CAR AGE were binned to make the machine learn faster and better
- Outliers were removed in certain columns like Children
- Downsampled the data in order to achieve better accuracy since the dataset was heavily imbalanced 

### The Top 3 Negative predictors of Default are: 
- EXT_SOURCE_2 & EXT_SOURCE_3: having a decent credit score is likely to decrease the chance of default. This makes sense as its a solid predictor of credit worthiness
- CODE_GENDER_F: It appears that females are less likely to default than males.

### The Top 3 Positive predictors of Default are:
- Days_birth: Older individuals are more likely to default. 
- Name_Income_Type_Working: Clients who are employees rather than business owners are more likely to default. 
- DAYS_Last_Phone_Change: Clients that have recently changed their phone numbers are at a higher default risk. 

## Modelling
- CATBOOST Model which gave a 70 percent accuracy compared to other models like logistic regression model and random forest model.
- Fast and reliable with high accuracy.
- Best for evaluating non linear parameters and giving the best decisison in case of classification problems.

### Evaluation Metric:
- Used confusion matrix, which is ideal for evaluating imbalanced classification problems.

## Challenges 
- Severe Class Imbalance: Only about 8% of applicants defaulted so downsampling was necessary.
-Missing Data: Many columns had >60% missing values, requiring careful dropping or imputation.

## Key Learnings and Conclusion
- Importance of designing transparent models with financial inclusion is the goal.
- Integrating with Ai would automate the model and increase efficiency.
- Personlized loan offers and transparent communication would reduce financial losses.


