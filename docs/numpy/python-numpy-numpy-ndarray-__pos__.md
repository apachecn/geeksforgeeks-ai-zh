# python | num py . ndaarray . _ _ _ pos _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ pos _/

借助 **Numpy** 的 **numpy.ndarray.__pos__()** 方法，可以将数组中的每个元素乘以 1。因此，结果数组的值**与原始数组的值**相同。

> **语法:**n 数组。__pos__($self，/)
> 
> **返回:**+自我

**示例#1 :**
在这个示例中我们可以看到，应用`numpy.__pos__()`后，我们得到了可以和原来一样的简单数组。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, -2, 3, 4, 5, 6])

# applying numpy.__pos__() method
print(gfg.__pos__())
```

**Output:**

```py
[ 1 -2  3  4  5  6]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, -3, 4, 5, 6],
                [-6, 5, 4, 3, 2, -1]])

# applying numpy.__pos__() method
print(gfg.__pos__())
```

**Output:**

```py
[[ 1  2 -3  4  5  6]
 [-6  5  4  3  2 -1]]

```