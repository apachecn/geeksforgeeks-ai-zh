# python | num py . choose()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-choose/

借助`**Numpy numpy.choose()**`方法，我们可以通过传递一个参数作为包含要选择的行号索引的数组，从多维数组中选择元素。输出数组的大小与参数中传递的大小相同。

> **语法:** `numpy.choose()`
> 
> **返回:** *返回元素选择的数组*

**示例#1 :**
在这个示例中，我们可以看到，借助`numpy.choose()`方法，我们能够从多维数组中提取选择数组。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = [[1, 2, 3, 4], [3, 1, 5, 6]]

# applying numpy.choose() method
geeks = np.choose([1, 0, 1, 0], gfg)

print(geeks)
```

**Output:**

```py
array([3 2 5 4])

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

# applying numpy.choose() method
geeks = np.choose([2, 0, 1], gfg)

print(geeks)
```

**Output:**

```py
array([7 2 6])

```