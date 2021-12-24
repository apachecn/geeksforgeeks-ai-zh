# python | num py . ndaarray . _ _ _ lshift _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray _ _ _ _ lshift _/

借助`**Numpy numpy.ndarray.__lshift__()**`方法，我们可以通过`numpy.ndarray.__lshift__()`方法中作为参数提供的值，得到**左移**的元素。

> **语法:**n 数组。_ _ lsshift _ _($ self，value，/)
> 
> **返回:**自我<T3】值

**示例#1 :**
在这个示例中，我们可以看到每个元素都向左移动了在`ndarray.__lshift__()`方法中作为参数传递的值。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__lshift__() method
print(gfg.__lshift__(2))
```

**Output:**

```
[ 4  8 12 16 20]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__lshift__() method
print(gfg.__lshift__(1))
```

**Output:**

```
[[ 2  4  6  8 10]
 [12 10  8  6  4]]

```