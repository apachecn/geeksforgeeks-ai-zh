# Python | Numpy matrix.std()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-std/](https://www.geeksforgeeks.org/python-numpy-matrix-std/)

借助`**matrix.std()**`方法，我们可以用同样的方法求出一个矩阵的标准差。

> **语法:** `matrix.std()`
> **返回:**返回矩阵的标准差

**示例#1 :**
在本例中，我们能够使用`matrix.std()`方法找到矩阵的标准差。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.std() method
geek = gfg.std()

print(geek)
```

**Output:**

```py
4.18330013267

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.std() method
geek = gfg.std()

print(geek)
```

**Output:**

```py
3.3993463424

```