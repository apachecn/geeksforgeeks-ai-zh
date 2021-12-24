# python | num py ndaarray。_ _ _ _ _ _ _ _ iand _ _(

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ iand _/

借助`**Numpy ndarray.__iand__()**`方法，我们可以得到由`numpy.ndarray.__iand__()`方法中作为参数提供的值进行 and 运算的元素。

> **语法:**n 数组。__ 和 _ _($自我，价值，/)
> 
> **返回:**自我&=值

**示例#1 :**
在这个示例中，我们可以看到每个元素都由在`ndarray.__iand__()`方法中作为参数传递的值进行 and 运算。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__iand__() method
print(gfg.__iand__(2))
```

**Output:**

```py
[0 2 2 0 0]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__iand__() method
print(gfg.__iand__(1))
```

**Output:**

```py
[[1 0 1 0 1]
 [0 1 0 1 0]]

```