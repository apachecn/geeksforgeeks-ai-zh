# python | num py . ndaarray . _ _ _ mod _()

> 哎哎哎::1230【https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ _ _ _ _/中文字幕翻译:http://www . geeksforgeeks . org/python-num py-ndaarray-_ _ _ mod _/

在`**Numpy numpy.ndarray.__mod__()**`的帮助下，数组中的每个元素都被二进制运算符操作，即 **mod(%)** 。请记住，我们可以在数组中使用任何类型的值，mod 的值在`ndarray.__mod__()`中用作参数。

> **语法:**n 数组。__mod__($self，value，/)
> 
> **返回:**自身%值

**示例#1 :**
在这个示例中，我们可以看到我们通过`ndarray.__mod__()`方法传递的值用于对数组的每个元素执行 mod 操作。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2.5, 3, 4.8, 5])

# applying ndarray.__mod__() method
print(gfg.__mod__(2))
```

**Output:**

```py
[ 1\.   0.5  1\.   0.8  1\. ]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4.45, 5],
                [6, 5.5, 4, 3, 2.62]])

# applying ndarray.__mod__() method
print(gfg.__mod__(3))
```

**Output:**

```py
[[ 1\.    2\.    0\.    1.45  2\.  ]
 [ 0\.    2.5   1\.    0\.    2.62]]

```