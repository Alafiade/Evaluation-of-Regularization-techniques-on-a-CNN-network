# Evaluation-of-Regularization-techniques-on-a-CNN-network

This project evaluates regularization techinques such as batch normalization and dropout to understand how they affect a model's performance.

Convolutional Neural Networks are prone to overfitting when trained on small datasets, to address this challenge, regularization techniques are used. The aim of these techniques is to improve generalization. In this project i  investigated two regularization techniques called dropout and batch-normalization, the goal was to evaluate individually and combined the effect these regularization  techniques have on a custom built CNN architecture trained on CIFAR 10 and to see whether implementation of these techniques can yield to better generalization and model performance.

## Model Performance Comparison

| Model Variant          | Epochs | Train Accuracy | Test Accuracy |
|------------------------|--------|---------------|---------------|
| BatchNorm Only         | 50     | 1.00          | 0.46          |
| Dropout Only           | 40     | 0.92          | 0.52          |
| BatchNorm + Dropout    | 40     | 0.93          | 0.54          |

Dataset used: CIFAR-10
Optimizer: SGD(momentum =0.9, lr = 0.01)
Architecture: 3 convolutional layers buit from scracth

## Interpretation of results
- Batch Normalization Only
  Train Accuracy:  1.00
  Test Accuracy: 0.46

This indicates severe overfitting because batchnormalization is not a strong regularizer. It improves convergency speed ans stabilizes learning.

- Dropout Only
  Training Accuracy: 0.92
  Test Accuracy: 0.52

This is a much more improvement  compared to the individual implementation of batch norm. The dropout reduced overfitting comparesd to batch norm and the generalization gap is smaller.

- Batch Norm + Dropout
  Train Accuracy: 0.93
  Test Accuracy: 0.54

Compared to the implementation of dropout we have a significant improvement in the test accuracy and the smallest overfitting gap among the  other models,

## Conclusion
This experiment evaluated the impact of individual and combined regularization techniques on a custom CNN trained on CIFAR-10, The results shows that implementing a single regularization technique is not enough to achieve a good generalization. To further improve the model's perfomance regularization strategies such as weight decay and data augmentation could be implemented. Together these twchniques could reduce overfitting and improve generalization
  




