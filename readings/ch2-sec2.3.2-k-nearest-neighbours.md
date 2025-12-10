From Introduction to Machine Learning Section 2.3.2


# K-nearest neighbours

Predicts new data sample depending on how close it is to a sample of existing data

K is the number of neighbours considered, and uses a majority rule to determine what class the sample is


For regression, multi neighbors, it evaluates the average of its neighbours


Got to find a good balance between how many neighbours to consider.
Too few neighbours makes the decision boundary complex, and can lead to a complex model (overfitting)
Like wise too many neighbours can lead to a flatter decision boundary, which leads to a simpler model (underfitting)


Not really used as much because it's not good with large datasets whether in features or samples
