# python | num py . ndaarray . _ _ _ add _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ add _/

借助`**Numpy numpy.ndarray.__add__()**`，我们可以添加一个特定的值，该值在`ndarray.__add__()`方法中作为参数提供。值将被添加到 **numpy 数组**中的每个元素。

> **语法:**n 数组。__add__($self，value，/)
> 
> **返回:**自身+值

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都添加了方法`ndarray.__add__()`中作为参数给出的值。记住一件事，它不会为双**类型值工作。**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__add__() method
print(gfg.__add__(5))
```

**Output:**

```
[ 6  7  8  9  10]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__add__() method
print(gfg.__add__(5))
```

**Output:**

```
[[ 6  7  8  9  10]
 [11  10  9  8  7]]

```