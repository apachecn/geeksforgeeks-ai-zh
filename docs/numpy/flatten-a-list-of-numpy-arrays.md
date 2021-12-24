# 展平 NumPy 阵列列表

> 原文:[https://www . geeksforgeeks . org/flat-a-list-numpy-arrays/](https://www.geeksforgeeks.org/flatten-a-list-of-numpy-arrays/)

先决条件[Python 中 Flatten()和 Ravel() Numpy 函数](Differences between Flatten() and Ravel() Numpy Functions)、 [numpy.ravel()的区别](https://www.geeksforgeeks.org/numpy-ravel-python/)，

在本文中，我们将看到如何展平 numpy 数组列表。 **NumPy** 是 Python 编程语言的一个库，增加了对大型、多维数组和矩阵的支持，以及大量对这些数组进行操作的高级数学函数。

展平 NumPy 数组列表意味着将多维 NumPy 数组组合成单个数组或列表，如下例所示

> **numpy 数组列表:**
> 【数组([[ 0.00353654]])，
> 数组([[ 0.00353654]])，
> 数组([[ 0.00353654]])，
> 数组([[ 0.00353654]])，
> 数组([[ 0.00353654]])，
> 数组([[0.003554
> 
> **展平 numpy 数组:**
> 数组(【0.00353654，0.00353654，0.00353654，0.00353654，0.00353654，
> 0.00353654，0.00353654，0.00353654，0.00353654

**方法 1**
使用 numpy 的连接方法

## 蟒蛇 3

```py
# importing numpy as np
import numpy as np

# list of numpy array
list_array = [np.array([[1]]),
               np.array([[2]]),
               np.array([[3]]),
               np.array([[4]]),
               np.array([[5]]),
               np.array([[6]]),
               np.array([[7]]),
               np.array([[8]]),
               np.array([[9]]),
               np.array([[10]]),
               np.array([[11]]),
               np.array([[12]]),
               np.array([[13]]),
               np.array([[14]]),
               np.array([[15]]),
               np.array([[16]])]

# concatenating all the numpy array
flatten = np.concatenate(list_array)

# printing the ravel flatten array
print(flatten.ravel())
```

**输出:**

```py
[ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
```

**方法 2**
使用 numpy 的展平方法

## 蟒蛇 3

```py
# importing numpy as np
import numpy as np

# list of numpy array
list_array = [np.array([[1]]),
               np.array([[2]]),
               np.array([[3]]),
               np.array([[4]]),
               np.array([[5]]),
               np.array([[6]]),
               np.array([[7]]),
               np.array([[8]]),
               np.array([[9]]),
               np.array([[10]]),
               np.array([[11]]),
               np.array([[12]]),
               np.array([[13]]),
               np.array([[14]]),
               np.array([[15]]),
               np.array([[16]])]

# flatten the numpy array
flatten = np.array(list_array).flatten()

# printing the flatten array
print(flatten)
```

**输出:**

```py
[ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
```

**方法 3**
使用纽姆皮的拉威尔法

## 蟒蛇 3

```py
# importing numpy as np
import numpy as np

# list of numpy array
list_array = [np.array([[1]]),
               np.array([[2]]),
               np.array([[3]]),
               np.array([[4]]),
               np.array([[5]]),
               np.array([[6]]),
               np.array([[7]]),
               np.array([[8]]),
               np.array([[9]]),
               np.array([[10]]),
               np.array([[11]]),
               np.array([[12]]),
               np.array([[13]]),
               np.array([[14]]),
               np.array([[15]]),
               np.array([[16]])]

# flatten the numpy array using ravel method
flatten = np.array(list_array).ravel()

# printing the flatten array
print(flatten)
```

**输出:**

```py
[ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
```

**方法 4**
使用 numpy 的重塑方法

## 蟒蛇 3

```py
# importing numpy as np
import numpy as np

# list of numpy array
list_array = [np.array([[1]]),
               np.array([[2]]),
               np.array([[3]]),
               np.array([[4]]),
               np.array([[5]]),
               np.array([[6]]),
               np.array([[7]]),
               np.array([[8]]),
               np.array([[9]]),
               np.array([[10]]),
               np.array([[11]]),
               np.array([[12]]),
               np.array([[13]]),
               np.array([[14]]),
               np.array([[15]]),
               np.array([[16]])]

# flatten the numpy array using reshape method
flatten = np.array(list_array).reshape(-1)

# printing the flatten array
print(flatten)
```

**输出:**

```py
[ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
```