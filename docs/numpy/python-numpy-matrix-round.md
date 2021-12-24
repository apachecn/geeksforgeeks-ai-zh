# Python | Numpy matrix . round()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-round/](https://www.geeksforgeeks.org/python-numpy-matrix-round/)

借助`**Numpy matrix.round()**`方法，我们能够**舍入**给定矩阵的值。

> **语法:** `matrix.round()`
> 
> **返回:** *返回矩阵中的舍入值*

**示例#1 :**

在给定的例子中，我们能够通过使用`matrix.round()`方法来舍入给定的矩阵。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6.4, 1.3; 12.7, 32.3]')

# applying matrix.round() method
geeks = gfg.round()

print(geeks)
```

**Output:**

```
[[  6\.   1.]
 [ 13\.  32.]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1.2, 2.3; 4.7, 5.5; 7.2, 8.9]')

# applying matrix.round() method
geeks = gfg.round()

print(geeks)
```

**Output:**

```
[[ 1\.  2.]
 [ 5\.  6.]
 [ 7\.  9.]]

```