# numpy.einsum()方法

> 原文:[https://www.geeksforgeeks.org/numpy-einsum-method/](https://www.geeksforgeeks.org/numpy-einsum-method/)

在 NumPy 中，我们可以借助 **numpy.einsum()找到两个给定多维数组的爱因斯坦求和约定。**我们将传递两个数组作为参数，它将返回爱因斯坦求和约定。

> **语法:**num py . un um()
> 
> **参数:**两个数组。
> 
> **返回:**将返回爱因斯坦求和约定。

**例 1:**

## 计算机编程语言

```
import numpy as np

array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])

# Original 1-d arrays
print(array1)
print(array2)
r = np.einsum("n,n", a, b)

# Einstein’s summation convention of 
# the said arrays
print(r)
```

**输出:**

```
[1 2 3]
[4 5 6]
32

```

**例 2:**

## 计算机编程语言

```
import numpy as np

ar1 = np.arange(9).reshape(3, 3)
ar2 = np.arange(10, 19).reshape(3, 3)

# Original Higher dimension
print(ar1)

print(ar2)
print("")
r = np.einsum("mk,kn", ar1, ar2)

# Einstein’s summation convention of 
# the said arrays
print(r)
```

**输出:**

```
[[0 1 2]
 [3 4 5]
 [6 7 8]]
[[10 11 12]
 [13 14 15]
 [16 17 18]]

[[ 45  48  51]
 [162 174 186]
 [279 300 321]]
```