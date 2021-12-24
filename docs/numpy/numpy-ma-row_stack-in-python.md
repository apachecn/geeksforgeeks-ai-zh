# Python 中的 numpy.ma.row_stack()

> 原文:[https://www.geeksforgeeks.org/numpy-ma-row_stack-in-python/](https://www.geeksforgeeks.org/numpy-ma-row_stack-in-python/)

**numpy.ma.row_stack() :** 此函数有助于以垂直方式按顺序逐行堆叠数组。

**参数:**

> **tup:**ndarrays 序列。1D 阵列必须具有相同的长度，阵列必须沿着所有轴具有相同的形状。

**结果:**

```
Row-wise stacked arrays
```

**代码#1:** 解释 row_stack()

```
# importing libraries
import numpy as np

# row_stacking array
a = np.array([1, 2, 3])
arr = np.ma.row_stack (a)

print ("arr : \n", arr)

# row_stacking array
b = np.array([[1], [2], [3]])
arr1 = np.ma.row_stack (b)

print ("\narr1 : \n", arr1)
```

**输出:**

```
arr : 
 [[1]
 [2]
 [3]]

arr1 : 
 [[1]
 [2]
 [3]]

```

**代码#2:** 使用 row_stack()生成错误

```
# importing libraries
import numpy as np

# row_stacking array

b = np.array([[1, 1], [2], [3]])
arr1 = np.ma.row_stack (b)

print ("\narr1 : \n", arr1)
```

**输出:**

> <font color="red">值错误:</font>除连接轴外，所有输入数组维度必须完全匹配。