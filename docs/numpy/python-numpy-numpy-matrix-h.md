# python | num py . matrix . h()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-matrix-h/

借助于`**Numpy numpy.matrix.H()**`方法，我们可以对任意一维或一维以上的复矩阵进行共轭转置。

> **语法:** `numpy.matrix.H()`
> 
> **返回:** *返回每个复矩阵的共轭转置*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.H()`方法，我们能够变换任何类型的复杂矩阵。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix([1-2j, 3-4j])

# applying matrix.H() method
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

# applying matrix.H() method
geeks = gfg.getH()

print(geeks)
```

**Output:**

```
[[ 1.+5.j  4.-6.j  7.-6.j]
 [ 2.-5.j  5.+8.j  8.+6.j]
 [ 3.+3.j  6.+2.j  9.-1.j]]

```