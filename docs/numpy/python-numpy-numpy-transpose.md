# python | num py . transponte()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py 转发器/

借助 **Numpy numpy .转置()**，我们可以利用 Numpy 的`**numpy.transpose()**`方法，实现一行内转置的简单功能。它可以转置二维数组，但对一维数组没有影响。这个方法转置二维数组。

> **参数:**
> **轴:**【无、整数元组或 n 整数】如果有人想传递参数，那么你可以，但这并不是全部必需的。但要想比记得只通过 **(0，1)** 或 **(1，0)** 。就像我们有一个形状数组(2，3)来改变它(3，2)，你应该传递(1，0)，其中 1 是 3，0 是 2。
> 
> **返回:**正常

**示例#1 :**
在这个示例中，我们可以看到只用一行就可以很容易地转置一个数组。

```
# importing python module named numpy
import numpy as np

# making a 3x3 array
gfg = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

# before transpose
print(gfg, end ='\n\n')

# after transpose
print(gfg.transpose())
```

**Output:**

```
[[1 2 3]
 [4 5 6]
 [7 8 9]]

[[1 4 7]
 [2 5 8]
 [3 6 9]]

```

**示例 2 :**
在本例中，我们演示了在`numpy.transpose()`中使用元组。

```
# importing python module named numpy
import numpy as np

# making a 3x3 array
gfg = np.array([[1, 2],
                [4, 5],
                [7, 8]])

# before transpose
print(gfg, end ='\n\n')

# after transpose
print(gfg.transpose(1, 0))
```

**Output:**

```
[[1 2]
 [4 5]
 [7 8]]

[[1 4 7]
 [2 5 8]]

```