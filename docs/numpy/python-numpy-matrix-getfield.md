# python | num py matrix . getfield()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-getfield/

借助`**Numpy matrix.getfield()**`方法，我们可以得到**场矩阵**，这意味着场是矩阵的视图，给定的数据类型与我们给定的矩阵大小相同。

> **语法:** `matrix.getfield()`
> 
> **返回:** *返回场阵*

**例#1 :**
在这个例子中我们可以看到，我们能够借助方法`matrix.getfield()`得到场矩阵。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 1; 2, 3]')

# applying matrix.getfield() method
geeks = gfg.getfield(int)

print(geeks)
```

**Output:**

```py
[[6 1]
 [2 3]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.getfield() method
geeks = gfg.getfield(int)

print(geeks)
```

**Output:**

```py
[[1 2 3]
 [4 5 6]
 [7 8 9]]

```