# 多标签排名指标–排名损失| ML

> 原文:[https://www . geesforgeks . org/multi label-ranking-metrics-ranking-loss-ml/](https://www.geeksforgeeks.org/multilabel-ranking-metrics-ranking-loss-ml/)

排名损失定义为相对于正确排序标签的数量，错误排序标签的数量。排名损失的最佳值可以为零

给定一个基本事实标签的二进制指示矩阵

<center>![y\epsilon \left \{ 0, 1 \right \}^{n_{samples} * n_{labels}}](img/56d5623e5f8790533a9269fc91ab6b8f.png "Rendered by QuickLaTeX.com")</center>

The score associated with each label is denoted by ![\hat{f}](img/38285c36748a9ba2a423494fec557473.png "Rendered by QuickLaTeX.com") where,

<center>
![ \hat{f}\epsilon \left \{ \mathbb{R} \right \}^{n_{samples} * n_{labels}} ](img/15ec92b058d97f59955337e42cc6eef6.png "Rendered by QuickLaTeX.com")
</center>

Ranking Loss can be calculated as :

<center>![ Ranking-Loss\left ( y, \hat{f} \right ) = \dfrac{1}{n_{samples}} * \sum_{i=0}^{n_{samples}-1}\dfrac{1}{\left \| y_{i} \right \|_0 * \left ( n_{labels}-\left \| y_i \right \|_0 \right )}  \left | \left \{  \left ( k, l \right ) \colon \hat{f_{ik}}\leq\hat{f_{il}} ; y_{ik} = 1, y_{il}=0  \right \} \right |](img/641cbcfb82be765c21fcecb0a5390329.png "Rendered by QuickLaTeX.com")
</center>

其中![ \left \| . \right \|_0](img/273b0878e3368a52c7a5b18bb011256c.png "Rendered by QuickLaTeX.com")表示集合中非零元素的个数，![\left | . \right |](img/4b924a4e4a0be3eb43a8c46adfea4b3a.png "Rendered by QuickLaTeX.com")表示向量中元素的个数(集合的基数)。最小排名损失可以是 0。这是当所有标签在预测标签中正确排序的时候。

**代码:使用 scikit-learn 库实现 Ranking Loss 的 Python 代码。**

```
# import sklearn and numpy libraries
import numpy as np
from sklearn.metrics import label_ranking_loss

# take sample dataset
y_true = np.array([[1, 0, 0], [0, 1, 0], [0, 0, 1]])
y_pred_score = np.array([[0.75, 0.5, 1], [1, 0.2, 0.1], [0.1, 1, 0.9]])

# calculate and print label ranking loss
print(label_ranking_loss(y_true, y_pred_score ))

# this will give minimum ranking loss
y_pred_score = np.array([[0.75, 0.5, 0.1], [0.1, 0.6, 0.1], [0.3, 0.3, 0.4]])
print(label_ranking_loss(y_true, y_pred_score ))
```

**输出:**

```
0.5
0
```

在第一个预测的第一个样本中，唯一的非零标签排在前 2 位。类似地，对于第二和第三样本。所有的在地面真相标签中只有一个非标签。

<center>
![ n_{label} =3 \\ ||y_0||_0 = ||y_1||_0 = ||y_2||_0 = 1 \\ ](img/bf8a8a6a3b692855dc2672ec0c6e0aaf.png "Rendered by QuickLaTeX.com")
</center>

By putting these values in the formula we get,

<center>
![ ranking-loss  = \dfrac{1}{3}\left ( \dfrac{1}{2}*1 +\dfrac{1}{2}*1+\dfrac{1}{2}*1 \right ) \\ ranking-loss = \dfrac{1}{3} * \dfrac{3}{2} \\ ranking-loss = \dfrac{1}{2} ](img/296c13413426b77778074b7e448b8db0.png "Rendered by QuickLaTeX.com")
</center>

In the second print statement, All the ground truth label corresponds to the highest value in the predicted label. Hence, the ranking loss is 0\. We can also got the same answer when we put those values in the formula because the rightmost term for each sample is *0*.
**References:**

*   左马卡斯，g .，Katakis，I .，& Vlahavas，I. (2010 年)。挖掘多标签数据。数据挖掘和知识发现手册(第 667-685 页)。斯普林格美国公司。