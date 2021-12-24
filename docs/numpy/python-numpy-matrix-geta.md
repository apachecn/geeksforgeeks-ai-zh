# Python | Numpy matrix . geta()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-geta/

借助`**Numpy matrix.getA()**`方法，我们可以得到与给定矩阵相同大小的**数组**。

> **语法:** `matrix.getA()`
> 
> **返回:** *返回与给定矩阵相同大小的数组*

**示例#1 :**
在这个示例中，我们可以看到我们能够借助方法`matrix.getA()`获得 numpy 数组。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6; 2; 3]')

# applying matrix.getA() method
geeks = gfg.getA()

print(geeks)
```

**Output:**

```py
[[6]
 [2]
 [3]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.getA() method
geeks = gfg.getA()

print(geeks)
```

**Output:**

```py
[[1 2 3]
 [4 5 6]
 [7 8 9]]

```