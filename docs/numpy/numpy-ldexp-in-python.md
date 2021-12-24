# python 中的 numpy . ldexp()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ldxp-in-python/

在 Python 中，numpy.ldexp(arr1，arr2[，out])函数按元素返回 arr1 * (2**arr2)。这也称为 numpy.frexp()函数的逆函数。

> **语法:** numpy.ldexp()
> **参数:**
> **arr 1:**【Array _ like】乘数数组。
> **arr 2:**【Array _ like，int】两个指数的数组。
> **出:**【n 数组，可选】输出结果数组。
> **返回:**【n 数组，标量】返回 arr1 * (2**arr2)的结果。如果 arr1 和 arr2 都是标量，这就是标量。

**代码#1:**

## 蟒蛇 3

```
# Python program explaining
# numpy.ldexp() method

# importing numpy 
import numpy as geek

# ldexp() Function on + ve nd -ve Numbers
print(geek.ldexp(6, geek.arange(4)))
print(geek.ldexp(-8, geek.arange(4)))

# ldexp() Function on fractional Number
print(geek.ldexp(5.2, geek.arange(3)))
print(geek.ldexp(-3.2, geek.arange(3)))
```

**Output:** 

```
[  6\.  12\.  24\.  48.]
[ -8\. -16\. -32\. -64.]
[  5.2  10.4  20.8]
[ -3.2  -6.4 -12.8]
```

**代码#2:** 不支持复杂的数据类型，它们会引发**类型错误。**

## 蟒蛇 3

```
# Python program explaining
# numpy.ldexp() method

# importing numpy
import numpy as geek

# ldexp() Function on complex dtypes
print(geek.ldexp(-5 + 9J, geek.arange(4)))
```

**Output:** 

```
 TypeError: ufunc 'ldexp' not supported for the input types
```