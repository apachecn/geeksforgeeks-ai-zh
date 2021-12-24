# python | num py . ndaarray . _ _ _ true div _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray _ _ _ _ true div _/

借助`**Numpy numpy.ndarray.__truediv__()**`，我们可以划分一个特定的值，该值在`ndarray.__truediv__()`方法中作为参数提供。值将被分配给 **numpy 数组**中的每个元素。

> **语法:**n 数组。__truediv__($self，value，/)
> 
> **返回:**自我/价值

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用方法`ndarray.__truediv__()`中作为参数给出的值进行了划分。此方法对于数组的正、负和浮点值都很有效。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2.5, 3, 4.8, 5])

# applying ndarray.__truediv__() method
print(gfg.__truediv__(2))
```

**Output:**

```
[ 0.5   1.25  1.5   2.4   2.5 ]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4.45, 5],
                [6, 5.5, 4, 3, 2.62]])

# applying ndarray.__truediv__() method
print(gfg.__truediv__(3))
```

**Output:**

```
[[ 0.33333333  0.66666667  1\.          1.48333333  1.66666667]
 [ 2\.          1.83333333  1.33333333  1\.          0.87333333]]

```