# Python | numpy.isin()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-isin-method/](https://www.geeksforgeeks.org/python-numpy-isin-method/)

借助`**numpy.isin()**`方法，我们可以看到一个有值的数组被检查在一个不同的 numpy 数组中，该数组有不同大小的不同元素。

> **语法:** `numpy.isin(target_array, list)`
> 
> **返回:**返回与 target_array 大小相同的布尔数组。

**示例#1 :**

在这个例子中我们可以看到，通过使用`numpy.isin()`方法，如果元素与目标数组匹配，我们就能够得到布尔数组。

```
# import numpy
import numpy as np

# using numpy.isin() method
gfg1 = np.array([1, 2, 3, 4, 5])
lis = [1, 3, 5]
gfg = np.isin(gfg1, lis)

print(gfg)
```

**输出:**

> [真假真假真]

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.isin() method
gfg1 = np.array([[1, 3], [5, 7], [9, 11]])
lis = [1, 3, 11, 9]
gfg = np.isin(gfg1, lis)

print(gfg)
```

**输出:**

> 【【真真】
> 【假假】
> 【真真】】