# python | num py NP . triu _ indices

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-NP-triu _ indices/

借助`**np.triu_indices()**`方法，我们可以用`np.triu_indices()`方法得到一个[n，m]数组的上三角的索引。

> **语法:** `np.triu_indices(n, m)`
> 
> **返回:**返回上三角的指数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.triu_indices()`方法，我们能够使用该方法获得[n，m]数组的上三角形的索引。

```py
# import numpy and triu_indices
import numpy as np

# using np.triu_indices() method
gfg = np.triu_indices(2, 3)

print(gfg)
```

**输出:**

> (数组([]，dtype = int64)，数组([]，dtype = int64))

**例 2 :**

```py
# import numpy and triu_indices
import numpy as np

# using np.triu_indices() method
gfg = np.triu_indices(4)

print(gfg)
```

**输出:**

> 数组([]，dtype = int64)