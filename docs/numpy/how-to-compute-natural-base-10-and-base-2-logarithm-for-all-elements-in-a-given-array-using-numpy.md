# 如何用 NumPy 计算给定数组中所有元素的自然对数、以 10 为底对数和以 2 为底对数？

> 原文:[https://www . geesforgeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-compute-natural-base-10-and-base-2-logarithm-for-all-elements-in-a-given-array-using-numpy/) 计算给定数组中所有元素的自然底数 10 和底数 2 对数

[numpy . log()](https://www.geeksforgeeks.org/numpy-log-python/)Python 中的函数返回输入的自然对数，其中一个数的自然对数是其对数学常数 e 的底的对数，其中 e 是约等于 2.718281828459 的无理数和超越数。

> **语法:** numpy.log(arr，out)
> 
> **参数:**
> **arr :** 输入值。也可以是标量和 numpy ndim 数组。
> **出:**存储结果的位置。如果提供，它必须具有
> 输入广播到的形状。如果未提供或无，则返回新分配的数组。
> 形状必须与输入数组相同。

如果将标量作为输入提供给函数，则函数将应用于标量，并返回一个标量。

**示例:**如果给出 3 作为输入，那么日志(3)将作为输出返回。

## 蟒蛇 3

```
import numpy

n = 3
print("natural logarithm of {} is".format(n), numpy.log(n))

n = 5
print("natural logarithm of {} is".format(n), numpy.log(n))
```

**输出:**

```
natural logarithm of 3 is 1.0986122886681098
natural logarithm of 5 is 1.6094379124341003

```

如果输入是 n-dim 数组，则按元素应用函数。ex- np.log([1，2，3])相当于[np.log(1)，np.log(2)，np.log(3)]

**示例:**

## 蟒蛇 3

```
import numpy

arr = np.array([6, 2, 3, 4, 5])
print(numpy.log(arr))
```

**输出:**

```
[1.79175947 0.69314718 1.09861229 1.38629436 1.60943791]

```

类似 numpy.log()的函数:

*   [**numpy . log2()**](https://www.geeksforgeeks.org/numpy-log2-python/)T4:计算基数 2 的对数。此函数的参数与 numpy.log()相同。它也被称为二进制对数。y 的以 2 为底的对数是数字 2 的幂，要得到 y 的值，必须将数字 2 加 1。
*   [**numpy.log10()**](https://www.geeksforgeeks.org/numpy-log10-python/) :计算基数 10 个对数。参数与 numpy.log()相同。y 的以 10 为底的对数是数字 10 的幂，要得到 y 的值，必须将它加 1。

**示例:**

## 计算机编程语言

```
# importing numpy
import numpy

# natural logarithm
print("natural logarithm -")
arr = numpy.array([6, 2, 3, 4, 5])
print(numpy.log(arr))

# Base 2 logarithm
print("Base 2 logarithm -")
arr = numpy.array([6, 2, 3, 4, 5])
print(numpy.log2(arr))

# Base 10 logarithm
print("Base 10 logarithm -")
arr = numpy.array([6, 2, 3, 4, 5])
print(numpy.log10(arr))
```

**输出:**

```
natural logarithm -
[1.79175947 0.69314718 1.09861229 1.38629436 1.60943791]
Base 2 logarithm -
[2.5849625  1\.         1.5849625  2\.         2.32192809]
Base 10 logarithm -
[0.77815125 0.30103    0.47712125 0.60205999 0.69897   ]

```