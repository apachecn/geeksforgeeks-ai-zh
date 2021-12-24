# python | num py ndaarray。_ _ _ _ _ _ _ _ _ imod _ _(

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ imod _/

在`**Numpy ndarray.__imod__()**`的帮助下，数组中的每一个元素都用二进制运算符进行运算，即 mod(%)。请记住，我们可以在数组中使用任何类型的值，mod 的值在`ndarray.__imod__()`中用作参数。

> **语法:**n 数组。__imod__($self，value，/)
> 
> **返回:**自身% =值

**示例#1 :**
在这个示例中，我们可以看到我们通过`ndarray.__imod__()`方法传递的值用于对数组的每个元素执行 mod 操作。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2.5, 3, 4.8, 5])

# applying ndarray.__imod__() method
print(gfg.__imod__(2))
```

**Output:**

```
[ 1\.   0.5  1\.   0.8  1\. ]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4.45, 5],
                [6, 5.5, 4, 3, 2.62]])

# applying ndarray.__imod__() method
print(gfg.__imod__(3))
```

**Output:**

```
[[ 1\.    2\.    0\.    1.45  2\.  ]
 [ 0\.    2.5   1\.    0\.    2.62]]

```