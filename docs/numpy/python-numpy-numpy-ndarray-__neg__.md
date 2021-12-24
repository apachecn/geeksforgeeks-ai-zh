# python | num py . ndaarray . _ _ _ neg _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ neg _/

借助 **Numpy** 的 **numpy.ndarray.__neg__()** 方法，可以将数组中的每个元素乘以-1。因此，具有像**正值这样的值的结果数组变成负的**和**负值变成正的**。

> **语法:**n 数组。__neg__($self，/)
> 
> **返回:**-自我

**例#1 :**
在这个例子中我们可以看到，应用`numpy.__neg__()`后，我们得到了一个数组中正负值组合的简单数组。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, -2, 3, 4, 5, 6])

# applying numpy.__neg__() method
print(gfg.__neg__())
```

**Output:**

```py
[-1  2 -3 -4 -5 -6]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, -3, 4, 5, 6],
                [-6, 5, 4, 3, 2, -1]])

# applying numpy.__neg__() method
print(gfg.__neg__())
```

**Output:**

```py
[[-1 -2  3 -4 -5 -6]
 [ 6 -5 -4 -3 -2  1]]

```