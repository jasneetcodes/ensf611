From: Introduction to machine learning in python


# 5.1 Cross Validation

Method used to evaluate how a model generalizes 

Most common form is the k-fold cross validation
- Dataset is split k times, and trained and tested.
- Returns k times accuracy results

Benefits
- Use data more effectively
- Allows the model to generalize to all samples in the dataset
- Shows how sensitive our model is
- Gives us a view on how the model performs in the worst and best case scenerios

- Only downside is the computational cost


- Use stratified k-fold cross-validation for classifications
- Allows you to keep the same proporations between the classes in each fold as they are in the whole dataset



# 5.2 Grid Search

Grid search is used to find the best possible parameters for the model

In it's most basic form, its a for loop with different ranges of parameters, validated, and tested for the highest score, returning the best score and best parameters


Best to split the data into 3 parts, one for training, one for validating, and then another for testing the model using the best parameters
- This is extremely time consuming btw


We can use GridSearchCV in scikit-learn to both grid search and cross validate

Example.
X_train, X_test, y_train, y_test = train_test_split(
iris.data, iris.target, random_state=0)

grid_search.fit(X_train, y_train)

print('Test set score: {grid_search.score(X_test,
y_test):.2f}')

print(f'Best parameters: {grid_search.best_params_}')

print(f'Best cross-validation score:
{grid_search.best_score_:.2f}')

print('Best estimator: {grid_search.best_estimator_}')