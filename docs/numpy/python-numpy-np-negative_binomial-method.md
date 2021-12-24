# Python | Numpy NP . negative _ binomial()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-negative _ binomial-method/](https://www.geeksforgeeks.org/python-numpy-np-negative_binomial-method/)

借助`**np.negative_binomial()**`方法，利用`np.negative_binomial()`方法可以得到负二项式数列的数组。

> **语法:** `np.negative_binomial(n, p, size)`
> **返回:**返回一组负二项式数列。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.negative_binomial()`方法，我们能够使用该方法获得负二项式序列的数组。

```
# import numpy
import numpy as np

# using np.negative_binomial() method
gfg = np.random.negative_binomial(3, 0.33, 10)

print(gfg)
```

**输出:**

> [ 8 12 23 1 2 7 5 3 1 5]

**例 2 :**

```
# import numpy
import numpy as np

# using np.negative_binomial() method
gfg = np.random.negative_binomial(5, 0.1234, 50)

print(gfg)
```

**输出:**

> [15 26 60 19 15 18 15 55 46 36 28 50 13 47 40 56 24 80 47 19 36 62 45 57
> 37 32 15 28 20 65 40 34 34 35 28 38 43 50 20 71 33 40 31 50 25 29 46 38
> 32 86]