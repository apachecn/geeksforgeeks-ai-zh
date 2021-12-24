# ML |使用 Sklearn 的投票分类器

> 原文:[https://www . geesforgeks . org/ml-投票-分类器-使用-sklearn/](https://www.geeksforgeeks.org/ml-voting-classifier-using-sklearn/)

投票分类器是一种机器学习模型，它在众多模型的集合上进行训练，并根据所选类别作为输出的最高概率来预测输出(类别)。
它简单地聚合传递到投票分类器的每个分类器的发现，并基于投票的最高多数预测输出类。我们的想法是，不是创建单独的专用模型并找到每个模型的准确性，而是创建一个单一的模型，根据这些模型进行训练，并根据每个输出类的投票总数预测输出。

投票分类器支持两种类型的投票。

1.  **硬投票:**在硬投票中，预测输出类是具有最高多数票的类，即每个分类器预测概率最高的类。假设三个分类器预测了*输出类(A，A，B)* ，那么这里大多数预测了 *A* 作为输出。因此 *A* 将是最终预测。
2.  **软投票:**在软投票中，输出类是基于给予该类概率平均值的预测。假设给定三个模型的一些输入，类 *A = (0.30，0.47，0.53)* 和 *B = (0.20，0.32，0.40)* 的预测概率。所以类 *A 的平均值为 0.4333* ， *B 的平均值为 0.3067* ，赢家显然是类 *A* ，因为它拥有每个分类器平均的最高概率。

**注意:**确保包含各种模型来馈送投票分类器，以确保一个模型产生的错误可能被另一个模型解决。
**代码:实现投票分类器的 Python 代码**

```
# importing libraries
from sklearn.ensemble import VotingClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.svm import SVC
from sklearn.tree import DecisionTreeClassifier
from sklearn.datasets import load_iris
from sklearn.metrics import accuracy_score
from sklearn.model_selection import train_test_split

# loading iris dataset
iris = load_iris()
X = iris.data[:, :4]
Y = iris.target

# train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, 
                                                    Y, 
                                                    test_size = 0.20, 
                                                    random_state = 42)

# group / ensemble of models
estimator = []
estimator.append(('LR', 
                  LogisticRegression(solver ='lbfgs', 
                                     multi_class ='multinomial', 
                                     max_iter = 200)))
estimator.append(('SVC', SVC(gamma ='auto', probability = True)))
estimator.append(('DTC', DecisionTreeClassifier()))

# Voting Classifier with hard voting
vot_hard = VotingClassifier(estimators = estimator, voting ='hard')
vot_hard.fit(X_train, y_train)
y_pred = vot_hard.predict(X_test)

# using accuracy_score metric to predict accuracy
score = accuracy_score(y_test, y_pred)
print("Hard Voting Score % d" % score)

# Voting Classifier with soft voting
vot_soft = VotingClassifier(estimators = estimator, voting ='soft')
vot_soft.fit(X_train, y_train)
y_pred = vot_soft.predict(X_test)

# using accuracy_score
score = accuracy_score(y_test, y_pred)
print("Soft Voting Score % d" % score)
```

**输出:**

```
Hard Voting Score 1
Soft Voting Score 1
```

**示例:**

```
Input  :4.7, 3.2, 1.3, 0.2 
Output :Iris Setosa 

```

实际上，软投票的输出精度会更高，因为它是所有估计器组合的平均概率，至于我们的基本虹膜数据集，我们已经过度拟合了，所以输出不会有太大差异。