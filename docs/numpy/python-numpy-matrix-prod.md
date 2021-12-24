# Python | Numpy matrix . prod()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-prod/

借助`**Numpy matrix.prod()**`方法，我们可以从给定的矩阵中得到同一轴上所有元素的**累积积**。

> **语法:** `matrix.prod(axis)`
> 
> **返回:** *从给定矩阵返回产品*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.prod()`，我们能够从给定的矩阵中获得同一轴上所有元素的乘积。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.prod() method
geeks = gfg.prod(1)

print(geeks)
```

**Output:**

```py
[[64]
 [36]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, -9]')

# applying matrix.prod() method
geeks = gfg.prod(0)

print(geeks)
```

**Output:**

```py
[[  28   80 -162]]

```