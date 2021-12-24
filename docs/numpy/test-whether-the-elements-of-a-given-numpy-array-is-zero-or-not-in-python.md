# 测试 Python 中给定 NumPy 数组的元素是否为零

> 原文:[https://www . geeksforgeeks . org/test-给定 numpy 数组的元素在 python 中是否为零/](https://www.geeksforgeeks.org/test-whether-the-elements-of-a-given-numpy-array-is-zero-or-not-in-python/)

在 numpy 中，我们可以借助 [**numpy.all()**](https://www.geeksforgeeks.org/numpy-all-in-python/) 函数检查给定数组的元素是否为零。在这个函数中，传递一个数组作为参数。如果传递的数组中的任何一个元素为零，则返回假，否则返回真布尔值。

> **语法:** numpy.all()
> 
> **参数:**一个数组
> 
> **返回:**一个布尔值(真或假 **)**

让我们看看例子:

**例 1:**

## 计算机编程语言

```py
# import numpy library
import numpy as np

# create an array
x = np.array([34, 56, 89,
              23, 69, 980,
              567])

# print array
print(x)

# Test if none of the elements 
# of the said array is zero
print(np.all(x))
```

**输出:**

```py
[34,56,89,23,69,980,567]
True

```

**例 2:**

## 计算机编程语言

```py
# import numpy library
import numpy as np

# create an array
x = np.array([1, 2, 3,
              4, 6, 7,
              8, 9, 10,
              0, 89, 67])

# print array
print(x)

# Test if none of the elements
# of the said array is zero
print(np.all(x))
```

**输出:**

```py
False

```