# Scikit-learn 中的学习模型构建:一个 Python 机器学习库

> 原文:[https://www . geesforgeks . org/learning-model-building-sci kit-learn-python-machine-learning-library/](https://www.geeksforgeeks.org/learning-model-building-scikit-learn-python-machine-learning-library/)

先决条件:[开始机器学习](https://www.geeksforgeeks.org/getting-started-machine-learning/)
[scikit-learn](http://scikit-learn.org/stable/) 是一个开源 Python 库，使用统一的界面实现了一系列机器学习、预处理、交叉验证和可视化算法。

**sci kit-learn 的重要特性:**

*   简单高效的数据挖掘和数据分析工具。它具有各种分类、回归和聚类算法，包括支持向量机、随机森林、梯度增强、k-means 等。
*   每个人都可以访问，并且可以在各种环境中重用。
*   建立在 NumPy、SciPy 和 matplotlib 之上。
*   开源、商业可用——BSD 许可证。

在本文中，我们将看到如何使用 scikit-learn 轻松构建机器学习模型。

**安装:**

Scikit-learn 需要:

*   NumPy
*   SciPy 作为其依赖项。

在安装 scikit-learn 之前，请确保您已经安装了 NumPy 和 SciPy。一旦您安装了 NumPy 和 SciPy，安装 scikit-learn 的最简单方法就是使用 pip:

```
pip install -U scikit-learn
```

现在让我们开始建模过程。

**步骤 1:加载数据集**

数据集只不过是数据的集合。数据集通常有两个主要组成部分:

*   **特征**:(也称为预测器、输入或属性)它们只是我们数据的变量。它们可以不止一个，因此由**特征矩阵**表示(‘X’是表示特征矩阵的常用符号)。所有特征名称的列表称为**特征名称**。
*   **响应**:(也称为目标、标签或输出)这是取决于特征变量的输出变量。我们通常只有一个响应列，它由一个**响应向量**表示(‘y’是表示响应向量的常用符号)。响应向量所取的所有可能值被称为**目标名称**。

**加载样本数据集:** scikit-learn 加载了一些示例数据集，如用于分类的[虹膜](https://en.wikipedia.org/wiki/Iris_flower_data_set)和[数字](http://archive.ics.uci.edu/ml/datasets/Pen-Based+Recognition+of+Handwritten+Digits)数据集以及用于回归的[波士顿房价](http://archive.ics.uci.edu/ml/datasets/Housing)数据集。
下面给出了如何加载样本数据集的示例:

```
# load the iris dataset as an example
from sklearn.datasets import load_iris
iris = load_iris()

# store the feature matrix (X) and response vector (y)
X = iris.data
y = iris.target

# store the feature and target names
feature_names = iris.feature_names
target_names = iris.target_names

# printing features and target names of our dataset
print("Feature names:", feature_names)
print("Target names:", target_names)

# X and y are numpy arrays
print("\nType of X is:", type(X))

# printing first 5 input rows
print("\nFirst 5 rows of X:\n", X[:5])
```

输出:

```
Feature names: ['sepal length (cm)','sepal width (cm)',
                'petal length (cm)','petal width (cm)']
Target names: ['setosa' 'versicolor' 'virginica']

Type of X is: 

First 5 rows of X:
 [[ 5.1  3.5  1.4  0.2]
 [ 4.9  3\.   1.4  0.2]
 [ 4.7  3.2  1.3  0.2]
 [ 4.6  3.1  1.5  0.2]
 [ 5\.   3.6  1.4  0.2]]
```

**加载外部数据集:**现在，考虑我们想要加载外部数据集的情况。为此，我们可以使用**熊猫库**轻松加载和操作数据集。

要安装熊猫，请使用以下 pip 命令:

```
pip install pandas 
```

在熊猫中，重要的数据类型有:

**Series** : Series 是一个可以容纳任意数据类型的一维带标记数组。

**数据框架**:这是一个带有可能不同类型的列的二维标记数据结构。你可以把它想象成一个电子表格或者一个 SQL 表，或者一组 Series 对象。它一般是熊猫最常用的对象。

注意:下面例子中使用的 CSV 文件可以从这里下载: [weather.csv](http://www.sharecsv.com/dl/327fb8f66f90a98c2ed4454665efae9d/weather.csv)

```
import pandas as pd

# reading csv file
data = pd.read_csv('weather.csv')

# shape of dataset
print("Shape:", data.shape)

# column names
print("\nFeatures:", data.columns)

# storing the feature matrix (X) and response vector (y)
X = data[data.columns[:-1]]
y = data[data.columns[-1]]

# printing first 5 rows of feature matrix
print("\nFeature matrix:\n", X.head())

# printing first 5 values of response vector
print("\nResponse vector:\n", y.head())
```

输出:

```
Shape: (14, 5)

Features: Index([u'Outlook', u'Temperature', u'Humidity', 
                u'Windy', u'Play'], dtype='object')

Feature matrix:
     Outlook Temperature Humidity  Windy
0  overcast         hot     high  False
1  overcast        cool   normal   True
2  overcast        mild     high   True
3  overcast         hot   normal  False
4     rainy        mild     high  False

Response vector:
0    yes
1    yes
2    yes
3    yes
4    yes
Name: Play, dtype: object
```

**第二步:拆分数据集**

所有机器学习模型的一个重要方面是确定它们的准确性。现在，为了确定它们的准确性，可以使用给定的数据集训练模型，然后使用该模型预测同一数据集的响应值，从而找到模型的准确性。
但是这个方法有几个缺陷，比如:

*   目标是在**样本外**数据上估计模型的可能性能。
*   最大限度地提高训练精度会奖励过于复杂的模型，这些模型不一定会推广我们的模型。
*   不必要的复杂模型可能会过度拟合训练数据。

更好的选择是将我们的数据分成两部分:第一部分用于训练我们的机器学习模型，第二部分用于测试我们的模型。
**总结一下:**

*   将数据集分成两部分:训练集和测试集。
*   在训练集上训练模型。
*   在测试集上测试模型，并评估我们的模型做得有多好。

**列车/测试分流的优势:**

*   模型可以在不同于用于训练的数据上进行训练和测试。
*   测试数据集的响应值是已知的，因此可以评估预测
*   测试精度是比样本外性能的训练精度更好的估计。

考虑下面的例子:

```
# load the iris dataset as an example
from sklearn.datasets import load_iris
iris = load_iris()

# store the feature matrix (X) and response vector (y)
X = iris.data
y = iris.target

# splitting X and y into training and testing sets
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.4, random_state=1)

# printing the shapes of the new X objects
print(X_train.shape)
print(X_test.shape)

# printing the shapes of the new y objects
print(y_train.shape)
print(y_test.shape)
```

输出:

```
(90L, 4L)
(60L, 4L)
(90L,)
(60L,)
```

**train_test_split** 函数有几个参数，解释如下:

*   **X，y** :这些是需要拆分的特征矩阵和响应向量。
*   **test_size** :是测试数据与给定数据的比值。例如，为 150 行的 X 设置 test_size = 0.4 会产生 150 x 0.4 = 60 行的测试数据。
*   **random_state** :如果使用 random_state = some_number，那么可以保证你的拆分永远不变。如果您想要可重现的结果，这很有用，例如在文档一致性测试中(这样每个人都能看到相同的数字)。

**第三步:训练模型**

现在，是时候使用我们的数据集训练一些预测模型了。Scikit-learn 提供了广泛的机器学习算法，这些算法具有用于拟合、预测精度等的统一/一致接口。

下面给出的例子使用了 [KNN (K 最近邻)分类器](http://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)。

**注**:我们不赘述算法是如何工作的，因为我们只对理解其实现感兴趣。

现在，考虑下面的例子:

```
# load the iris dataset as an example
from sklearn.datasets import load_iris
iris = load_iris()

# store the feature matrix (X) and response vector (y)
X = iris.data
y = iris.target

# splitting X and y into training and testing sets
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.4, random_state=1)

# training the model on training set
from sklearn.neighbors import KNeighborsClassifier
knn = KNeighborsClassifier(n_neighbors=3)
knn.fit(X_train, y_train)

# making predictions on the testing set
y_pred = knn.predict(X_test)

# comparing actual response values (y_test) with predicted response values (y_pred)
from sklearn import metrics
print("kNN model accuracy:", metrics.accuracy_score(y_test, y_pred))

# making prediction for out of sample data
sample = [[3, 5, 4, 2], [2, 3, 5, 4]]
preds = knn.predict(sample)
pred_species = [iris.target_names[p] for p in preds]
print("Predictions:", pred_species)

# saving the model
from sklearn.externals import joblib
joblib.dump(knn, 'iris_knn.pkl')
```

输出:

```
kNN model accuracy: 0.983333333333
Predictions: ['versicolor', 'virginica']

```

上述代码中需要注意的要点:

*   我们使用

    ```
    knn = KNeighborsClassifier(n_neighbors=3) 
    ```

    创建一个 knn 分类器对象
*   使用 X_train 数据训练分类器。这个过程被称为**拟合**。我们传递特征矩阵和相应的响应向量。

    ```
    knn.fit(X_train, y_train) 
    ```

*   现在，我们需要在 X_test 数据上测试我们的分类器。 **knn.predict** 法就是为此目的而使用的。它返回预测响应向量 **y_pred** 。

    ```
    y_pred = knn.predict(X_test) 
    ```

*   现在，我们有兴趣通过比较 **y_test** 和 **y_pred** 来找到我们模型的准确性。这是使用度量模块的方法**准确度分数** :

    ```
    print(metrics.accuracy_score(y_test, y_pred)) 
    ```

    完成的
*   当你想让你的模型对样本数据中的**进行预测时，考虑这种情况。然后，可以像传递任何特征矩阵一样简单地传递样本输入。

    ```
    sample = [[3, 5, 4, 2], [2, 3, 5, 4]]
    preds = knn.predict(sample) 
    ```** 
*   如果你对反复训练你的分类器并使用预训练的分类器不感兴趣，你可以使用 **joblib** 保存他们的分类器。你需要做的就是:

    ```
    joblib.dump(knn, 'iris_knn.pkl') 
    ```

*   如果要加载已经保存的分类器，使用以下方法:

    ```
    knn = joblib.load('iris_knn.pkl')
    ```

当我们接近本文的结尾时，这里有一些使用 scikit-learn 相对于其他机器学习库(如 R 库)的好处:

*   **机器学习模型的一致接口**
*   提供许多**调谐参数**，但是有**合理的默认值**
*   例外**文件**
*   **伴随任务**的丰富功能集。
*   **活跃社区**进行开发和扶持。

**参考文献:**

*   [http://scikit-learn.org/stable/documentation.html](http://scikit-learn.org/stable/documentation.html)
*   [https://github . com/justtmarkham/scikit-learn 视频](https://github.com/justmarkham/scikit-learn-videos)

本文由[尼克尔·库马尔](https://www.facebook.com/nikhilksingh97)供稿。如果你喜欢极客博客并想投稿，你也可以用 contribute.geeksforgeeks.org 写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。