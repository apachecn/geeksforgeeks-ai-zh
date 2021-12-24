# python | num py . matrix . t()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-matrix-t/

借助`**Numpy numpy.matrix.T()**`方法，我们可以对任意一维或一维以上的矩阵进行转置。

> **语法:** `numpy.matrix.T()`
> 
> **返回:** *返回每个矩阵的转置*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.T()`方法，我们能够变换任何类型的矩阵。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4]')

# applying matrix.T() method
geeks = gfg.getT()

print(geeks)
```

**Output:**

```
[[1]
 [2]
 [3]
 [4]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.T() method
geeks = gfg.getT()

print(geeks)
```

**Output:**

```
[[1 4 7]
 [2 5 8]
 [3 6 9]]

```