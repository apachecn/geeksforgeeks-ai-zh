# Python | Numpy NP . multiply _ normal()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-multiva _ normal-method/](https://www.geeksforgeeks.org/python-numpy-np-multivariate_normal-method/)

借助`**np.multivariate_normal()**`方法，我们可以利用`np.multivariate_normal()`方法得到多元正常值的数组。

> **语法:** `np.multivariate_normal(mean, matrix, size)`
> **返回:**返回多元正常值数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.multivariate_normal()`方法，我们能够使用该方法获得多元正常值的数组。

```
# import numpy
import numpy as np

mean = [1, 2]
matrix = [[5, 0], [0, 5]]
# using np.multinomial() method
gfg = np.random.multivariate_normal(mean, matrix, 10)

print(gfg)
```

**输出:**

> 【【6.24847794 6.57894103】
> 【1.24114594 3.22013831】
> 【3.0660329 2.1442572】
> 【0.3239289 2.79949784】
> 【-1.42964186】1.11846394】
> 【-1

**例 2 :**

```
# import numpy
import numpy as np

mean = [0, 0, 0]
matrix = [[1, 0, 0], [0, 1, 0], [0, 0, 1]]
# using np.multinomial() method
gfg = np.random.multivariate_normal(mean, matrix, 5)

print(gfg)
```

**输出:**

> 【-2.21792571-1.04526811-0.4586839】
> 【0.15760965 0.83934119-0.52943583】
> 【-0.9978205 0.79594411-0.00937】
> 【-0.1682821 0.79590937】