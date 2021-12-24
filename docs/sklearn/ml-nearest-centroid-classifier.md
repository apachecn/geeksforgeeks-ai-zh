# ML–最近质心分类器

> 原文:[https://www . geesforgeks . org/ml-最近质心-分类器/](https://www.geeksforgeeks.org/ml-nearest-centroid-classifier/)

最近质心分类器是机器学习中最被低估和利用最少的分类器之一。然而，它非常强大，对于某些机器学习分类任务非常高效。最近质心分类器有点类似于最近邻分类器。要了解更多关于 K 近邻(KNN)分类器的信息，您可以参考下面的链接:
[K 近邻/](https://www.geeksforgeeks.org/k-nearest-neighbours/)
机器学习中一个经常被忽视的原则是从简单但有意义的数据中构建简单的算法，它可以有效地完成特定的任务，而不是使用复杂的模型。这也称为统计学中的*充分性原则*。最近质心分类器可以说是机器学习中最简单的分类算法。最近质心分类器基于一个简单的原理工作:给定一个数据点(观测值)，最近质心分类器简单地为它分配训练样本的标签(类)，该样本的平均值或质心最接近它。
当应用于文本分类时，最近质心分类器也被称为**rochio 分类器**。Python 中的 scikit-learn 库提供了一个实现最近质心分类器的简单函数。
**最近质心分类器是如何工作的？**
基本上，最近质心分类器做什么可以用三个步骤来解释:

*   训练时计算每个目标类的质心。
*   训练后，给定任何一个点，说“X”。计算点 X 和每个类的质心之间的距离。
*   从所有计算的距离中，选择最小距离。给定点的距离最小的质心，它的类被分配给给定点。

最近质心分类器非常容易理解，是最简单的分类器算法之一。
**Python 中最近质心分类器的实现:**
对于这个例子，我们将使用 scikit-learn 库中流行的‘iris’数据集。在训练分类器之后，我们将在训练集和测试集上打印分类器的准确性。然后，我们打印分类器报告。
**代码:Python 代码实现近质心分类器**

## 蟒蛇 3

```
# Importing the required libraries
from sklearn.neighbors import NearestCentroid
from sklearn.datasets import load_iris
from sklearn.metrics import classification_report
from sklearn.model_selection import train_test_split
import pandas as pd

# Loading the dataset
dataset = load_iris()

# Separating data and target labels
X = pd.DataFrame(dataset.data)
y = pd.DataFrame(dataset.target)

# Splitting training and test data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2, shuffle = True, random_state = 0)

# Creating the Nearest Centroid Classifier
model = NearestCentroid()

# Training the classifier
model.fit(X_train, y_train.values.ravel())

# Printing Accuracy on Training and Test sets
print(f"Training Set Score : {model.score(X_train, y_train) * 100} %")
print(f"Test Set Score : {model.score(X_test, y_test) * 100} %")

# Printing classification report of classifier on the test set set data
print(f"Model Classification Report : \n{classification_report(y_test, model.predict(X_test))}")
```

**输出:**

```
Training Set Score : 94.16666666666667 %
Test Set Score : 90.0 %
Model Classification Report : 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        11
           1       0.86      0.92      0.89        13
           2       0.80      0.67      0.73         6

    accuracy                           0.90        30
   macro avg       0.89      0.86      0.87        30
weighted avg       0.90      0.90      0.90        30
```

因此，我们在训练集和测试集上分别达到了 94.17%和 90%的准确率。
**结论:**
现在你已经知道了什么是最近质心分类器以及如何实现它，下次当你有一些简单的分类任务需要一个轻量级且简单的分类器时，你应该尝试使用它。