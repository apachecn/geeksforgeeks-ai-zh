# python | num py . matrix . a()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-matrix-a/

借助`**Numpy numpy.matrix.A()**`方法，我们可以得到与自我相同的矩阵。这意味着通过这种方法我们可以得到相同的矩阵。

> **语法:** `numpy.matrix.A()`
> 
> **返回:** *返回自身矩阵*

**例#1 :**
在这个例子中我们可以看到，借助`matrix.A()`方法，我们能够得到自矩阵。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4]')

# applying matrix.A() method
geeks = gfg.getA()

print(geeks)
```

**Output:**

```
[[1 2 3 4]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.A() method
geeks = gfg.getA()

print(geeks)
```

**Output:**

```
[[1 2 3]
 [4 5 6]
 [7 8 9]]

```