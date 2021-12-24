# Python | Numpy matrix . trace()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-trace/](https://www.geeksforgeeks.org/python-numpy-matrix-trace/)

借助`**Numpy matrix.trace()**`方法，我们可以用`matrix.trace()`方法求出一个矩阵所有对角线元素的和。

> **语法:** `matrix.trace()`
> **返回:** **返回矩阵对角线元素之和**

**示例#1 :**
在这个示例中我们可以看到，通过使用`**matrix.trace()**`方法可以帮助我们找到给定矩阵的对角线的所有元素的和。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.trace() method
geek = gfg.trace()

print(geek)
```

**Output:**

```py
[[7]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.trace() method
geek = gfg.trace()

print(geek)
```

**Output:**

```py
[[13]]

```