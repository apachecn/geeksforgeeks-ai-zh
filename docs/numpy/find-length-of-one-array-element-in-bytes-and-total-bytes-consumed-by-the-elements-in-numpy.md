# 找出一个数组元素的长度(以字节为单位)和 Numpy 中元素消耗的总字节数

> 原文:[https://www . geeksforgeeks . org/find-每字节一个数组元素的长度和每字节元素消耗的总字节数/](https://www.geeksforgeeks.org/find-length-of-one-array-element-in-bytes-and-total-bytes-consumed-by-the-elements-in-numpy/)

在 NumPy 中，我们可以借助 **itemsize 找到一个字节中一个数组元素的长度。**返回整数形式的数组长度。并在 numpy 中借助 **nbytes 计算元素消耗的总字节数。**

> **语法:**数组.项目大小
> 
> **Return :** 它将以字节为单位返回数组的长度(int)。

> **语法:** array.nbytes
> 
> **返回:**它将返回元素消耗的总字节数。

**例 1:**

## 计算机编程语言

```
import numpy as np

array = np.array([1,3,5], dtype=np.float64)

# Size of the array
print(array.size)

# Length of one array element in bytes,
print( array.itemsize)

# Total bytes consumed by the elements
# of the array
print(array.nbytes)
```

**输出:**

```
3
8
24
```

**例 2:**

## 计算机编程语言

```
import numpy as np

array = np.array([20, 34, 56, 78, 1, 9], dtype=np.float64)

# Size of the array
print(array.size)

# Length of one array element in bytes,
print(array.itemsize)

# Total bytes consumed by the elements
# of the array
print(array.nbytes)
```

**输出:**

```
6
8
48
```