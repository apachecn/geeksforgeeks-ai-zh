# 计算给定 NumPy 阵列沿第二轴的最大值和最小值之差

> 原文:[https://www . geeksforgeeks . org/沿第二轴计算给定 numpy 数组的最大值和最小值之差/](https://www.geeksforgeeks.org/calculate-the-difference-between-the-maximum-and-the-minimum-values-of-a-given-numpy-array-along-the-second-axis/)

让我们看看如何沿着第二个轴计算给定 NumPy 数组的最大值和最小值之间的差值。这里，第二个轴表示行方向。

所以首先为了找到 numpy 数组中的最大和最小元素，我们分别使用了 NumPy 库的[**【NumPy . amax()】**](https://www.geeksforgeeks.org/numpy-amax-python/)和 [**numpy.amin()**](https://www.geeksforgeeks.org/numpy-amin-python/) 函数。然后我们简单地对它进行减法运算。

**numpy.amax():** 此函数返回数组的最大值或沿轴的最大值(如有提及)。

> **语法:** numpy.amax(arr，axis = None，out = None，keepdims =)

**numpy.amin():** 此函数返回数组的最小值或沿轴的最小值(如果提到的话)。

> **语法:** numpy.amin(arr，axis = None，out = None，keepdims =)

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```
# import library
import numpy as np

# create a numpy 2d-array
x = np.array([[100, 20, 305],
             [ 200, 40, 300]])

print("given array:\n", x)

# get maximum element row
# wise from numpy array
max1 = np.amax(x ,1)

# get minimum element row
# wise from numpy array
min1 = np.amin(x, 1)

# print the row-wise max 
# and min difference
print("difference:\n", max1 - min1)
```

**输出:**

```
given array:
 [[100  20 305]
 [200  40 300]]
difference:
 [285 260]
```

**例 2:**

## 蟒蛇 3

```
# import library
import numpy as np

# list
x = [12, 13, 14, 15, 16]
y = [17, 18, 19, 20, 21]

# create a numpy 2d-array
array = np.array([x, y]).reshape((2, 5))

print("original array:\n", array)

# find max and min elements
# row-wise
max1, min1 = np.amax(array, 1), np.amin(array,1)

# print the row-wise max 
# and min difference
print("Difference:\n", max1 - min1)
```

**输出:**

```
original array:
 [[12 13 14 15 16]
 [17 18 19 20 21]]
Difference:
 [4 4]
```