# python | num py matrix . item set()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py 矩阵项集/

借助`**Numpy matrix.itemset()**`方法，只需提供索引号和项目，就可以在给定的矩阵中设置**项目**。

> **语法:** `matrix.itemset(index, item)`
> 
> **返回:** *返回有物品的新矩阵*

**示例#1 :**
在这个示例中，我们可以看到，通过提供索引号和项目，我们可以借助方法`matrix.itemset()`来设置项目。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 1; 2, 3]')

# applying matrix.itemset() method
gfg.itemset((1, 0), 5)

print(gfg)
```

**Output:**

```py
[[6 1]
 [5 3]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.itemset() method
gfg.itemset((2, 0), 10)

print(gfg)
```

**Output:**

```py
[[ 1  2  3]
 [ 4  5  6]
 [10  8  9]]

```