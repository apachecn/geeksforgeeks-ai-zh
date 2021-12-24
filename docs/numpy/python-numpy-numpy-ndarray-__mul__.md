# python | numpy num py . ndaarray . _ _ _ mul _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ mul _/

借助`**Numpy numpy.ndarray.__mul__()**`，我们可以将`ndarray.__mul__()`方法中作为参数提供的特定值相乘。值将乘以 **numpy 数组**中的每个元素。

> **语法:**n 数组。__mul__($self，value，/)
> 
> **返回:**自身*值

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都与方法`ndarray.__mul__()`中作为参数给出的值相乘。此方法对于数组的正、负和浮点值都很有效。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2.5, 3, 4.8, 5])

# applying ndarray.__mul__() method
print(gfg.__mul__(5))
```

**Output:**

```
[  5\.   12.5  15\.   24\.   25\. ]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4.45, 5],
                [6, 5.5, 4, 3, 2.62]])

# applying ndarray.__mul__() method
print(gfg.__mul__(5))
```

**Output:**

```
[[  5\.    10\.    15\.    22.25  25\.  ]
 [ 30\.    27.5   20\.    15\.    13.1 ]]

```