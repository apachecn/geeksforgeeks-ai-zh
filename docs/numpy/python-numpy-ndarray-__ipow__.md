# python | num py ndaarray。_ _ _ _ _ _ _ _ ipow _ _(

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ ipow _/

借助`**Numpy ndarray.__ipow__()**`方法，我们将获得所有元素的供电值，该值在`numpy.ndarray.__ipow__()`方法中作为参数提供。

> **语法:**n 数组。__ipow__($self，value，/)
> 
> **返回:**自* * =值

**示例#1 :**
在此示例中，我们可以看到每个元素都使用`ndarray.__ipow__()`方法中作为参数提供的值供电。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__ipow__() method
print(gfg.__ipow__(3))
```

**Output:**

```py
[  1   8  27  64 125]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__ipow__() method
print(gfg.__ipow__(2))
```

**Output:**

```py
[[ 1  4  9 16 25]
 [36 25 16  9  4]]

```