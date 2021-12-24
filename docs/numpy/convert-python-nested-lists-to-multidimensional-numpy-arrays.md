# 将 Python 嵌套列表转换为多维 NumPy 数组

> 原文:[https://www . geesforgeks . org/convert-python-nested-list-to-多维-numpy-arrays/](https://www.geeksforgeeks.org/convert-python-nested-lists-to-multidimensional-numpy-arrays/)

**先决条件:** [Python 列表](https://www.geeksforgeeks.org/python-list/)[Numpy ndarray](https://www.geeksforgeeks.org/numpy-ndarray/)

列表和 NumPy 数组都是可相互转换的。由于 NumPy 是一个用于执行数学运算的快速(高性能)Python 库，因此最好使用 NumPy 数组，而不是嵌套列表。

**方法 1:** 使用 **numpy.array()。**

**进场:**

*   导入 numpy 包。
*   初始化嵌套列表，然后使用 numpy.array()函数将列表转换为数组，并将其存储在不同的对象中。
*   显示列表和 NumPy 数组，并观察其区别。

下面是实现。

## 蟒蛇 3

```py
# importing numpy library
import numpy

# initializing list
ls = [[1, 7, 0],
       [ 6, 2, 5]]

# converting list to array
ar = numpy.array(ls)

# displaying list
print ( ls)

# displaying array
print ( ar)
```

**输出:**

```py
[[1, 7, 0], [6, 2, 5]]
[[1 7 0]
 [6 2 5]]
```

**方法 2:** 使用**纽姆皮·阿萨雷()。**

**进场:**

*   导入 numpy 包。
*   初始化嵌套的 4 维列表，然后使用 numpy.asarray()函数将列表转换为数组，并将其存储在不同的对象中。
*   显示列表和 NumPy 数组，并观察其区别。

下面是实现。

## 蟒蛇 3

```py
# importing numpy library
import numpy

# initializing list
ls = [[1, 7, 0],[ 6, 2, 5],[ 7, 8, 9],[ 41, 10, 20]]

# converting list to array
ar = numpy.asarray(ls)

# displaying list
print ( ls)

# displaying array
print ( ar)
```

**输出:**

```py
[[1, 7, 0], [6, 2, 5], [7, 8, 9], [41, 10, 20]]
[[ 1  7  0]
 [ 6  2  5]
 [ 7  8  9]
 [41 10 20]]
```