# 用 SciPy 进行 K 均值聚类

> 原文:[https://www . geesforgeks . org/k-means-clustering-with-scipy/](https://www.geeksforgeeks.org/k-means-clustering-with-scipy/)

**先决条件:** [**K-Means 聚类**](https://www.geeksforgeeks.org/k-means-clustering-introduction/)

K-Means 聚类是一种划分方法，每个聚类都用一个计算出的质心来表示。集群中的所有数据点与计算出的质心的距离最小。

**Scipy** 是一个可以用于复杂计算的开源库。它主要用于 NumPy 数组。它可以通过运行下面给出的命令来安装。

> *pip 安装 scipy*

它有专用于集群过程的包。有两个模块可以提供聚类方法。

1.  cluster.vq
2.  集群.层次结构

## cluster.vq

本模块给出了**矢量量化**的特征，用于 K-Means 聚类方法。矢量量化在减少失真和提高精度方面起着重要作用。这里的失真主要是使用质心和每个矢量之间的欧几里得距离来计算的。基于此，矢量 od 数据点被分配给一个聚类。

## 集群.层次结构

本模块提供了一般层次聚类的方法及其类型，如凝聚聚类。它有各种例程，可用于对层次结构应用统计方法、可视化聚类、绘制聚类、检查聚类中的联系，以及检查两个不同的层次结构是否等价。

本文将使用 cluster.vq 模块进行 K-Means 聚类。

## 基于 Scipy 库的 k 均值聚类

通过执行以下步骤，可以对给定的数据进行 K 均值聚类。

1.  标准化数据点。
2.  计算质心(称为代码，质心的 2D 阵列称为代码簿)。
3.  形成集群并分配数据点(称为代码簿映射)。

### cluster . VQ . blind()

此方法用于规范化数据点。当考虑的属性具有不同的单位时，规范化非常重要。例如，如果长度以米为单位，宽度以英寸为单位，可能会产生向量的不等方差。在进行 K-Means 聚类时，总是希望有单位方差，以获得准确的聚类。因此，数据数组必须在任何其他步骤之前传递给白化()方法。

> **cluster.vq .白化(input_array，check _ limited)**
> 
> 参数:
> 
> 1.  input_array:要规范化的数据点数组。
> 2.  check _ limited:如果设置为 true，则检查输入矩阵是否只包含有限个数字。如果设置为 false，将忽略检查。

### cluster.vq.kmeans()

这个 vq 模块有两种方法，即 kmeans()和 kmeans2()。

**kmeans()** 方法使用阈值，当该阈值小于或等于最后一次迭代中的失真变化时，算法终止。该方法返回计算出的质心以及观测值和质心之间的欧几里得距离的平均值。

> **cluster . VQ . kmeans(input _ array，k，迭代，阈值，check _ limited)**
> 
> 参数:
> 
> 1.  input_array:要规范化的数据点数组。
> 2.  k:簇数(质心)
> 3.  迭代次数:执行 kmeans 的迭代次数，以便最小化失真。如果指定了 k，它将被忽略。
> 4.  阈值:一个整数值，如果在最后一次迭代中变得小于或等于失真的变化，则算法终止。
> 5.  check _ limited:如果设置为 true，则检查输入矩阵是否只包含有限个数字。如果设置为 false，将忽略检查。

**kmeans2()** 方法不使用阈值检查收敛性。它有更多的参数来决定质心的初始化方法，处理空簇的方法，以及验证输入矩阵是否只包含有限个。这个方法返回质心和向量所属的簇。

> **cluster . VQ . kmeans 2(input _ array，k，迭代，threshold，minit，missing，check _ limited)**
> 
> 参数:
> 
> 1.  input_array:要规范化的数据点数组。
> 2.  k:簇数(质心)
> 3.  迭代次数:执行 kmeans 的迭代次数，以便最小化失真。如果指定了 k，它将被忽略。
> 4.  阈值:一个整数值，如果在最后一次迭代中变得小于或等于失真的变化，则算法终止。
> 5.  minit:表示质心初始化方法的字符串。可能的值有**‘随机’，‘点数’，“++”，‘矩阵’**。
> 6.  缺少:表示对空簇的操作的字符串。可能的值是**‘警告’‘升高’**。
> 7.  check _ limited:如果设置为 true，则检查输入矩阵是否只包含有限个数字。如果设置为 false，将忽略检查。

### cluster.vq.vq()

该方法将观测值映射到由 kmeans()方法计算的适当质心。它要求输入矩阵标准化。它将规范化的输入和生成的代码簿作为输入。它返回观测值对应的代码簿中的索引以及观测值与其代码(质心)之间的距离。

## **K 均值聚类与** a **2D 阵列数据**

**步骤 1:** 导入所需模块。

## 蟒蛇 3

```py
# import modules
import numpy as np
from scipy.cluster.vq import whiten, kmeans, vq, kmeans2
```