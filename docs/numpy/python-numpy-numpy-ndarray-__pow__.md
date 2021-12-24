# python | num py . ndaarray . _ _ _ pow _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ pow _/

借助`**Numpy numpy.ndarray.__pow__()**`方法，我们将获得所有元素**供电的**，其值在`numpy.ndarray.__pow__()`方法中作为参数提供。

> **语法:**n 数组。__pow__($self，value，mod=None，/)
> 
> **返回:**功率(自身，数值，mod)

**示例#1 :**
在此示例中，我们可以看到每个元素都使用`ndarray.__pow__()`方法中作为参数提供的值供电。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__pow__() method
print(gfg.__pow__(3))
```

**Output:**

```py
[  1   8  27  64  125]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__pow__() method
print(gfg.__pow__(2))
```

**Output:**

```py
[[ 1  4  9 16 25]
 [36 25 16  9  4]]

```