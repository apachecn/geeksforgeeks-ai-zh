# python | num py matrix . set field()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-setfield/

借助`**matrix.setfield()**`方法，将矩阵中的所有字段设置为以参数形式传递的值。

> **语法:** `matrix.setfield()`
> 
> **返回:**值作为参数传递的新矩阵

**Example #1 :**

在这个例子中，我们可以看到`matrix.setfield()`方法用于生成一个新的矩阵，该矩阵的值在这个方法中作为参数传递。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.setfield() method
gfg.setfield(2, np.int32)

print(gfg)
```

**Output:**

```py
[[2 2]
 [2 2]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.setfield() method
gfg.setfield(25, np.int32)

print(gfg)
```

**Output:**

```py
[[25 25 25]
 [25 25 25]
 [25 25 25]]

```