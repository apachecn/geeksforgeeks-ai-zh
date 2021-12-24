# 管道 Python 和 sci kit-学习

> 原文:[https://www . geesforgeks . org/pipelines-python-and-sci kit-learn/](https://www.geeksforgeeks.org/pipelines-python-and-scikit-learn/)

任何机器学习项目的工作流程都包括构建它所需的所有步骤。一个合适的 ML 项目基本上由四个主要部分组成，如下所示:

*   **收集数据:**
    收集数据的过程取决于项目，可以是实时数据，也可以是从文件、数据库、调查等各种来源收集的数据。
*   **数据预处理:**
    通常情况下，在采集的数据内部，有大量的缺失数据、超大值、无组织的文本数据或有噪声的数据，因而无法在模型内部直接使用，因此，数据在进入模型之前需要进行一些预处理。
*   **训练和测试模型:**一旦数据准备好用于算法应用，那么它就准备好放入机器学习模型。在此之前，重要的是要知道要使用什么模型，这可能会提供良好的性能输出。数据集分为 3 个基本部分，即训练集、验证集和测试集。主要目的是在训练集中训练数据，使用“验证集”调整参数，然后测试性能测试集。
*   **评估:**
    评估是模型开发过程的一部分。它有助于找到代表数据的最佳模型，以及所选模型在未来的运行情况。这是在完成不同算法中的模型训练之后完成的。主要座右铭是总结评估，并据此重新选择模型。

**python 中的 ML Workflow**
工作流的执行是管道式的，即第一步的输出变成第二步的输入。Scikit-learn 是一个强大的机器学习工具，在名为 pipeline 的 sklearn.pipeline 模块下提供了处理这种管道的功能。
需要 2 个重要参数，说明如下:

*   **步骤列表:**
    按链接顺序排列的(名称、转换)元组列表(实现拟合/转换)，最后一个对象是估计器。
*   **啰嗦:**

**代码:**

## 蟒蛇 3

```py
from sklearn import datasets
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
from sklearn.tree import DecisionTreeClassifier
# import some data within sklearn for iris classification
iris = datasets.load_iris()
X = iris.data
y = iris.target

# Splitting data into train and testing part
# The 25 % of data is test size of the data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.25)
# importing pipes for making the Pipe flow
from sklearn.pipeline import Pipeline
# pipe flow is :
# PCA(Dimension reduction to two) -> Scaling the data -> DecisionTreeClassification
pipe = Pipeline([('pca', PCA(n_components = 2)), ('std', StandardScaler()), ('decision_tree', DecisionTreeClassifier())], verbose = True)

# fitting the data in the pipe
pipe.fit(X_train, y_train)

# scoring data
from sklearn.metrics import accuracy_score
print(accuracy_score(y_test, pipe.predict(X_test)))
```

**输出:**

```py
[Pipeline] ............... (step 1 of 3) Processing pca, total=   0.0s
[Pipeline] ............... (step 2 of 3) Processing std, total=   0.0s
[Pipeline] ..... (step 3 of 3) Processing Decision_tree, total=   0.0s
0.9736842105263158
```

**重要物业:**

*   **pipe . named _ steps:**pipe . named _ steps 是一个字典，存储链接到管道中各个对象的名称键。例如:

```py
pipe.named_steps['decision_tree'] # returns a decision tree classifier object  
```

**超参数:**
在作为管道传入的类中有不同的超参数集。要查看它们，请使用 pipe.get_params()方法。此方法返回管道中每个类的参数和描述的字典。
**例:**

## 蟒蛇 3

```py
from sklearn import datasets
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
from sklearn.tree import DecisionTreeClassifier
# import some data within sklearn for iris classification
iris = datasets.load_iris()
X = iris.data
y = iris.target

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.25)

from sklearn.pipeline import Pipeline
pipe = Pipeline([('pca', PCA(n_components = 2)), ('std', StandardScaler()), ('Decision_tree', DecisionTreeClassifier())], verbose = True)

pipe.fit(X_train, y_train)

# to see all the hyper parameters
pipe.get_params()
```

**输出:**

```py
{'memory': None,
 'steps': [('pca',
   PCA(copy=True, iterated_power='auto', n_components=2, random_state=None,
       svd_solver='auto', tol=0.0, whiten=False)),
  ('std', StandardScaler(copy=True, with_mean=True, with_std=True)),
  ('Decision_tree',
   DecisionTreeClassifier(ccp_alpha=0.0, class_weight=None, criterion='gini',
                          max_depth=None, max_features=None, max_leaf_nodes=None,
                          min_impurity_decrease=0.0, min_impurity_split=None,
                          min_samples_leaf=1, min_samples_split=2,
                          min_weight_fraction_leaf=0.0, presort='deprecated',
                          random_state=None, splitter='best'))],
 'verbose': True,
 'pca': PCA(copy=True, iterated_power='auto', n_components=2, random_state=None,
     svd_solver='auto', tol=0.0, whiten=False),
 'std': StandardScaler(copy=True, with_mean=True, with_std=True),
 'Decision_tree': DecisionTreeClassifier(ccp_alpha=0.0, class_weight=None, criterion='gini',
                        max_depth=None, max_features=None, max_leaf_nodes=None,
                        min_impurity_decrease=0.0, min_impurity_split=None,
                        min_samples_leaf=1, min_samples_split=2,
                        min_weight_fraction_leaf=0.0, presort='deprecated',
                        random_state=None, splitter='best'),
 'pca__copy': True,
 'pca__iterated_power': 'auto',
 'pca__n_components': 2,
 'pca__random_state': None,
 'pca__svd_solver': 'auto',
 'pca__tol': 0.0,
 'pca__whiten': False,
 'std__copy': True,
 'std__with_mean': True,
 'std__with_std': True,
 'Decision_tree__ccp_alpha': 0.0,
 'Decision_tree__class_weight': None,
 'Decision_tree__criterion': 'gini',
 'Decision_tree__max_depth': None,
 'Decision_tree__max_features': None,
 'Decision_tree__max_leaf_nodes': None,
 'Decision_tree__min_impurity_decrease': 0.0,
 'Decision_tree__min_impurity_split': None,
 'Decision_tree__min_samples_leaf': 1,
 'Decision_tree__min_samples_split': 2,
 'Decision_tree__min_weight_fraction_leaf': 0.0,
 'Decision_tree__presort': 'deprecated',
 'Decision_tree__random_state': None,
 'Decision_tree__splitter': 'best'}
```