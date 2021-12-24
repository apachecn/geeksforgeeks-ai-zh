# Python 中的 numpy.where()

> 原文:[https://www.geeksforgeeks.org/numpy-where-in-python/](https://www.geeksforgeeks.org/numpy-where-in-python/)

**numpy.where()** 函数返回满足给定条件的输入数组中元素的索引。

> **语法:** numpy.where(条件[，x，y])
> **参数:**
> **条件:**当为真时，产生 x，否则产生 y。
> **x，y :** 可供选择的值。x、y 和条件需要可以扩展到某种形状。
> 
> **返回:**
> **out :** 【数组或数组元组】如果同时指定了 x 和 y，则输出数组包含 x 的元素，其中条件为真，而 y 的元素在别处。
> 
> 如果只给定了条件，则返回元组条件非零()，即条件为真的索引。

**代码#1:**

```
# Python program explaining 
# where() function 

import numpy as np

np.where([[True, False], [True, True]],
         [[1, 2], [3, 4]], [[5, 6], [7, 8]])
```

**输出:**

```
array([[1, 6],
       [3, 4]])
```

**代码#2:**

```
# Python program explaining 
# where() function 

import numpy as np

# a is an array of integers.
a = np.array([[1, 2, 3], [4, 5, 6]])

print(a)

print ('Indices of elements <4')

b = np.where(a<4)
print(b)

print("Elements which are <4")
print(a[b])
```

**输出:**

```
[[1 2 3]
 [4 5 6]]

Indices of elements <4
(array([0, 0, 0], dtype=int64), array([0, 1, 2], dtype=int64))

Elements which are <4
array([1, 2, 3])

```