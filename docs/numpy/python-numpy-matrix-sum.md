# Python | Numpy matrix.sum()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-sum/](https://www.geeksforgeeks.org/python-numpy-matrix-sum/)

借助`**matrix.sum()**`方法，我们可以用同样的方法求出矩阵中值的和。

> **语法:** `matrix.sum()`
> **返回:**返回矩阵中值的总和

**示例#1 :**
在本例中，我们能够使用`matrix.sum()`方法找到矩阵中值的总和。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.sum() method
geek = gfg.sum()

print(geek)
```

**Output:**

```
20

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.sum() method
geek = gfg.sum(axis = 1)

print(geek)
```

**Output:**

```
[[14]
 [16]
 [15]]

```