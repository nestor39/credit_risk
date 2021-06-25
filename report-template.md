# Module 12 Report Template

## Overview of the Analysis


The purpose of this analysis is to evaluate models with imbalanced classes. I used a CSV dataset of historical lending activity from a peerto peer lending services company to build a model that can identify the creditworthiness of borrowers.

The CSV file mentioned above contains: loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt. Thanks to this information we can predict what customer will pay off.

I created some variables for this analysis, for example:


I used some function from python to help me out with the variables i was trying to predict:
```value_counts``` : function to count the number of firms in each category.

```fit function``` : funtion that scikit-learn makes available to the logistic regression classifier

```predict``` function to classify our features and discover if the model can assign them to the correct targets.

```Logistic Regression```: is designed to predict discrete outcomes.

The analysis consists of the following steps:
* Split the Data into Training and Testing Sets

* Create a Logistic Regression Model with the Original Data

* Predict a Logistic Regression Model with Resampled Training Data

One of the methods that I used was the Resampling Method: it is a way to artificially balance the classes that the model gets during training. This helps the model avoid hyperfocusing on the larger class and can improve the predictions for the smaller class.

Three types of resampling techniques exist: oversampling, undersampling, and combination sampling.

## Results



* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    * Balanced accuracy score (95.2%)
    * Precision score 0 : (100%)
    * Precision score 1 : (85%)
    * Recall score 0 : (99%)
    * Recall score 1 : (91%)



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    * Balanced accuracy score (99.4%)
    * Precision score 0 : (100%)
    * Precision score 1 : (84%)
    * Recall score 0 : (99%)
    * Recall score 1 : (99%)

Note:
The balanced accuracy in binary and multiclass classification problems to deal with imbalanced datasets. It is defined as the average of recall obtained on each class.
The best value is 1 and the worst value is 0 when ```adjusted=False.```

The precision is the ratio ```tp / (tp + fp)``` where ```tp``` is the number of true positives and fp the number of false positives. The precision is intuitively the ability of the classifier not to label as positive a sample that is negative.
The best value is 1 and the worst value is 0.


The recall is the ratio ```tp / (tp + fn)``` where tp is the number of true positives and ```fn``` the number of false negatives. The recall is intuitively the ability of the classifier to find all the positive samples.
The best value is 1 and the worst value is 0.

## Summary


* Which one seems to perform best? Model #2
* How do you know it performs best? Higher values
* Does performance depend on the problem we are trying to solve? In this case class 1 helped us   solve the problem. It was the one that gives us the answer 

I would recommend the second model, the we can see that the results for this model with oversampled data, fits much better and gives us a better result (Balanced accuracy score (99.4%),* Recall score 1 : (99%), etc.)
