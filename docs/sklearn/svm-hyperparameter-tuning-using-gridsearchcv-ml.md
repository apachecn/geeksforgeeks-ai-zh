# 使用 GridSearchCV | ML 进行 SVM 超参数调谐

> 原文:[https://www . geesforgeks . org/SVM-超参数-调谐-使用-gridsearchcv-ml/](https://www.geeksforgeeks.org/svm-hyperparameter-tuning-using-gridsearchcv-ml/)

机器学习模型被定义为具有许多参数的数学模型，这些参数需要从数据中学习。然而，有一些参数，被称为**超参数**，这些参数不能直接学习。它们通常是人类在实际训练开始前基于某种直觉或击打和试验而选择的。这些参数通过提高模型的性能(如复杂性或学习率)来显示其重要性。模型可以有许多超参数，寻找参数的最佳组合可以被视为一个搜索问题。
**SVM** 也有一些超参数(比如用什么 C 或者 gamma 值)，找到最优超参数是一个非常难解决的任务。但只要尝试所有组合，看看什么参数效果最好，就能找到。它背后的主要思想是创建一个超参数网格，并尝试它们的所有组合(因此，这种方法被称为 **Gridsearch** ，但不要担心！我们不需要手动操作，因为 Scikit-learn 在 GridSearchCV 中内置了这一功能。
**GridSearchCV** 拿着一本描述可以在模型上尝试的参数的字典来训练它。参数网格被定义为字典，其中键是参数，值是要测试的设置。
本文演示了如何使用 **GridSearchCV** 搜索方法找到最佳超参数，从而提高精度/预测结果

### 导入必要的库并获取数据:

我们将使用 Scikit Learn 的内置乳腺癌数据集。我们可以通过负载函数得到:

## 蟒蛇 3

```
import pandas as pd
import numpy as np
from sklearn.metrics import classification_report, confusion_matrix
from sklearn.datasets import load_breast_cancer
from sklearn.svm import SVC

cancer = load_breast_cancer()

# The data set is presented in a dictionary form:
print(cancer.keys())
```