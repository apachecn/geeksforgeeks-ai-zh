# 如何得到给定 NumPy 数组沿第二轴的最小值和最大值？

> 原文:[https://www . geesforgeks . org/如何沿第二轴获取给定 numpy 数组的最小值和最大值/](https://www.geeksforgeeks.org/how-to-get-the-minimum-and-maximum-value-of-a-given-numpy-array-along-the-second-axis/)

让我们看看如何沿着第二个轴获得给定 NumPy 数组的最小值和最大值。这里，第二个轴表示行方向。

我们使用 numpy 的 [**numpy.amax()**](https://www.geeksforgeeks.org/numpy-amax-python/) 和 [**numpy.amin()**](https://www.geeksforgeeks.org/numpy-amin-python/) 函数分别得到数组沿第二轴的最小值和最大值。

**numpy.amax():** 此函数返回数组的最大值或沿轴的最大值(如有提及)。

> **语法:** numpy.amax(a，axis=None，out=None，keepdims= <无值>，初始值= <无值>，其中= <无值>

**numpy.amin():** 此函数返回数组的最小值或沿轴的最小值(如果提到的话)。

> **语法:** numpy.amin(a，axis=None，out=None，keepdims= <无值>，初始值= <无值>，其中= <无值>

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```
# Import numpy library
import numpy as np

# Create a numpy array
arr = np.array([[0, 1],
                [2, 3]])

print("Given Array:\n",
     arr)

# find row-wise max values 
rslt1 = np.amax(arr, 1)
print("\nMaximum Value:",
      rslt1)

# find row-wise min values
rslt2 = np.amin(arr, 1)
print("\nMinimum Value:",
      rslt2)
```

**输出:**

```
Given Array:
[[0 1]
[2 3]]

Maximum Value: [1 3]

Minimum Value: [0 2]
```

**例 2:**

## 蟒蛇 3

```
# Import numpy library
import numpy as np

# Create a numpy array
arr = np.array([[10, 34, 45],
                [22, -3, 46], 
                [33, 4, 6]])

print("Given array:\n",
     arr)

# find row-wise max values 
rslt1 = np.amax(arr, 1)
print("\nMaximum value along the second axis:",
      rslt1)

# find row-wise min values 
rslt2 = np.amin(arr, 1)
print("\nMinimum value along the second axis:",
     rslt2)
```

**输出:**

```
Given array:
[[10 34 45]
[22 -3 46]
[33  4  6]]

Maximum value: [45 46 33]

Minimum value: [10 -3  4]
```