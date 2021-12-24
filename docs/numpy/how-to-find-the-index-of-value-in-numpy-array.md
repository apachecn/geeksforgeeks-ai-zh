# 如何找到 Numpy 数组中值的索引？

> 原文:[https://www . geeksforgeeks . org/如何找到 numpy 数组中的值索引/](https://www.geeksforgeeks.org/how-to-find-the-index-of-value-in-numpy-array/)

在本文中，我们将找到 NumPy 数组中元素的索引。 [**(其中)**](https://www.geeksforgeeks.org/numpy-where-in-python/) 方法用于指定条件中指定的特定元素的索引。

**语法:**

> numpy.where(条件)
> 
> 这里，条件是指定的条件。

**例 1:**

在这个程序中，我们将使用 NumPy 创建一个数组并显示它。

我们可以使用以下语法用 numpy 创建一个数组:

```py
numpy.array([value1,value2,value3,.....,value n])
```

## 蟒蛇 3

```py
# import numpy package
import numpy as np

# create an numpy array with 1 
# to 10 elements
a = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

print(a)
```

**输出:**

```py
[ 1  2  3  4  5  6  7  8  9 10]
```

找到 3 的索引

## 蟒蛇 3

```py
# display index value
# of 3
print(np.where(a == 3))
```