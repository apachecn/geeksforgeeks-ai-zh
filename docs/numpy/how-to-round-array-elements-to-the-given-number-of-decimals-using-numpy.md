# 如何使用 NumPy 将数组元素舍入到给定的小数位数？

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-round-array-elements-to-the-given-number-of-decimals-using-numpy/) 将数组元素舍入到给定的小数位数

在 NumPy 中，我们可以借助 round()将数组元素舍入到给定的小数位数。

**语法:**

```py
np.round(a, decimals=0, out=None)
```

第一个参数是一个数组，第二个参数是需要舍入的小数位数。如果没有参数作为第二个参数传递，默认情况下取 0。它将把数组元素舍入到给定的小数位数。

**例 1:**

## 蟒蛇 3

```py
import numpy as np

# perform the numpy.round
rounded_array = np.round([1.5, 1.53, 1.23, 3.89])

# print the rounded_array
print(rounded_array)
```

**输出**

```py
[2\. 2\. 1\. 4.]

```

**例 2:**

## 蟒蛇 3

```py
import numpy as np

# perform the numpy.round
rounded_array = np.round([1.5, 1.53, 1.23, 3.89], 
                         decimals=1)

# print the rounded_array
print(rounded_array)
```

**输出:**

```py
[1.5 1.5 1.2 3.9]

```

**例**

## 蟒蛇 3

```py
import numpy as np

# perform the numpy.round
rounded_array = np.round(
    [1.534, 1.5389, 1.2301, 3.89903, 6.987, 4.09], decimals=2)

# print the rounded_array
print(rounded_array)
```

**输出:**

```py
[1.53 1.54 1.23 3.9  6.99 4.09]

```