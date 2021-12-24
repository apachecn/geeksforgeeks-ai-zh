# Python–迭代 NumPy 中的列

> 原文:[https://www . geesforgeks . org/python-iterate-over-columns-in-numpy/](https://www.geeksforgeeks.org/python-iterate-over-columns-in-numpy/)

`Numpy`(简称“*数值 Python* ”)是一个快速高效执行大规模数学运算的库。本文旨在向您介绍可以用来迭代 2D `NumPy`数组中的列的方法。由于一维数组仅由线性元素组成，因此其中不存在行和列的区别定义。因此，为了执行这样的操作，我们需要一个其 *`len(ary.shape) > 1` 的数组。*

要在 python 环境中安装`NumPy`，请在操作系统的命令处理器( **CMD、Bash** 等)中键入以下代码:

> pip 安装 numpy

我们将研究迭代数组/矩阵的一列的几种方法:-

**方法 1:**

**代码:在一个数组上使用原始 2D 切片操作来获得所需的一列或多列**

```
import numpy as np

# Creating a sample numpy array (in 1D)
ary = np.arange(1, 25, 1)

# Converting the 1 Dimensional array to a 2D array 
# (to allow explicitly column and row operations)
ary = ary.reshape(5, 5)

# Displaying the Matrix (use print(ary) in IDE)
print(ary)

# This for loop will iterate over all columns of the array one at a time
for col in range(ary.shape[1]):
    print(ary[:, col])
```

**输出:**

```
[[ 0,  1,  2,  3,  4],
 [ 5,  6,  7,  8,  9],
 [10, 11, 12, 13, 14],
 [15, 16, 17, 18, 19],
 [20, 21, 22, 23, 24]])

[ 0  5 10 15 20]
[ 1  6 11 16 21]
[ 2  7 12 17 22]
[ 3  8 13 18 23]
[ 4  9 14 19 24]

```

**说明:**

在上面的代码中，我们首先使用 *`np.arange(25)`* 创建一个由 25 个元素(0-24)组成的线性数组。然后，我们使用 *`np.reshape()`* 重塑(将 1D 转换为 2D)，从线性阵列中创建 2D 阵列。然后我们输出转换后的数组。现在，我们使用了一个 for 循环，该循环将迭代 *x* 次(其中 x 是数组中的列数)，我们将 *`range()`* 与参数 *`ary.shape[1]`* 一起使用(其中*`shape[1]`*= 2D 对称数组中的列数)。在每次迭代中我们使用 *`ary[:, col]`* 从数组中输出一列，这意味着给定列的所有元素编号= *`col`* 。

**方法 2:**
在这个方法中，我们会转置数组，将每个列元素视为行元素(这又相当于列迭代)。

**代码:**

```
# libraries
import numpy as np

# Creating an 2D array of 25 elements 
ary = np.array([[ 0,  1,  2,  3,  4],
                [ 5,  6,  7,  8,  9],
                [10, 11, 12, 13, 14],
                [15, 16, 17, 18, 19],
                [20, 21, 22, 23, 24]])

# This loop will iterate through each row of the transposed 
# array (equivalent of iterating through each column)
for col in ary.T:
    print(col)
```

**输出:**

```

[ 0  5 10 15 20]
[ 1  6 11 16 21]
[ 2  7 12 17 22]
[ 3  8 13 18 23]
[ 4  9 14 19 24]

```

**说明:**
首先，我们使用 *`np.array()`* 创建了一个 2D 数组(与前面的例子相同)，并用 25 个值初始化它。然后我们转置数组，使用 *`ary.T`* 依次切换行和列以及列和行。然后我们迭代这个转置数组的每一行，并打印行值。