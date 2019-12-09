# Task2

## Task2 - Description

"This task is primarily concerned with multi-class classification where you have 3 classes. However, we have changed the original image features in several ways. You will need to deal with class imbalance; in the training set, there are 600 examples from class 0 and 2 but 3600 examples from class 1. Test set has the same class imbalance as the training set."

## Task2 - Solution

The problem was a classification task. We had 3 classes but these were unbalanced with one to have a significantly higher number of samples. To fix the unbalanced classes different techniques were used including upsampling of the classes with lower number of samples and downsampling of the class with higher number of samples. All of these techniques were outperformed though by using different weights for the penalty term. In this way we use all the power of the real dataset since we don't lose information like we did in the downsampling scenario either we introduce artificial information which might be wrong like we did in the upsampling scenario. Finally, using cross-validation we tested different models for the classification task. The best model proved to be through the cross-validation a Support Vector Machine model for the classification task. More precisely we used the SVC function from sklearn package. For the hyperparameters we used balanced classes weights and One -Versue -Rest strategy and C = 1.0 for the penalty term error. The model has 0.702 mean score in the cross-validation and 0.7185 in the public scoreboard.

