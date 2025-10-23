# Chapter 2 Supervised Learning


## Section 2.3.3 Linear Models

Linear models make prediction using a linear function


### Linear models for regression

Prediction formula

ŷ = w[0] * x[0] + w[1] * x[1] + ... + w[p] * x[p] + b

w = coefficient / slope
b = y intercept
### Linear Regression (ordinary least squares)

Simplest linear method for regression

Find the w and b that minimize the Mean Squared Error MSE between predictions and true regression analysis


MSE = sum of squared difference between prediction and true values / number of samples


Linear regressions uses R^2 as the scoring method

R^2 = How much of the variance in Y is explained by X?
Between 0 - 1

.score() in python


If the training and test score are low and around the same then model is UNDERFITTING

If the training score is HIGH and training score is LOW then the model is OVERFITTING


### RIDGE REGRESSION


Want the magnitude of coefficient to be as low as possible so w is as close to 0

This means each feature has little effect on the outcome, which translates to having a small slope

This constraints is called REGULARIZATION
- restricing a model to avoid overfitting

Ridge regression uses L2 regularization



### Linear Classification

ŷ = w[0] * x[0] + w[1] * x[1] + ... + w[p] * x[p] + b > 0

Threshold for a predicted value at 0

If function is smaller than 0 = class -1
If function is greater than 0 = class +1

2 common linear classification algorithms are:
- Logistic Regression
- Linear Support Vector Machines (Linear SVMs)


Both use L2 regularization 


IF test score and training score are high and close, it could be that the model is underfitting. Decreasing regularization and making the model more complex might help with that