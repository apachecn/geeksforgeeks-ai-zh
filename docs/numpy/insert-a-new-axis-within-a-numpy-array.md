# 在 NumPy 数组中插入一个新轴

> 原文:[https://www . geeksforgeeks . org/insert-a-new-axis-in-a-numpy-array/](https://www.geeksforgeeks.org/insert-a-new-axis-within-a-numpy-array/)

这篇文章讨论了在 NumPy 中增加数组维数的方法。NumPy 为我们提供了两种不同的内置函数来增加数组的维数，即

```
1D array will become 2D array
2D array will become 3D array
3D array will become 4D array
4D array will become 5D array

```

**方法一:使用 numpy.newaxis()**
第一种方法是使用 numpy.newaxis 对象。此对象相当于在声明数组时使用无作为参数。诀窍是在要添加新轴的索引位置使用 numpy.newaxis 对象作为参数。
**例:**

## 蟒蛇 3

```
import numpy as np

arr = np.arange(5*5).reshape(5, 5)
print(arr.shape)

# promoting 2D array to a 5D array
# arr[None, ..., None, None]
arr_5D = arr[np.newaxis, ..., np.newaxis, np.newaxis]

print(arr_5D.shape)
```