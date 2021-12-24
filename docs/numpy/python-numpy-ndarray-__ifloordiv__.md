# python | num py ndaarray。_ _ _ _ _ _ _ _()

> 哎哎哎::1230【https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ _ ifordiv _/

借助`**Numpy ndarray.__ifloordiv__()**`，我们可以划分一个特定的值，该值在`ndarray.__ifloordiv__()`方法中作为参数提供。数值将被分配给 numpy 数组中的每个元素，记住它总是在分配后给出最低值。

> **语法:**n 数组。_ _ ifloodiv _ _($ self，value，/)
> 
> **返回:**self//=值

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用方法`ndarray.__ifloordiv__()`中作为参数给出的值进行了划分，并给出了数组中被划分的每个元素的基底值。此方法对于数组的正、负和浮点值都很有效。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2.5, 3, 4.8, 5])

# applying ndarray.__ifloordiv__() method
print(gfg.__ifloordiv__(2))
```

**Output:**

```py
[ 0\.  1\.  1\.  2\.  2.]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4.45, 5],
                [6, 5.5, 4, 3, 2.62]])

# applying ndarray.__ifloordiv__() method
print(gfg.__ifloordiv__(3))
```

**Output:**

```py
[[ 0\.  0\.  1\.  1\.  1.]
 [ 2\.  1\.  1\.  1\.  0.]]

```