# python | num py ndaarray。_ _ _ _ irshift _ _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray _ _ _ _ irshift _/

借助`**numpy.ndarray.__irshift__()**`方法，我们可以得到被`numpy.ndarray.__irshift__()`方法中作为参数提供的值右移的元素。

> **语法:**n 数组。__irshift__($self，value，/)
> 
> **返回:**自我>>=值

**示例#1 :**
在这个示例中，我们可以看到每个元素都向右移动了在`ndarray.__irshift__()`方法中作为参数传递的值。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__irshift__() method
print(gfg.__irshift__(2))
```

**Output:**

```
[0 0 0 1 1]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__irshift__() method
print(gfg.__irshift__(1))
```

**Output:**

```
[[0 1 1 2 2]
 [3 2 2 1 1]]

```