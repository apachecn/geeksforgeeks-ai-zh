# Python | Numpy np.kron()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-kron-method/](https://www.geeksforgeeks.org/python-numpy-np-kron-method/)

借助`**np.kron()**`方法，我们可以用`np.kron()`方法得到两个列表的**克罗内克**乘积。

> **语法:** `np.kron(list1, list2)`
> 
> **返回:**返回两个列表的 kronecker 积。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.kron()`方法，我们能够获得作为参数传递的两个数组的 kronecker 积。

```py
# import numpy
import numpy as np

# using np.kron() method
gfg = np.kron([1, 2, 3], [5, 10, 15])

print(gfg)
```

**输出:**

> [ 5 10 15 10 20 30 15 30 45]

**例 2 :**

```py
# import numpy
import numpy as np

# using np.kron() method
gfg = np.kron([[1, 2, 3], [9, 8, 7]], [5, 10, 15])

print(gfg)
```

**输出:**

> [[5 10 15 10 20 30 15 30 45]
> [45 90 135 40 80 120 35 70 105]]