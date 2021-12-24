# 使用 Python 中的 sklearn 进行同质性评分

> 原文:[https://www . geesforgeks . org/同质 _ score-using-sklearn-in-python/](https://www.geeksforgeeks.org/homogeneity_score-using-sklearn-in-python/)

一个完全同质的聚类是指每个聚类都有指向相似类别标签的信息。同质性描绘了聚类算法对这种(*同质性 _ 得分*)完美性的接近程度。

这个度量独立于标签的直接值。聚类标签值的排列不会以任何方式改变分值。

> **语法:** sklearn.metrics .同质性 _score(labels_true，labels_pred)
> 
> 度量不对称，将*标签 _ 真*切换为*标签 _ 预解码*将返回*完整性分数*。
> 
> **参数:**
> 
> *   **标签 _ 真:<** *int array，shape =【n _ samples】*>**:**它接受地面真类标签作为参考。
> *   **标签 _pred:** < *阵列状的形状(n_samples)，* > **:** 它接受要评估的聚类标签。
> 
> **返回:**
> 
> **同质:<** *浮动* > **:** 其返回 0.0 到 1.0 之间的分数代表完全同质标注。

**示例 1:**

## 蟒蛇 3

```py
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn.metrics import homogeneity_score

# Changing the location file
# cd C:\Users\Dev\Desktop\Credit Card Fraud

# Loading the data
df = pd.read_csv('creditcard.csv')

# Separating the dependent and independent variables
y = df['Class']
X = df.drop('Class', axis=1)

# Building the clustering model
kmeans = KMeans(n_clusters=2)

# Training the clustering model
kmeans.fit(X)

# Storing the predicted Clustering labels
labels = kmeans.predict(X)

# Evaluating the performance
homogeneity_score(y, labels)
```

**输出:**

```py
0.00496764949717645

```

**实施例 2:** 完全均匀:

## 蟒蛇 3

```py
from sklearn.metrics.cluster import homogeneity_score

# Evaluate the score
hscore = homogeneity_score([0, 1, 0, 1], [1, 0, 1, 0])

print(hscore)
```

**输出:**

```py
1.0

```

**示例 3:** 进一步将类分成更多簇的非完美标签可以是完全同质的:

## 蟒蛇 3

```py
from sklearn.metrics.cluster import homogeneity_score

# Evaluate the score
hscore = homogeneity_score([0, 0, 1, 1], [0, 1, 2, 3])

print(hscore)
```

**输出:**

```py
0.9999999999999999

```

**示例 4:** 包含不同类别的样本不适合同质标记:

## 蟒蛇 3

```py
from sklearn.metrics.cluster import homogeneity_score

# Evaluate the score
hscore = homogeneity_score([0, 0, 1, 1], [0, 1, 0, 1])

print(hscore)
```

**输出:**

```py
0.0

```