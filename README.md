# Predicting Result of Shots in La Liga

## Introduction
This project is focused on predicting the outcome of shots in La Liga using machine learning techniques. Our primary goal is to determine whether a shot results in a goal or not.

## Problem Statement
The problem at hand is a classification problem where the target is to classify whether a shot is a goal or not. This model can be used in real-world applications such as analyzing player performance, understanding player habits on the field, deciding which players to substitute during a game, or determining if a new player will be compatible with the team during transfer seasons.

## Data Exploration
We used data from Understat for La Liga. The target variable in our dataset is "result," which indicates whether a shot is a goal or not. Several features were utilized to help our model learn and predict the target variable.

## Imbalancedness
Our dataset has an imbalance problem, where the majority of target variables significantly outnumber the minority. This imbalance can lead to the model learning the features of the majority class better than the minority class, causing inaccurate predictions.

#### SMOTE (Synthetic Minority Over-Sampling Technique)
We initially tried to use SMOTE for oversampling to bridge the gap between minority and majority target variables. SMOTE generates synthetic observations based on original ones using clustering methods. However, it resulted in overfitting as the synthetic observations did not represent the minority class well.

#### Undersampling
We resolved the imbalance issue by decreasing the count of the majority class using undersampling techniques.

## Model Selection and Hyperparameter Tuning
We employed Gradient Boosting Machines (GBM) for modeling. To find the best model and hyperparameters, we used H2O AutoML, which automated the process of finding the ideal model and hyperparameter combinations for our data.

## Final Model Selection
The final model was selected based on balanced accuracy scores and confusion matrices obtained from testing the models on unseen data. Both the Stacked Ensemble and vanilla Gradient Boosting Machines showed similar performance metrics. However, considering domain knowledge and processing time, we chose the vanilla Gradient Boosting Machines as our final model.

## Conclusion
Our final model provides a robust method for predicting whether a shot results in a goal, offering valuable insights for player performance analysis and strategic planning in football.

## Authors
- Sezai Ufuk Oral
- Emre Çorbacı

## Supervisor
- Dr. Mustafa Çavuş
