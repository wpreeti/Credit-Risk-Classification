# Module 20 Challenge: Supervised Learning - Credit Risk Classification 

In this Challenge, we will use various techniques to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer lending services company build a model that can identify the creditworthiness of borrowers.

Leveraging a logistic regression model to compare two versions of the dataset, use the original dataset and then resample the data by using the RandomOverSampler module from the imbalanced-learn library.

For both cases, we’ll get the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.


## Instructions
This challenge consists of the following subsections:
- Split the Data into Training and Testing Sets

- Create a Logistic Regression Model with the Original Data

- Predict a Logistic Regression Model with Resampled Training Data


## Split the Data into Training and Testing Sets
Open the starter code notebook and then use it to complete the following steps:

1. Read the `lending_data.csv ` data from the `Resources` folder into a Pandas DataFrame.

2. Create the labels set `(y) `from the “loan_status” column, and then create the features `(X)` DataFrame from the remaining columns.

    > Note A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

3. Check the balance of the labels variable `(y)` by using the `value_counts` function.

4. Split the data into training and testing datasets by using `train_test_split`.
      
## Create a Logistic Regression Model with the Original Data
Employ your knowledge of logistic regression to complete the following steps:

1. Fit a logistic regression model by using the training data `(X_train and y_train)`.

2. Save the predictions on the testing data labels by using the testing feature data `(X_test)` and the fitted model.

3. Evaluate the model’s performance by doing the following:

    - Calculate the accuracy score of the model.

    - Generate a confusion matrix.

    - Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the `0 (healthy loan)` and `1 (high-risk loan)` labels?

## Predict a Logistic Regression Model with Resampled Training Data
Did you notice the small number of high-risk loan labels? Perhaps, a model that uses resampled data will perform better. You’ll thus resample the training data and then reevaluate the model. Specifically, you’ll use `RandomOverSampler`.

To do so, complete the following steps:

1. Use the `RandomOverSampler` module from the imbalanced-learn library to resample the data. Be sure to confirm that the labels have an equal number of data points.

2. Use the `LogisticRegression` classifier and the resampled data to fit the model and make predictions.

3. Evaluate the model’s performance by doing the following:

    - Calculate the accuracy score of the model.

    - Generate a confusion matrix.

    - Print the classification report.

4. Answer the following question: How well does the logistic regression model, fit with oversampled data, predict both the `0 (healthy loan)` and `1 (high-risk loan)` labels?
