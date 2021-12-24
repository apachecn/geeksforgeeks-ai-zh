# python | numpy num py . ndaarray . _ _ _ sub _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ sub _/

在`**Numpy numpy.ndarray.__sub__()**`的帮助下，我们可以减去在`ndarray.__sub__()`方法中作为参数提供的特定值。值将被减去到 **numpy 数组**中的每个元素。

> **语法:**n 数组。__sub__($self，value，/)
> 
> **回归:**自我价值

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都被减去了方法`ndarray.__sub__()`中作为参数给出的值。记住一件事，它不会为双**类型值工作。**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__sub__() method
print(gfg.__sub__(5))
```

**Output:**

```py
[-4 -3 -2 -1  0]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__sub__() method
print(gfg.__sub__(5))
```

**Output:**

```py
[[-4 -3 -2 -1  0]
 [ 1  0 -1 -2 -3]]

```