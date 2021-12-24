# python | numpy num py . ndaarray . _ _ _ imml _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ imml _/

借助 **numpy.ndarray.__imul__()** 方法，我们可以乘以一个特定的值，该值在 ndarray 中作为参数提供。__imul__()方法。数值将被**乘以**到 numpy 数组中的每个元素。

> **语法:**n 数组。__imul__($self，value，/)
> **返回:** self*=value

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都是**乘以**的值，该值在方法 ndarray 中作为参数给出。__imul__()。请记住，此方法适用于所有类型的数值。

## 蟒蛇 3

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1.2, 2.6, 3, 4.5, 5])

# applying ndarray.__imul__() method
print(gfg.__imul__(5))
```

**Output:** 

```
[  6\.   13\.   15\.   22.5  25\. ]
```

**例 2 :**

## 蟒蛇 3

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2.2, 3, 4, 5.01],
                [6.1, 5, 4.8, 3, 2]])

# applying ndarray.__imul__() method
print(gfg.__imul__(3))
```

**Output:** 

```
[[  3\.     6.6    9\.    12\.    15.03]
 [ 18.3   15\.    14.4    9\.     6\.  ]]
```