# python | numpy num py . ndaarray . _ _ _ iadd _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ iadd _/

借助`**numpy.ndarray.__iadd__()**`方法，我们可以添加一个特定的值，该值在`ndarray.__iadd__()`方法中作为参数提供。数值将被**添加到 numpy 数组的每个元素中。**

> **语法:**n 数组。_ _ iadd _ _($自我，价值，/)
> 
> **返回:**自身+=值

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都被**添加了**，该值在方法`ndarray.__iadd__()`中作为参数给出。请记住，此方法适用于所有类型的数值。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1.2, 2.6, 3, 4.5, 5])

# applying ndarray.__iadd__() method
print(gfg.__iadd__(5))
```

**Output:**

```py
[  6.2   7.6   8\.    9.5  10\. ]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2.2, 3, 4, 5.01],
                [6.1, 5, 4.8, 3, 2]])

# applying ndarray.__iadd__() method
print(gfg.__iadd__(3))
```

**Output:**

```py
[[ 4\.    5.2   6\.    7\.    8.01]
 [ 9.1   8\.    7.8   6\.    5\.  ]]

```