# Metrics for Multiclass Classification

When you move from binary → multiclass, you now have many “positive” classes (digits 0–9).
So how do you define “precision,” “recall,” or “F1” when there’s more than one class?

Answer:
You treat each class as if it were binary (“this class” vs. “all others”) → compute metrics for each → then average them.





Accuracy = correct predictions ÷ total samples.
In the digits example, it’s 95.3%, which looks great.
But if one class (say “0”) is much more common, accuracy could still be misleading — same problem as before.

So we use confusion matrix + classification report for more insight.


Because you have 10 classes, you can average the 10 F1-scores in three ways:

| Type         | How It’s Computed                                       | When to Use                                                                   |
| ------------ | ------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Micro**    | Combine all TP, FP, FN across classes → then compute F1 | When you care about **each sample equally** (like overall accuracy)           |
| **Macro**    | Mean of per-class F1s (equal weight per class)          | When you care about **each class equally**, even rare ones                    |
| **Weighted** | Mean of per-class F1s weighted by class size            | When classes are **imbalanced**, and you want to reflect dataset distribution |
