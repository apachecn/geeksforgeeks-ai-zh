# Python | Numpy matrix . geta 1()

> 哎哎哎::1230【https://www . geeksforgeeks . org/python-num py-matrix-geta 1/

借助于`**Numpy matrix.getA1()**`方法，我们可以得到给定矩阵的一维**矩阵**。

> **语法:** `matrix.getA1()`
> 
> **返回:** *返回给定矩阵的一维数组*

**示例#1 :**
在这个示例中，我们可以看到我们能够借助方法`matrix.getA1()`获得 numpy 数组。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6; 2; 3]')

# applying matrix.getA1() method
geeks = gfg.getA1()

print(geeks)
```

**Output:**

```py
[6 2 3]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.getA1() method
geeks = gfg.getA1()

print(geeks)
```

**Output:**

```py
[1 2 3 4 5 6 7 8 9]

```