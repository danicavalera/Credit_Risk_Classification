# Credit Risk Classification

For this analysis, I used various techniques to train and evaluate models with imbalanced classes. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Instructions:

This challenge consists of the following subsections:

### Split the Data into Training and Testing Sets

1. Read the `lending_data.csv` data from the `Resources` folder into a Pandas DataFrame.

2. Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

3. Check the balance of the labels variable (`y`) by using the `value_counts` function.

4. Split the data into training and testing datasets by using `train_test_split`.


### Create a Logistic Regression Model with the Original Data

Employ your knowledge of logistic regression to complete the following steps:

1. Fit a logistic regression model by using the training data (`X_train` and `y_train`).

2. Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.

3. Evaluate the model’s performance by doing the following:

    * Calculate the accuracy score of the model.

    * Generate a confusion matrix.

    * Print the classification report.

### Predict a Logistic Regression Model with Resampled Training Data


1. Use the `RandomOverSampler` module from the imbalanced-learn library to resample the data. Be sure to confirm that the labels have an equal number of data points. 

2. Use the `LogisticRegression` classifier and the resampled data to fit the model and make predictions.

3. Evaluate the model’s performance by doing the following:

    * Calculate the accuracy score of the model.

    * Generate a confusion matrix.

    * Print the classification report.
    

### Write a Credit Risk Analysis Report

## The results
### Machine Learning Model 1:
Accuracy: 95%
The precision and recall for the 0 class (healthy loan) is much better than that for the 1 class (high risk). For example, the precision for the 0 values is 1, meaning that out of all the times that the model predicted a testing data observation to be the value 0, 100% of those predictions were correct. In contrast, out of all the times that the model predicted a value of 1, only 85% of those predictions were correct.

### Machine Learning Model 2:
Accuracy: 99.36%
The precision for 0 class is much better than that for the 1 class, however, the recall for both classes are equivalent. 100% of class 0's predictions were correct, yet only 84% of class 1's predictions were correct. However, with recall, both classes reported 99%.

## Summary

Overall, the resampled model performed the best. Although both models gave a good accuracy score, Model 2 (resampled), resulted in a 99% accuracy score, making it higher than Model 1 (original), at 95% accuracy. It is also equally important to predict the 0's and 1's, and model 2 had a much more balanced recall with class 0 and 1 being at 99%. With this in mind, I would recommend using the resampled model.