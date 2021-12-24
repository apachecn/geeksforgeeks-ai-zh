# python | num py ndaarray。_ _ _ _ _ ixor _(

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ _ _ _ ixor _/

借助`**Numpy ndarray.__ixor__()**`方法，我们可以通过`numpy.ndarray.__ixor__()`方法中作为参数提供的值得到异或的元素。

> **语法:**n 数组。_ _ ixor _($ self，value，/)
> 
> **返回:** self^=value

**示例#1 :**
在这个示例中，我们可以看到每个元素都被作为参数在`ndarray.__ixor__()`方法中传递的值异或。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__ixor__() method
print(gfg.__ixor__(2))
```

**Output:**

```py
[3 0 1 6 7]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__ixor__() method
print(gfg.__ixor__(1))
```

**Output:**

```py
[[0 3 2 5 4]
 [7 4 5 2 3]]

```