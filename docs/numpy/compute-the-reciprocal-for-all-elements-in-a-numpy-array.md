# 计算 NumPy 数组中所有元素的倒数

> 原文:[https://www . geeksforgeeks . org/计算 numpy 数组中所有元素的倒数/](https://www.geeksforgeeks.org/compute-the-reciprocal-for-all-elements-in-a-numpy-array/)

在本文中，让我们讨论如何计算给定 NumPy 数组中所有元素的倒数。

**方法 1:** 通过**倒数 _arr = 1/arr** 语句，我们可以将 arr 的每个元素都转换为它的倒数，并保存为倒数 _arr。但是有一个问题，如果“arr”的任何元素为零，您将会遇到一个错误。所以注意不要将任何包含 0 的数组传递给倒数 _arr。

**例 1:**

## 计算机编程语言

```py
# PROGRAM TO FIND RECIPROCAL OF EACH 
# ELEMENT OF NUMPY ARRAY
import numpy as np

lst = [22, 34, 65, 50, 7]
arr = np.array(lst)
reciprocal_arr = 1/arr

print(reciprocal_arr)
```

**输出:**

> [0.04545455 0.02941176 0.01538462 0.02       0.14285714]

**例 2:**

## 计算机编程语言

```py
# PROGRAM TO FIND RECIPROCAL OF EACH
# ELEMENT OF NUMPY ARRAY
import numpy as np

tup = (12, 87, 77, 90, 57, 34)
arr = np.array(tup)
reciprocal_arr = 1/arr

print(reciprocal_arr)
```

**输出:**

> [0.08333333 0.01149425 0.01298701 0.01111111 0.01754386 0.02941176]

**方法 2:** 使用 [numpy .倒数()](https://www.geeksforgeeks.org/numpy-reciprocal-in-python/)方法

Numpy 库还提供了一个简单的方法来寻找数组中每个元素的倒数。倒数()方法可以很容易地用来创建一个新的数组，每个数组包含每个元素的倒数。

**例 1:**

## 蟒蛇 3

```py
#  program to compute the Reciprocal
# for all elements in a given array
# with the help of numpy.reciprocal()
import numpy as np

arr = [2, 1.5, 8, 9, 0.2]
reciprocal_arr = np.reciprocal(arr)

print(reciprocal_arr)
```

**输出:**

> [0.5        0.66666667 0.125      0.11111111 5\.        ]

**例 2:**

## 蟒蛇 3

```py
#  program to compute the Reciprocal for
# all elements in a given array with the
# help of numpy.reciprocal()
import numpy as np

arr = (3, 6.5, 1, 5.9, 8)
reciprocal_arr = np.reciprocal(arr)

print(reciprocal_arr)
```

**输出:**

> [0.33333333 0.15384615 1\.         0.16949153 0.125     ]