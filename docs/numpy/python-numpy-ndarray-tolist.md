# python | num py ndaarray . tolist()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-tolist/

借助`**numpy.ndarray.tolist()**`方法，我们可以得到数据元素列表，该列表是使用`ndarray.tolist()`方法从**数组**转换而来的。

> **语法**ndar . tolist()
> 
> **参数:**无
> 
> **返回:**数组元素的可能嵌套列表。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`ndarray.tolist()`方法，我们可以拥有 ndarray 中的数据项列表。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.tolist() method
print(gfg.tolist())
```

**Output:**

```py
[1, 2, 3, 4, 5]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.tolist() method
print(gfg.tolist())
```

**Output:**

```py
[[1, 2, 3, 4, 5], [6, 5, 4, 3, 2]]

```