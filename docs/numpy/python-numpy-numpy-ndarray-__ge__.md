# python | num py . ndaarray . _ _ _ ge _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ ge _/

借助于 **Numpy** 的 **numpy.ndarray.__ge__()** 方法，我们可以发现数组中的哪个元素大于或等于参数中提供的值**。它将返回一个布尔类型的 numpy 数组，只有值**真**和**假**。**

> **语法:**n 数组。__ge__($self，value，/)
> 
> **返回:**自我>=值

**示例#1 :**
在这个示例中，我们可以看到在应用`numpy.__ge__()`之后，我们得到了简单的布尔数组，它可以告诉我们数组中的哪个元素大于或等于提供的参数的元素。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5, 6])

# applying numpy.__ge__() method
print(gfg.__ge__(4))
```

**Output:**

```py
[False False False  True  True  True]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5, 6],
                [6, 5, 4, 3, 2, 1]])

# applying numpy.__ge__() method
print(gfg.__ge__(4))
```

**Output:**

```py
[[False False False  True  True  True]
 [ True  True  True False False False]]

```