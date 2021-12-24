# 计算扁平 NumPy 阵列的中间值

> 原文:[https://www . geeksforgeeks . org/计算扁平 numpy 阵列的中值/](https://www.geeksforgeeks.org/compute-the-median-of-the-flattened-numpy-array/)

在本文中，我们将讨论如何计算扁平数组的中值。[中值](https://www.geeksforgeeks.org/median/)基本上是将数组的下半部分与数组的上半部分分开的值。

**示例:**

> 如果数组中有奇数。
> A = [1，2，3，4，5，6，7]
> 那么中值元素将是 7+1/2=数组的第 4 个元素。
> 因此这个数组的中位数是 4。
> 
> 如果一个数组中有偶数
> A = [1，2，3，4，5，6，7，8]
> 那么中间元素将是两个中间元素的平均值。
> 这里是数组第 4 和第 5 个元素的平均值，即 4+1/2 =4.5。

可以使用 Python 中的 [numpy.median()](https://www.geeksforgeeks.org/numpy-median-in-python/) 函数计算。该函数计算沿着指定轴的给定数据(数组元素)的中值。

**语法:**

```
numpy.median(arr, axis = None)
```

**示例 1:** 奇数个元素

## 蟒蛇 3

```
# importing numpy as library
import numpy as np

# creating 1 D array with odd no of 
# elements
x_odd = np.array([1, 2, 3, 4, 5, 6, 7])
print("\nPrinting the Original array:")
print(x_odd)

# calculating median
med_odd = np.median(x_odd)
print("\nMedian of the array that contains \
odd no of elements:")
print(med_odd)
```

**输出:**

```
Printing the Original array:
[1 2 3 4 5 6 7]

Median of the array that contains odd no of elements:
4.0

```

**例 2:** 甚至没有元素:

## 蟒蛇 3

```
# importing numpy as library
import numpy as np

# creating 1 D array with even no of 
# elements
x_even = np.array([1, 2, 3, 4, 5, 6, 7, 8])
print("\nPrinting the Original array:")
print(x_even)

# calculating median
med_even = np.median(x_even)
print("\nMedian of the array that contains \
even no of elements:")
print(med_even)
```

**输出:**

```
Printing the Original array:
[1 2 3 4 5 6 7 8]

Median of the array that contains even no of elements:
4.5

```