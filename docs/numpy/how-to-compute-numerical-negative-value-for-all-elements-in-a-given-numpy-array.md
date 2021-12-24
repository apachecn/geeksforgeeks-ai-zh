# 如何计算给定 NumPy 数组中所有元素的数值负值？

> 原文:[https://www . geesforgeks . org/如何计算给定 numpy 数组中所有元素的数值负值/](https://www.geeksforgeeks.org/how-to-compute-numerical-negative-value-for-all-elements-in-a-given-numpy-array/)

在本文中，我们将看到如何计算给定 NumPy 数组中所有元素的负值。所以，负值实际上是加到任何一个数上就变成 0 的数。

**示例:**

如果我们把一个数当作 4，那么-4 就是它的负数，因为当我们把-4 加到 4 时，我们得到的和是 0。现在让我们再举一个例子，假设我们取一个数字-6，当我们加上+6 时，总和为零。因此+6 是-6 的负值。现在假设我们有一组数字:

```
A = [1,2,3,-1,-2,-3,0]
So, the negative value of A is 
A'=[-1,-2,-3,1,2,3,0].
```

所以，要求一个元素的数值负值，就要用到 numpy 库的 [**numpy.negative()**](https://www.geeksforgeeks.org/numpy-negative-in-python/) 函数。

> **语法:** numpy.negative(arr，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，subok=True[，signature，extobj]，ufunc 'negative ')
> 
> **返回:**【数组或标量】返回的数组或标量= -(输入 arr 或标量)

现在，让我们看看例子:

**例 1:**

## 蟒蛇 3

```
# importing library
import numpy as np

# creating a array
x = np.array([-1, -2, -3,
              1, 2, 3, 0])

print("Printing the Original array:",
      x)

# converting array elements to
# its corresponding negative value
r1 = np.negative(x)

print("Printing the negative value of the given array:",
      r1)
```

**输出:**

```
Printing the Original array: [-1 -2 -3  1  2  3  0] 
Printing the negative value of the given array: [ 1  2  3 -1 -2 -3  0] 

```

**例 2:**

## 蟒蛇 3

```
# importing library
import numpy as np

# creating a numpy 2D array
x = np.array([[1, 2],
              [2, 3]])

print("Printing the Original array Content:\n",
      x)

# converting array elements to
# its corresponding negative value
r1 = np.negative(x)

print("Printing the negative value of the given array:\n",
      r1)
```

**输出:**

```
Printing the Original array Content:
[[1 2]
[2 3]]
Printing the negative value of the given array:
[[-1 -2]
[-2 -3]]
```