# python | num py . ndaarray . _ _ _ rsift _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray _ _ _ _ rsift _/

借助`**numpy.ndarray.__rshift__()**`方法，我们可以通过`numpy.ndarray.__rshift__()`方法中作为参数提供的值，得到**右移**的元素。

> **语法:**n 数组。__rshift__($self，value，/)
> 
> **返回:**自我>T3】值

**示例#1 :**
在这个示例中，我们可以看到每个元素都向右移动了在`ndarray.__rshift__()`方法中作为参数传递的值。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__rshift__() method
print(gfg.__rshift__(2))
```

**Output:**

```py
[0 0 0 1 1]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__rshift__() method
print(gfg.__rshift__(1))
```

**Output:**

```py
[[0 1 1 2 2]
 [3 2 2 1 1]]

```