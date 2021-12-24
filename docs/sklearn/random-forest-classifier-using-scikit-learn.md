# 使用 Scikit-learn 的随机森林分类器

> 原文:[https://www . geesforgeks . org/random-forest-classifier-use-sci kit-learn/](https://www.geeksforgeeks.org/random-forest-classifier-using-scikit-learn/)

在本文中，我们将看到如何使用 Python 编程语言的 **Scikit-Learn 库**构建一个**随机森林分类器**，为了做到这一点，我们使用了 **IRIS 数据集**，这是一个相当常见和著名的数据集。随机森林或随机决策森林是一种有监督的机器学习算法，用于使用决策树进行分类、回归和其他任务。
随机森林分类器从训练集中随机选择的子集创建一组决策树。它基本上是*从训练集中随机选择的子集中选择一组决策树，然后从不同的决策树中收集投票来决定最终的预测。*
在这个分类算法中，我们将使用 IRIS 花卉数据集对模型进行训练和测试。我们将建立一个模型来分类花的类型。

**Code: Loading dataset**

```py
# importing required libraries
# importing Scikit-learn library and datasets package
from sklearn import datasets 

# Loading the iris plants dataset (classification)
iris = datasets.load_iris()   
```

**代码:检查我们的数据集内容和其中存在的要素名称。**

```py
print(iris.target_names)
```

**输出:**

```py
[‘setosa’ ‘versicolor’ ‘virginica’]
```

**代码:**

```py
print(iris.feature_names)
```

**输出:**

```py
[‘sepal length (cm)’, ’sepal width (cm)’, ’petal length (cm)’, ’petal width (cm)’]
```

**代码:**

```py
# dividing the datasets into two parts i.e. training datasets and test datasets
X, y = datasets.load_iris( return_X_y = True)

# Spliting arrays or matrices into random train and test subsets
from sklearn.model_selection import train_test_split
# i.e. 70 % training dataset and 30 % test datasets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.30)
```

**代码:导入需要的库和随机森林分类器模块。**

```py
# importing random forest classifier from assemble module
from sklearn.ensemble import RandomForestClassifier
import pandas as pd
# creating dataframe of IRIS dataset
data = pd.DataFrame({‘sepallength’: iris.data[:, 0], ’sepalwidth’: iris.data[:, 1],
                     ’petallength’: iris.data[:, 2], ’petalwidth’: iris.data[:, 3],
                     ’species’: iris.target})
```

**代码:查看数据集**

```py
# printing the top 5 datasets in iris dataset
print(data.head())
```

**输出:**

```py
     sepallength   sepalwidth   petallength     petalwidth   species

0          5.1             3.5               1.4                0.2           0

1          4.9             3.0               1.4                0.2           0

2          4.7             3.2               1.3                0.2           0

3          4.6             3.1               1.5               0.2            0

4          5.0             3.6               1.4               0.2            0
```

**代码:**

```py
# creating a RF classifier
clf = RandomForestClassifier(n_estimators = 100) 

# Training the model on the training dataset
# fit function is used to train the model using the training sets as parameters
clf.fit(X_train, y_train)

# performing predictions on the test dataset
y_pred = clf.predict(X_test)

# metrics are used to find accuracy or error
from sklearn import metrics 
print()

# using metrics module for accuracy calculation
print("ACCURACY OF THE MODEL: ", metrics.accuracy_score(y_test, y_pred))
```

**输出:**

```py
ACCURACY OF THE MODEL: 0.9238095238095239
```

**编码:从数据集预测花的类型**

```py
# predicting which type of flower it is.
clf.predict([[3, 3, 2, 2]])
```

**输出:**

```py
array([0])
```

这意味着它是**濑户花**的花型，因为我们在我们的数据集中获得了三个物种或类:**濑户花、云芝和弗吉尼亚。**现在我们也将通过使用下面几行代码来找出 IRIS 数据集中的重要特征或选择特征。

**代码:**

```py
# importing random forest classifier from assemble module
from sklearn.ensemble import RandomForestClassifier
# Create a Random forest Classifier
clf = RandomForestClassifier(n_estimators = 100)

# Train the model using the training sets
clf.fit(X_train, y_train)
```

**代码:计算特征重要性**

```py
# using the feature importance variable
import pandas as pd
feature_imp = pd.Series(clf.feature_importances_, index = iris.feature_names).sort_values(ascending = False)
feature_imp
```

**输出:**

```py
petal width (cm)     0.458607
petal length (cm)    0.413859
sepal length (cm)    0.103600
sepal width (cm)     0.023933
dtype: float64

```