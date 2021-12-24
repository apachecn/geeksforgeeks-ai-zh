# python | num py ndaarray。t〔t1〕

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-t/

借助`**Numpy ndarray.T**`对象，我们可以对维度大于等于 2 的数组进行**转置**。

> 语法:`**ndarray.T**`
> 
> 返回:数组的转置

**示例#1 :**
在这个示例中，我们可以看到在`ndarray.T`对象的帮助下，我们能够变换一个数组。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3], [4, 5, 6]])

# applying ndarray.T object
geeks = gfg.T

print(geeks)
```

**Output:**

```
[[1 4]
 [2 5]
 [3 6]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4], [4, 5, 6, 7], [7, 8, 9, 0]])

# applying ndarray.T object
geeks = gfg.T

print(geeks)
```

**Output:**

```
[[1 4 7]
 [2 5 8]
 [3 6 9]
 [4 7 0]]

```