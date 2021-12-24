# python | num py matrix . tolist()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-tolist/](https://www.geeksforgeeks.org/python-numpy-matrix-tolist/)

借助`**Numpy matrix.tolist()**`方法，我们可以使用`matrix.tolist()`方法将矩阵转换为列表。

> **语法:** `matrix.tolist()`
> **返回:** **返回新列表**

**示例#1 :**
在这个示例中，我们可以看到，通过传递矩阵，我们可以使用`matrix.tolist()`方法将其转换为列表。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 12, 3]')

# applying matrix.tolist() method
geek = gfg.tolist()

print(geek)
```

**Output:**

```py
[[4, 1, 12, 3]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.tolist() method
geek = gfg.tolist()

print(geek)
```

**Output:**

```py
[[4, 1, 9], [12, 3, 1], [4, 5, 6]]

```