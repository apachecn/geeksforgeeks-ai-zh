# python | num py ndaarray。_ _ _ _ _ _ _ _ _ 年 _ _ _ _ 月 _ _ _ _ 日〔t1〕

> 哎哎哎::1230【https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ _ _ _ _ _/

借助`**Numpy ndarray.__ior__()**`方法，我们可以通过`numpy.ndarray.__ior__()`方法中作为参数提供的值得到为或的元素。

> **语法:**n 数组。__ior__($self，value，/)
> 
> **返回:**自| =值

**示例#1 :**
在这个示例中，我们可以看到每个元素都是或者是在`ndarray.__ior__()`方法中作为参数传递的值。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__ior__() method
print(gfg.__ior__(2))
```

**Output:**

```
[3 2 3 6 7]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__ior__() method
print(gfg.__ior__(1))
```

**Output:**

```
[[1 3 3 5 5]
 [7 5 5 3 3]]

```