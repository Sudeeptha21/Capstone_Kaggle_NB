## Business problem Overview
The notebook begins by exploring the application_train.csv file, which contains key demographic information about the applicants, such as age, income, along with their credit history and other significant documents. Throughout the notebook, extensive data cleaning is performed to ensure the dataset is in optimal shape for analysis. Furthermore, the notebook focuses on identifying the most important predictors that influence the likelihood of defaulting. By carefully removing unnecessary rows and columns, the analysis reduces noise and enhances the model's overall efficiency.

## Table of Contents:
1. Objectives
2. Data Description: Exploring Target Variable
4. Data Cleaning and Wrangling
5. Correlation Heatmap
6. Modelling
7. Summary and Overall Insights with Ethical Considerations

## Objectives
Understand the target variable (TARGET):
Identify important predictors using statistics and visualizations.
Create and train a Logistic Regression model
Check the score of the model by using: accuracy, confusion matrix, and a ROC/AUC score.

The Top 3 Negative predictors of Default are: 

EXT_SOURCE_2    -0.160295
EXT_SOURCE_3    -0.135996
CODE_GENDER_F   -0.054704

Positive Correlations with TARGET (Default):

Days_birth: Older individuals are more likely to default. 
Name_Income_Type_Working: Clients who are employees rather than business owners are more likely to default. 
DAYS_Last_Phone_Change: Clients that have recently changed their phone numbers are at a higher default risk. 

Negative Correlations with TARGET (Default):

EXT SOURCE 2 & EXT SOURCE 3: Having a decent credit score is likely to decrease the chance of default. This makes sense as its a solid predictor of credit worthiness. 
CODE GENDER F: It appears that females are less likely to default than males. 

Data Summary: The Null values were cleaned. Null values exceeding 60% had their columns removed whereas Null values that were < 60% of the entire dataset were imputed with the median for numerical columns and with mode for categorical columns. 

Best model : CATBOOST Model which gave a 70 percent accuracy compare to other models like logistic and random forest.
