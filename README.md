# Kaggle Playground S3E14
My solution to episode 14, series 3 of the kaggle playground series.

## Overview
This repository showcases my proposed solution to the blueberry yield prediction problem within the current Kaggle playground series (series 3, episode 14). During the exploratory data analysis phase, I observed that several 'numerical' columns exhibited a discrete range of values. To address this, I made the decision to discretize these values by grouping them into distinct bins, treating these columns as categorical variables. Additionally, I removed certain columns that displayed perfect correlation with each other, as such correlations can potentially diminish accuracy and increase variance in the model.

For the remaining columns, I applied one-hot encoding to the categorical variables and employed the StandardScaler class from the sklearn library to scale the numerical columns. Subsequently, I conducted a series of mlflow experiments to identify the most effective base model, which turned out to be the LightGBMRegressor. I further fine-tuned the model's hyperparameters using optuna.

However, when evaluating the final results on the test set, I discovered signs of overfitting in the initial model. Consequently, I decided to optimize a RandomForest model instead, which exhibited better performance on the test set. As a result, I chose this refined model for my final submission.
