# 找出两个 NumPy 数组之间的公共值

> 原文:[https://www . geeksforgeeks . org/find-common-values-two-numpy-arrays/](https://www.geeksforgeeks.org/find-common-values-between-two-numpy-arrays/)

在 NumPy 中，我们可以借助 intersect1d()找到两个数组之间的公共值。它将接受参数二数组，并将返回一个数组，其中将出现所有公共元素。

> **语法:**numpy . intersection 1d(array 1，array2)
> 
> **参数:**两个数组。
> 
> **返回:**一个数组，其中所有的公共元素都会出现。

**例 1:**

## 计算机编程语言

```
import numpy as np

ar1 = np.array([0, 1, 2, 3, 4])
ar2 = [1, 3, 4]

# Common values between two arrays
print(np.intersect1d(ar1, ar2))
```

**输出:**

```
[1,3,4]

```

**例 2:**

## 计算机编程语言

```
import numpy as np

ar1 = np.array([12, 14, 15, 16, 17])
ar2 = [2, 4, 5, 6, 7, 8, 9, 12]

# Common values between two arrays
print(np.intersect1d(ar1, ar2))
```

**输出:**

```
[12]

```