# Regression Metrics


R2 = coefficient of determination
- measures how well regression model explains the variation in the target Y by X

R2 = 1 - (RSS / TSS)

Variance = How much Y changes from its mean, spread of actual Y values. Mathematically that is TSS

RSS = Residual Sum of Squares -> unexplained variance after fitting model (model error). Difference between actual Y to the predicted Y

TSS = Total Sum of Squares -> Total variance in Y before considering model. Difference between actual Y and mean of Y

So RSS / TSS → the fraction of total variability that’s unexplained by the model.

1 − (RSS / TSS) → the fraction that is explained by the model.

R² tells you what percentage of Y’s variation is explained by X




R2 is the more intuitive metric used for regression

Altough you could use mean squared error or mean absolute error