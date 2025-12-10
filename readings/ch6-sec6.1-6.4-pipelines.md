From Introduction to machine learning in python

# Pipelines

You can use it to chain preprocessing + modeling

For many machine learning algorithms, the
representation of the data you provide is very important

Consequently, most machine learning applications
require not only the application of a single algorithm, but
the chaining together of many different processing steps
and machine learning models
4


## Main Benefit ** 

Scaling outside cross validation causes information leakage since scaling affects the whole training data, including the one that is used to test a fold in cross validation.

Any data dependent transformation (scaling, feature selection, PCA) should be placed inside a pipeline before using cross validation or gridsearchCV


Using a Pipeline ensures:

For each CV split, preprocessing (like MinMaxScaler) is refit only on the training fold.

No info from the CV test fold influences preprocessing.

Proper pipeline usage improves validity of model eval

Each pipeline step is a tuple, and all steps need to have a transform function EXCEPT the last step, which ONLY needs a FIT function


Pipeline steps

1. Load & split data

1. Create the pipeline

1. Do NOT fit the pipeline here

1. Define param grid

1. Construct GridSearchCV with the pipeline

1. grid.fit(X_train, y_train)

1. Inside this step:

- For each CV fold:

- - Pipeline is fit from scratch

- - Scaler is fit only on that fold’s training split

- - SVM is fit on the transformed training split

- - Validation happens on the fold’s test split

8. After the best params are found:

- Pipeline is refit on the full training set just once