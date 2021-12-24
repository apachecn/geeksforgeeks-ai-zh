# python | numpy num py . ndaarray . _ _ _ xorg _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ _ _ _ _/上

借助`**Numpy numpy.ndarray.__xor__()**`方法，我们可以通过`numpy.ndarray.__xor__()`方法中作为参数提供的值，得到**异或**的元素。

> **语法:**n 数组。__xor__($self，value，/)
> 
> **返回:** self^value

**示例#1 :**
在这个示例中，我们可以看到每个元素都通过在`ndarray.__xor__()`方法中作为参数传递的值进行**异或**。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__xor__() method
print(gfg.__xor__(2))
```

**Output:**

```
[3 0 1 6 7]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__xor__() method
print(gfg.__xor__(1))
```

**Output:**

```
[[0 3 2 5 4]
 [7 4 5 2 3]]

```