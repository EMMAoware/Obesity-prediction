# Estimation of Obesity Levels Based on Eating Habits and Physical Condition

## Introduction
The analysis of the given dataset of nutritional and health data from people in Mexico, Peru, and Colombia is the main goal of this study. Using Python, 
the objective of this project is to estimate obesity levels based on eating patterns and physical condition. The research aims to find out how lifestyle factors affect 
obesity through the use of advanced visualizations, exploratory data analysis (EDA), and data cleansing. 
Further, predictive models that estimate obesity levels will be constructed using machine learning approaches, offering a data-driven method of comprehending health 
patterns in the aforementioned countries.

## Objective
The purpose of this project is to explore some given risk factors and identify the leading risk factors of obesity using machine learning. This would help bring awareness to 
individuals, health practitioners and insurance companies in making critical decisions.

## Dataset
The dataset was comprised of 2,111 records with 17 features. Eight of the features were continuous variables, while the remaining nine were categorical variables. In this dataset, 
the target variable ‘NObeyesdad’ (Obesity Level) categorizes the various individuals into the following:
-Normal_Weight 
-Overweight_Level_I 
-Overweight_Level_II
-Obesity_Type_I
-Insufficient_Weight
-Obesity_Type_II
-Obesity_Type_III

## Data pre-processing
### Missing values
As part of the data pre-processing stage, a look at the data collected did not reveal any missing values

### Duplicate Values
A total of twenty-four (24) duplicate values were detected out of the 2,111 records and removed. They were removed because relative to the total 
dataset, the number of duplicates is quite small.

### Outliers
Outliers were detected for two variables, Age and Weight. From observation, the outliers are true outliers that represent natural variations in 
the dataset, as such, they were maintained.

### Feature Scaling
Because Age and Weight had outliers, I used a Robust Scaler on them in this study. Because it is less susceptible to 
outliers than other scaling techniques, the Robust Scaler was selected to better handle the skewed distribution of these variables. 
This guarantees that the performance of the model is not unduly impacted by the extreme values.

### Encoding
The mode of transportation feature, 'MTRANS', was transformed using the one-hot encoding technique because it is not binary and lacks any i
nherent order. For other features with more than two categories and an intrinsic order, ordinal encoding was applied.

### Feature Selection
5.6	Feature Selection
In deciding the number of features to be trained for the model, there was the need for some form of dimensionality reduction. 
The first step was to check for features that are statistically significant. Features that have a statistically significant 
relationship with the target variable (p-value less than 0.05) were used, which turned out to be all the features.

## Model Selection
- Random Forest
- K Nearest Neighbour( KNN)
- XGBoost
- Gradient Boosting

## Results and Discusion
•	XGBoost achieved the highest metrics across the board, with an accuracy of 0.97 and matching weighted precision, recall, and f1-score values. 
This consistency across metrics suggests that XGBoost handles the dataset's complexities well, capturing both majority and minority class 
characteristics effectively

•	Gradient Boosting follows closely, with each metric at 0.96. This is aligned with Gradient Boosting's iterative learning approach, 
though XGBoost may hold a slight advantage due to its more optimized handling of regularization and computational efficiency.

•	Random Forest also performed well with a 0.95 accuracy and similarly high precision, recall, and f1-scores. As a bagging-based ensemble, 
Random Forest is robust to variance, which is beneficial for achieving stable performance, though it may lack the refinement that boosting-based 
methods provide

•	K-Nearest Neighbors (KNN), however, showed a lower performance with an accuracy of 0.85 and slightly lower weighted metrics. KNN’s sensitivity 
to high dimensionality may account for this, indicating that it is less suited for this dataset compared to ensemble methods.

## Conclusion
Important insights into the risk factors promoting obesity were gained from the examination of food and physical health data collected 
from people in Mexico, Peru, and Colombia. Using their powerful feature optimization skills and iterative learning, XGBoost and Gradient Boosting 
produced the greatest accuracy of all the algorithms, at 97% and 96%, respectively. 

