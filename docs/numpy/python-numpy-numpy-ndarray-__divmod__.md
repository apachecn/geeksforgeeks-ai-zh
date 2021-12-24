# python | numpy num py . ndaarray . _ _ _ divmod _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray _ _ _ _ divmod _/

借助`**Numpy numpy.ndarray.__divmod__()**`方法，我们将得到两个数组，一个是具有被`numpy.ndarray.__divmod__()`方法中提供的值除以的元素，第二个是具有与`numpy.ndarray.__divmod__()`方法中提供的值相同的执行 **mod** 操作的元素。

> **语法:**n 数组。__divmod__($self，value，/)
> 
> **返回:** divmod(自我，值)

**示例#1 :**
在这个示例中，我们可以看到，通过使用`ndarray.__divmod__()`方法，我们得到了两个数组。一个是用作为参数传递的值除以，另一个是用 mod 值。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__divmod__() method
print(gfg.__divmod__(3))
```

**Output:**

```py
(array([0, 0, 1, 1, 1]), array([1, 2, 0, 1, 2]))

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__divmod__() method
print(gfg.__divmod__(3))
```

**Output:**

```py
(array([[0, 0, 1, 1, 1],
       [2, 1, 1, 1, 0]]), 
 array([[1, 2, 0, 1, 2],
       [0, 2, 1, 0, 2]]))

```