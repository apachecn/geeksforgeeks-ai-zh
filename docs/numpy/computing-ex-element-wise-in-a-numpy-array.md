# 在 NumPy 数组中逐元素计算 e^x

> 原文:[https://www . geeksforgeeks . org/computing-ex-element-wise-in-a-numpy-array/](https://www.geeksforgeeks.org/computing-ex-element-wise-in-a-numpy-array/)

在本文中，我们将讨论如何计算 NumPy 数组中每个元素的 e^x。

**示例:**

```py
Input : [1, 3, 5, 7]
Output : [2.7182817, 20.085537, 148.41316, 1096.6332]

Explanation :
e^1 = 2.7182817
e^3 = 20.085537
e^5 = 148.41316
e^7 = 1096.6332

```

我们将使用 [numpy.exp()](https://www.geeksforgeeks.org/numpy-exp-python/) 方法来计算指数值。

**例 1 :**

```py
# importing the module
import numpy as np

# creating an array
arr = np.array([1, 3, 5, 7])
print("Original array: ")
print(arr)

# converting array elements into e ^ x
res = np.exp(arr)
print("\nPrinting e ^ x, element-wise of the said:")
print(res)
```

**输出:**

```py
Original array: 
[1 3 5 7]

Printing e ^ x, element-wise of the said:
[   2.71828183   20.08553692  148.4131591  1096.63315843]

```

**例 2 :** 我们也可以用 [math.exp()](https://www.geeksforgeeks.org/python-math-library-exp-method/) 方法求指数。虽然不会一次占用整个 NumPy 数组，但是我们必须一次传递一个元素。

```py
# importing the module
import numpy as np
import math

# creating an array
arr = np.array([1, 3, 5, 7])
print("Original array: ")
print(arr)

# converting array elements into e ^ x
res = []
for element in arr:
    res.append(math.exp(element))
print("\nPrinting e ^ x, element-wise of the said:")
print(res)
```

**输出:**

```py
Original array: 
[1 3 5 7]

Printing e ^ x, element-wise of the said:
[2.718281828459045, 20.085536923187668, 148.4131591025766, 1096.6331584284585]

```