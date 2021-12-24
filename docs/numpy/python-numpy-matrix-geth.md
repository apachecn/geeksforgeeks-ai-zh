# python | num py matrix . geth()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-geth/](https://www.geeksforgeeks.org/python-numpy-matrix-geth/)

借助于`**Numpy numpy.matrix.getH()**`方法，我们可以对任意一维或一维以上的复矩阵进行共轭转置。

> **语法:** `matrix.getH()`
> 
> **返回:** *返回复矩阵的共轭转置*

**例#1 :**
在这个例子中我们可以看到，借助`matrix.getH()`我们可以得到任意维数的复矩阵的共轭转置。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix([1-2j, 3-4j])

# applying matrix.getH() method
geeks = gfg.getH()

print(geeks)
```

**Output:**

```
[[ 1.+2.j]
 [ 3.+4.j]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix([[1-5j, 2 + 5j, 3-3j], [4 + 6j, 5-8j, 6-2j], [7 + 6j, 8-6j, 9 + 1.j]])

# applying matrix.getH() method
geeks = gfg.getH()

print(geeks)
```

**Output:**

```
[[ 1.+5.j  4.-6.j  7.-6.j]
 [ 2.-5.j  5.+8.j  8.+6.j]
 [ 3.+3.j  6.+2.j  9.-1.j]]

```