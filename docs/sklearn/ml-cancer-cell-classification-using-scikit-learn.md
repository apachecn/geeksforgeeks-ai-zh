# ML |使用 Scikit 进行癌细胞分类-学习

> 原文:[https://www . geesforgeks . org/ml-癌细胞-分类-使用-scikit-learn/](https://www.geeksforgeeks.org/ml-cancer-cell-classification-using-scikit-learn/)

机器学习是人工智能的一个子领域，它赋予系统在没有被明确编程的情况下学习自己的能力。机器学习可以用于解决许多现实世界的问题。
让我们根据癌细胞的特征进行分类，并识别它们是‘恶性’还是‘良性’。我们将使用 scikit-learn 解决机器学习问题。Scikit-learn 是一个开源的 Python 编程语言的机器学习、数据挖掘和数据分析库。
**数据集:**
Scikit-learn 附带了一些小型标准数据集，不需要从任何外部网站下载任何文件。我们将用于机器学习问题的数据集是威斯康星乳腺癌(诊断)数据集。数据集包括几个关于乳腺癌肿瘤的数据以及分类标签，即。，恶性或良性。可以使用以下功能加载:

```
load_breast_cancer([return_X_y])
```

该数据集有 569 个肿瘤的 569 个实例或数据，包括 30 个属性或特征的数据，如半径、纹理、周长、面积等。一个肿瘤。我们将使用这些功能来训练我们的模型。
**安装必要的模块:**
对于这个机器学习项目，我们将需要‘Scikit-learn’Python 模块。如果您的机器上没有安装它，请通过在命令提示符下运行以下命令来下载并安装它:

```
pip install scikit-learn
```

**注:**本项目可以使用任何 IDE，强烈推荐使用 Jupyter 笔记本进行项目。这是因为，由于 Python 是一种解释语言，所以，人们可以通过运行几行代码来充分利用它，一步一步地看到和理解正在发生的事情，而不是编写整个脚本，然后运行一次。
在命令提示符下运行以下命令进行安装:

```
pip install jupyter
```

#### 使用 Scijit-learn 逐步实施分类:

**步骤#1:** 导入必要的模块和数据集。
我们将需要“Scikit-learn”模块和威斯康星乳腺癌(诊断)数据集。

## 蟒蛇 3

```
# importing the Python module
import sklearn

# importing the dataset
from sklearn.datasets import load_breast_cancer
```

**步骤 2:** 将数据集加载到变量中。

## 蟒蛇 3

```
# loading the dataset
data = load_breast_cancer()
```

我们必须从该数据集中考虑的重要属性是“目标名称”(标签的含义)、“目标”(分类标签)、“特征名称”(特征的含义)和“数据”(要学习的数据)。
**第三步:**整理数据并查看。
为了更好地理解数据集包含什么，以及我们可以如何使用数据来训练我们的模型，让我们首先组织数据，然后使用 print()函数查看它包含什么。

## 蟒蛇 3

```
# Organize our data
label_names = data['target_names']
labels = data['target']
feature_names = data['feature_names']
features = data['data']
```

然后，使用**打印()**功能，让我们检查数据。

## 蟒蛇 3

```
# looking at the data
print(label_names)
```

**输出:**

```
['malignant' 'benign']
```

因此，我们看到肿瘤的每个数据集都被标记为“恶性”或“良性”。

## 蟒蛇 3

```
print(labels)
```

**输出:**

```
[0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 1 0 0 0 0 0 0 0 0 1 0 1 1 1 1 1 0 0 1 0 0 1 1 1 1 0 1 0 0 1 1 1 1 0 1 0 0
 1 0 1 0 0 1 1 1 0 0 1 0 0 0 1 1 1 0 1 1 0 0 1 1 1 0 0 1 1 1 1 0 1 1 0 1 1
 1 1 1 1 1 1 0 0 0 1 0 0 1 1 1 0 0 1 0 1 0 0 1 0 0 1 1 0 1 1 0 1 1 1 1 0 1
 1 1 1 1 1 1 1 1 0 1 1 1 1 0 0 1 0 1 1 0 0 1 1 0 0 1 1 1 1 0 1 1 0 0 0 1 0
 1 0 1 1 1 0 1 1 0 0 1 0 0 0 0 1 0 0 0 1 0 1 0 1 1 0 1 0 0 0 0 1 1 0 0 1 1
 1 0 1 1 1 1 1 0 0 1 1 0 1 1 0 0 1 0 1 1 1 1 0 1 1 1 1 1 0 1 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 1 1 1 1 1 1 0 1 0 1 1 0 1 1 0 1 0 0 1 1 1 1 1 1 1 1 1 1 1 1
 1 0 1 1 0 1 0 1 1 1 1 1 1 1 1 1 1 1 1 1 1 0 1 1 1 0 1 0 1 1 1 1 0 0 0 1 1
 1 1 0 1 0 1 0 1 1 1 0 1 1 1 1 1 1 1 0 0 0 1 1 1 1 1 1 1 1 1 1 1 0 0 1 0 0
 0 1 0 0 1 1 1 1 1 0 1 1 1 1 1 0 1 1 1 0 1 1 0 0 1 1 1 1 1 1 0 1 1 1 1 1 1
 1 0 1 1 1 1 1 0 1 1 0 1 1 1 1 1 1 1 1 1 1 1 1 0 1 0 0 1 0 1 1 1 1 1 0 1 1
 0 1 0 1 1 0 1 0 1 1 1 1 1 1 1 1 0 0 1 1 1 1 1 1 0 1 1 1 1 1 1 1 1 1 1 0 1
 1 1 1 1 1 1 0 1 0 1 1 0 1 1 1 1 1 0 0 1 0 1 0 1 1 1 1 1 0 1 1 0 1 0 1 0 0
 1 1 1 0 1 1 1 1 1 1 1 1 1 1 1 0 1 0 0 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
 1 1 1 1 1 1 1 0 0 0 0 0 0 1]
```

从这里，我们看到每个标签都链接到二进制值 0 和 1，其中 0 代表恶性肿瘤，1 代表良性肿瘤。

## 蟒蛇 3

```
print(feature_names)
```

**输出:**

```
['mean radius' 'mean texture' 'mean perimeter' 'mean area'
 'mean smoothness' 'mean compactness' 'mean concavity'
 'mean concave points' 'mean symmetry' 'mean fractal dimension'
 'radius error' 'texture error' 'perimeter error' 'area error'
 'smoothness error' 'compactness error' 'concavity error'
 'concave points error' 'symmetry error' 'fractal dimension error'
 'worst radius' 'worst texture' 'worst perimeter' 'worst area'
 'worst smoothness' 'worst compactness' 'worst concavity'
 'worst concave points' 'worst symmetry' 'worst fractal dimension']
```

在这里，我们看到了肿瘤的每个数据集所具有的全部 30 个特征或属性。我们将使用这些特征的数值来训练我们的模型，并根据这些特征做出正确的预测，无论肿瘤是恶性还是良性。

## 蟒蛇 3

```
print(features)
```