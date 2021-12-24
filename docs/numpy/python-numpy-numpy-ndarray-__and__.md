# python | num py . ndaarray . _ _ _ 和 __()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ and _/

借助`**Numpy numpy.ndarray.__and__()**`方法，我们可以通过`numpy.ndarray.__and__()`方法中作为参数提供的值，得到**和**元素。

> **语法:**n 数组。__ 和 __($self，value，/)
> 
> **返回:**自我&值

**示例#1 :**
在这个示例中，我们可以看到每个元素都由在`ndarray.__and__()`方法中作为参数传递的值进行 and 运算。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__and__() method
print(gfg.__and__(2))
```

**Output:**

```
[0 2 2 0 0]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__and__() method
print(gfg.__and__(1))
```

**Output:**

```
[[1 0 1 0 1]
 [0 1 0 1 0]]

```