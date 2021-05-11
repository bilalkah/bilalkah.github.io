---
title: Machine Learning Metrics
published: true
---

# Classification Metrics

When we built our model for a specific purpose and trained it for this goal with some data, we need to check situation of the model. In this way, we can understand what we are doing. With these metrics, we would able to understand which outputs are most confused with each other, how much is the model generalizable, does the model memorize the input and so on. 

# Accuracy

Accuracy, which is the most well-know metric, the ratio of the total number of correct predictions to the total number of predictions. 
```
Accuracy = (Total Number of True Predictions) / (Total Predictions) 
```
Although it is used more frequently than other metrics, it does not always give the correct output. For example, consider there are 95% samples of class A and 5% samples of class B in our dataset. After training, our model probably predicts everything as class A then we will get 95% accuracy which is not correct. Accuracy can be useful when dataset is balanced. However, if we want to have a full picture of the model evaluation, other metrics also should be considered.

# Confusion Matrix

The confusion matrix is ​​like a table in which we can compare the Model estimation outputs with the actual output. We observe 4 different metrics (TP, FP, FN, TN) from here. 

|Samples |Predicted: NO|Predicted: YES|
|-|-|-|
|Actual: NO| TN | FP |
|Actual: Yes| FN | TP |

- True Positives (TP) : Actual Output YES, Predicted Output YES
- True Negatives (TN) : Actual Output NO, Predicted Output NO
- False Positives (FP) : Actual Output NO, Predicted Output YES
- False Negatives (FN) : Actual Output YES, Predicted Output NO

The accuracy metric is obtained by dividing the sum of the diagonal axis of the confusion matrix by the sum of the cells of the matrix.

```
Accuracy = (TP + TN) / (TP + FP + FN + TN)
```

The confusion matrix is so fundamental metric that it is the basis for the other types of metrics. 

# Recall (Sensitivity)

Recall is a metric used to measure correctly predicted instances of a class. It gives us a kind of class-based accuracy.

```
Recall = (TP) / (TP + FN)
```

# Precision (Specificity)

Precision is a measure to check the proportion of identifications was correct. It is very useful if our dataset is imbalanced.

```
Precision = (TP) / (TP + FP)
``` 

# F1 Score

F1 Score is a combination of Presicion and Recall. When we want to improve both of these metrics, we would use F1. The formula is the harmonic mean of the precision and the recall.

```
F1 = 2 / ((1 / Recall) + (1 / Precision))
```

# Receiver Operating Characteristic Curve (ROC Curve)

A Roc Curve is a graph showing the performance of a classification model at all classification thresholds. It plots two parameters:
- True Positive Rate (TPR) (Sensitivity)
```
TPR = (TP) / (TP + FN)
```
- False Positive Rate (FPR) (1 - Specificity)
```
FPR = (FP) / (FP + TN)
```
The graph consists of the ratio of TPR to FPR for various threshold values and makes it easy to identify the best threshold for making a decision.

# Area Under Curve (AUC)

AUC is one of the most used metrics for model evaluation. It is used for binary classification problem. It is a representation of the probability that the model will rank a randomly chosen positive example higher than a randomly chosen negative example. So, when we have to ROC Curve and we need to decide which one is better? The AUC will give us the answer to that question.



### References

https://towardsdatascience.com/20-popular-machine-learning-metrics-part-1-classification-regression-evaluation-metrics-1ca3e282a2ce

https://towardsdatascience.com/metrics-to-evaluate-your-machine-learning-algorithm-f10ba6e38234

https://www.kdnuggets.com/2020/04/performance-evaluation-metrics-classification.html#:~:text=The%20key%20classification%20metrics%3A%20Accuracy,Receiver%20Operating%20Characteristic%20(ROC)%20curve