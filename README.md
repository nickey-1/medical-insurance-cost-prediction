# medical-insurance-cost-prediction
The project is framed around UrbanNest Health Analytics, where insurance providers are described as relying on rough assumptions when setting prices. The aim is to predict charges based on available characteristics.
The goal is to use available patient characteristics — age, sex, BMI, number of children, smoking status, and region — to develop a more data-driven and consistent approach to estimating insurance charges.

Business Problem

Insurance charges can vary substantially between patients. A pricing approach based mainly on broad assumptions may fail to reflect important differences in patient characteristics.

This project therefore investigates:

Which patient characteristics are most strongly associated with insurance charges?
How do smoking status, age, BMI, sex, number of children, and region relate to cost?
Can these characteristics be used to predict insurance charges?
How well does a Linear Regression model perform on previously unseen patients?
Project Objectives
Inspect and clean the insurance dataset.
Explore relationships between patient characteristics and insurance charges.
Identify important patterns through exploratory data analysis.
Prepare categorical variables for machine learning.
Train a Linear Regression model.
Evaluate the model using MAE, RMSE, and R².
Interpret the model coefficients.
Generate predictions for hypothetical patients.
Dataset

The dataset contains 1,337 patient records and seven variables:

Variable	Description
age	Patient age
sex	Patient sex
bmi	Body Mass Index
children	Number of children
smoker	Smoking status
region	Patient region
charges	Medical insurance charge
Data Quality Checks

The dataset was inspected for missing values, duplicate records, data types, descriptive statistics, and categorical values.

Records: 1,337
Variables: 7
Missing values: 0
Duplicate rows: 0
Technologies Used
Python
Pandas — data manipulation and analysis
NumPy — numerical operations
Matplotlib — data visualization
Scikit-learn — machine learning and model evaluation
Google Colab — development environment
Project Workflow
Load Data
    ↓
Inspect Dataset
    ↓
Clean Data
    ↓
Exploratory Data Analysis
    ↓
Prepare Features
    ↓
One-Hot Encode Categorical Variables
    ↓
Train/Test Split
    ↓
Train Linear Regression Model
    ↓
Evaluate Model
    ↓
Interpret Coefficients
    ↓
Generate Predictions
Exploratory Data Analysis

The analysis examined the distribution of insurance charges and how charges varied according to different patient characteristics.

Smoking Status

Smoking status showed the largest difference in average insurance charges.

Smoking status	Average charge
Non-smoker	$8,440.66
Smoker	$32,050.23

Smokers in this dataset had average charges approximately 3.8 times those of non-smokers.

Age

Average insurance charges increased across the age groups examined.

Age group	Average charge
18–25	$9,111.43
26–35	$10,495.16
36–45	$13,493.49
46–55	$15,986.90
56–64	$18,795.99

The correlation between age and charges was approximately 0.30, indicating a positive relationship.

BMI

Average charges also varied according to BMI category.

BMI category	Average charge
Underweight	$8,852.20
Normal	$10,409.34
Overweight	$10,987.51
Obese	$15,572.04

The correlation between BMI and charges was approximately 0.20.

BMI and Smoking Status

The combined analysis of BMI category and smoking status revealed a substantial difference in average charges.

BMI category	Non-smoker	Smoker
Underweight	$5,532.99	$18,809.82
Normal	$7,685.66	$19,942.22
Overweight	$8,257.96	$22,495.87
Obese	$8,855.53	$41,557.99

The highest average charge occurred among obese smokers, at approximately $41,557.99.

Sex

Average charges were:

Female: $12,569.58
Male: $13,975.00

The difference was considerably smaller than the difference observed between smokers and non-smokers.

Region

Average charges by region were:

Region	Average charge
Southeast	$14,735.41
Northeast	$13,406.38
Northwest	$12,450.84
Southwest	$12,346.94

Regional differences were relatively small compared with the difference associated with smoking status.

Machine Learning
Model

A Linear Regression model was used to predict charges.

The model used:

Age
Sex
BMI
Number of children
Smoking status
Region

Categorical variables were converted into numerical features using one-hot encoding.

The dataset was divided into:

80% training data: 1,069 records
20% test data: 268 records

A random_state of 42 was used for reproducibility.

Model Performance

The model was evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R².
