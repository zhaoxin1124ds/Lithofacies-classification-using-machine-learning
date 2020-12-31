![Picture1](https://user-images.githubusercontent.com/45460506/103392078-c2ba0500-4ae1-11eb-9b49-17310a60d909.png)
# Lithofacies classification using machine learning
An accurate identification of rock class is critical in oil and gas industry. It usually takes long time for petroleum specialists to examine the rock features and label the rock class. Therefore, it could be worthwhile to create a product that helps people save time by automating that process. In this project, I explore to solve this challenge using supervised learning algorithms.

This experiment is identified as a typical Classification problem:

  * Target: rock facies
  * Features: log measurement

## [Presentation](https://github.com/zhaoxin1124ds/Lithofacies-classification-using-machine-learning/blob/main/facies_classification.pdf)
https://github.com/zhaoxin1124ds/Lithofacies-classification-using-machine-learning/blob/main/facies_classification.pdf

## Data
The well log data are from real wells of Council Grove gas reservoir in Southwest Kansas. It is can be downloaded from [Github](https://https://github.com/seg/tutorials-2016/tree/master/1610_Facies_classification).

The challenge of this experiment is that the facies aren't discrete and gradually blend into one another. Some have adjacent facies that are rather close. Mislabeling within these adjacent facies can be expected to occur. So it is challenging to predict the facies accurately.

## Experiment procedure
#### Data preparation
There are total 9 wells in the data. I will use 8 for modeling and leave 1 for blind test of modeling. performance
#### Algorithms tests
I will test below supervised learning algorithms:
* Support vector machine (SVM)
* Gradient boosting (GB)
* Random forest (RM)
* Nearest neighbors (KNN)
#### Modeling performance evaluation
I designed a T-test flow to tell the significance in difference of prediction accuracy.
and choose the best model

## Evaluation
#### Best model
* _Random Forest_ is determined to have the best prediction accuracy.
#### Accuracy
* Current best F1 score from _Random Forest_ is 0.53.
* The F1 score is 0.87 if considering the adjacent facies prediction.

## More thinks for further improvement
* Some facies are not well precited as others during the experiments. I think this is due to the limited measurements available for those facies. More well information could help.
* Feature engineering to create more correlated variables could also help.
* Labeling the importance of rocks could also increase the power to evaluate the modeling performance.
