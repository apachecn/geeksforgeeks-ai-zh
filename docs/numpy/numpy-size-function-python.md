# Numpy size()函数| Python

> 原文:[https://www.geeksforgeeks.org/numpy-size-function-python/](https://www.geeksforgeeks.org/numpy-size-function-python/)

在 Python 中，numpy.size()函数计算沿给定轴的元素数量。

> **语法:** numpy.size(arr，axis=None)
> **参数:**
> **arr:**【array _ like】输入数据。
> **轴:**【int，可选】计算元素(行或列)的轴(x，y，z)。默认情况下，给出数组中元素的总数
> **返回:**【int】返回沿给定轴的元素数。

**代码#1 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.size() method

# importing numpy
import numpy as np

# Making a random array
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

# By default, give the total number of elements.
print(np.size(arr))
```

**Output:** 

```py
8
```

**代码#2 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.size() method

# importing numpy
import numpy as np

# Making a random array
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

# count the number of elements along the axis.
# Here rows and columns are being treated
# as elements

#gives no. of rows along x-axis
print(np.size(arr, 0))

#gives no. of columns along y-axis
print(np.size(arr, 1))
```

**Output:** 

```py
2
4
```