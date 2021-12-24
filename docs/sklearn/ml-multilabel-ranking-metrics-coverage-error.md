# ML |多标签排名指标–覆盖率错误

> 原文:[https://www . geesforgeks . org/ml-multi label-ranking-metrics-coverage-error/](https://www.geeksforgeeks.org/ml-multilabel-ranking-metrics-coverage-error/)

覆盖误差告诉我们有多少得分最高的最终预测标签，我们必须包括在内，而不会遗漏任何基本事实标签。如果我们想知道预测所需的最高得分预测的平均数量，以便不遗漏任何基础事实标签，这是有用的。
给定一个基本事实标签的二进制指示矩阵![y\epsilon \left \{ 0, 1 \right \}^{n_{samples} * n_{labels}}](img/56d5623e5f8790533a9269fc91ab6b8f.png "Rendered by QuickLaTeX.com")。与每个标签相关的分数由![\hat{f}](img/38285c36748a9ba2a423494fec557473.png "Rendered by QuickLaTeX.com")表示，其中，

<center>
![ \hat{f}\epsilon \left \{ \mathbb{R} \right \}^{n_{samples} * n_{labels}} ](img/15ec92b058d97f59955337e42cc6eef6.png "Rendered by QuickLaTeX.com")
</center>

The coverage error is defined as:

<center>
![ coverage\left ( y, \hat{f} \right ) = \dfrac{1}{n_{samples}} * \sum_{i=0}^{n_{samples}-1}max_{j: y_{ij}=1} rank_{ij} ](img/a91e813d30a47b31bc69bcb44ea02b9b.png "Rendered by QuickLaTeX.com")
</center>

where rank is defined as

<center>
![ rank_{ij} = \left | \left \{  k \colon \hat{f_{ik}}\geq\hat{f_{ij}} \right \}\right | ](img/b9f2dc9057cd88f06be76aa07814cb01.png "Rendered by QuickLaTeX.com")
</center>

**代码:使用 scikit-learn 检查任何带有真实标签的预测分数的覆盖率误差。**

```
# Import dataset
import numpy as np
from sklearn.metrics import coverage_error

# Create Imaginary prediction and truth dataset
y_true = np.array([[1, 0, 1], [0, 0, 1], [0, 1, 1]])
y_pred_score = np.array([[0.75, 0.5, 1], [1, 1, 1.2], [2.3, 1.2, 0.1]])
print(coverage_error(y_true, y_pred_score))
```

**输出:**

```
coverage error of *2.0*
```

让我们手动计算上述示例的覆盖误差
我们的第一个样本具有*【1，0，1】*的地面真值。为了涵盖这两个真正的标签，我们需要将我们的预测*(这里是【0.75，0.5，1】)*按照降序排列。因此，我们需要这个样本中的前 2 个预测标签。同样，对于第二个和第三个样本，我们需要 top-1 和 top-2 预测样本。对多个样本的这些结果进行平均，得到 *2.0* 的输出。

<center>
![  Coverage Error  =\dfrac{\left ( 2+1+3 \right )}{3} = 2.0  ](img/b23813a597b1de1aa01c3570f599b0c8.png "Rendered by QuickLaTeX.com")
</center>

The best value of coverage is when it is equal to average number of true class labels.