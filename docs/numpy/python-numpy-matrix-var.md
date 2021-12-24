# Python | Numpy matrix.var()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-var/](https://www.geeksforgeeks.org/python-numpy-matrix-var/)

借助`**Numpy matrix.var()**`方法，我们可以用`matrix.var()`方法求出一个矩阵的方差。

> **语法:** `matrix.var()`
> **返回:** **返回矩阵的方差**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`**matrix.var()**`方法，我们能够找到给定矩阵的方差。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.var() method
geek = gfg.var()

print(geek)
```

**Output:**

```
17.5

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.var() method
geek = gfg.var()

print(geek)
```

**Output:**

```
11.5555555556

```