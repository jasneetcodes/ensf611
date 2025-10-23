# Metrics for Binary Classification


## Unbalanced Data and Accuracy as a metric
Most data set in the real world is skewed
- Majority of the data goes one way, meaning in binary classification there is one class that is majority and one minority

This can cause accuracy (prediction) evaluation metric to not really show a clear picture

Accuracy evaluates = correct predictions / total predictions

WHY?

If the majority of the data goes one way, lets say 70% then even a dummy model that simply always predicts that class (ex. no), it will still give us a score of 70%. It doesn't even do any anything!!


## Confusion Matrices

A way to visualize the evaluation of binary classifcation.

Gives us a 2 X 2 array. The rows represent the TRUE Classes and the Columns represent the Predicted Classes.

Negative class row on top
Positive class row on bottom

Predicted negative first row
Predicted positive second row
 
So positive on bottom row and second column
Negative top row and first column

Negative, positive, negative, positive


## Evaluation Formulas

Accuracy = TP + TN / TP + TN + FP + FN

- Number of correct predictions / number of all samples


Precision = TP / TP + FP

- Measures how many predicted positives were truly positives
- Used when you want to limit the number of false positives
- Model should maximize ONLY True positives
- Ex. Effectiveness of a new drug
- Also known as positive predictive value (PPV)

Recall = TP / TP + FN

- Measures how many positive samples were correctly caught as true positives
- Used when you want to know all the positive samples
- Want to limit the false negatives
- Ex. System to detect cancer in patients, Cannot have false negatives
- Also known as sensitivity, hit rate, true positive rate (TPR)


F-score = 2 * (precision * recall / precision + recall)

- Harmonic mean of precisoin and recall
- Penalizes models that do well on one metric but poorly on the other


## Uncertainty into account

most classifiers use decision_function or predict_proba methods to assess degrees of certainty about predictions

Binary classification we use 0 for decison function, and 0.5 for predict_proba


** To increase recall (catch more positives at the risk of FP) we can adjust decision_function away from 0.
- Points with a decision_function value greater than 0 are = Class 1
- So reduce decision_function treshold to less than 0 to have more Class 1

With predict_proba, we use a range of 0 to 1. So with the default .5
- Model needs to be 50% sure that the point is of the positive class to classify it as such
- Increasing threshold, means model needs to be more sure to label a point as positive


## Precicion - Recall curves and ROC curves


Setting a req like 90% recall is called OPERATING POINT

To know the trade offs between precision and recall, we can use the precision-recall 
- Returns a list of precision and recall values for all possible threshold (all values in decision function) in sorted order


CAn use average precison to get area under the curve of the precision recall curve
- 0 to 1
- AP of random classifier ~~ fraction of positive samples in data -> 0.1 if 10% positives.
- Expected precision across all recall levels
- How well does the model find rare positives while avoiding false alarms?


## Receiver operating characteristics ROC and AUC

It shows false positive rate against the true positive rate

true positive rate = recall
false positive rate = fraction of FP out of all negative samples

FPR = FP / FP + TN

X = FPR
Y = TPR (recall)

Best curve is close to top left, produce HIGH recall and low false positive rate

AUC is the area under the ROC curve
- Range of 0 to 1
- Probability that a randomly chosen positive example will get a higher model score than a randomly chosen negative one
- Can the model rank positives above negatives overall?

The higher the AUC, the more often the model gives higher scores to real positives than to negatives.
That means the model has learned a meaningful scale of “how positive something is


The model has learned a good internal scale — it gives higher scores to true positives and lower scores to true negatives consistently.

In plain terms:

The model can separate (differentiate) the two classes well, even before deciding where to cut off (threshold).






