# 计算给定 NumPy 数组的加权平均值

> 原文:[https://www . geeksforgeeks . org/计算给定 numpy 数组的加权平均值/](https://www.geeksforgeeks.org/compute-the-weighted-average-of-a-given-numpy-array/)

在 NumPy 中，我们可以通过两种方法计算给定数组的权重:第一种方法是借助 numpy.average()函数，在该函数中，我们将权重数组传递给参数。第二种方法是通过数学计算，首先将权重数组的和除以权重数组，然后乘以给定的数组，计算该数组的和。

**方法 1:** 使用 numpy.average()方法

**例 1:**

## 计算机编程语言

```
import numpy as np

# Original array
array = np.arange(5)
print(array)

weights = np.arange(10, 15)
print(weights)

# Weighted average of the given array
res1 = np.average(array, weights=weights)
print(res1)
```

**输出:**

```
[0 1 2 3 4]
[10 11 12 13 14]
2.1666666666666665

```

**例 2:**

## 计算机编程语言

```
import numpy as np

# Original array
array = np.arange(2, 7)
print(array)

weights = np.arange(2, 7)
print(weights)

# Weighted average of the given array
res1 = np.average(array, weights=weights)
print(res1)
```

**输出:**

```
[2 3 4 5 6]
[2 3 4 5 6]
4.5

```

**方法二:**运用数学运算

**例 1:**

## 计算机编程语言

```
import numpy as np

# Original array
array = np.arange(2, 7)
print(array)

weights = np.arange(2, 7)
print(weights)

# Weighted average of the given array
res2 = (array*(weights/weights.sum())).sum()
print(res2)
```

**输出:**

```
[2 3 4 5 6]
[2 3 4 5 6]
4.5

```

**例 2:**

## 计算机编程语言

```
import numpy as np

# Original array
array = np.arange(5)
print(array)

weights = np.arange(10, 15)
print(weights)

# Weighted average of the given array
res2 = (array*(weights/weights.sum())).sum()
print(res2)
```

**输出:**

```
[0 1 2 3 4]
[10 11 12 13 14]
2.166666666666667

```