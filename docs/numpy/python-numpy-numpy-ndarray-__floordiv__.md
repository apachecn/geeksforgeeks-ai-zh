# python | numpy num py . ndaarray . _ _ _ flood ev _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ flood rdiv _/t1]

在`**Numpy numpy.ndarray.__floordiv__()**`的帮助下，可以划分一个特定的值，该值在`ndarray.__floordiv__()`方法中作为参数提供。值将被划分到一个 **numpy 数组**中的每一个元素，并且记住它总是在划分之后给出**楼层值**。

> **语法:**n 数组。__floordiv__($self，value，/)
> 
> **返回:** self//value

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用方法`ndarray.__floordiv__()`中作为参数给出的值进行了划分，并给出了数组中被划分的每个元素的 floor 值。此方法对于数组的正、负和浮点值都很有效。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2.5, 3, 4.8, 5])

# applying ndarray.__floordiv__() method
print(gfg.__floordiv__(2))
```

**Output:**

```
[ 0\.  1\.  1\.  2\.  2.]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4.45, 5],
                [6, 5.5, 4, 3, 2.62]])

# applying ndarray.__floordiv__() method
print(gfg.__floordiv__(3))
```

**Output:**

```
[[ 0\.  0\.  1\.  1\.  1.]
 [ 2\.  1\.  1\.  1\.  0.]]

```