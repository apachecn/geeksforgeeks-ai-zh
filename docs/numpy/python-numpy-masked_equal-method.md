# python | Numpy masked_equal()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-masked _ equal-method/](https://www.geeksforgeeks.org/python-numpy-masked_equal-method/)

借助`**numpy.ma.masked_equal()**`方法，我们可以通过使用`numpy.ma.masked_equal()`方法获得数组中的掩码值。

> **语法:** `numpy.ma.masked_equal(array, value)`
> 
> **返回:**去掉掩码值后返回数组。

**示例#1 :**

在这个例子中，我们可以看到，通过使用`numpy.ma.masked_equal()`方法，我们能够在移除与数组一起传递的掩码值之后获得新的数组。

```py
# import numpy
import numpy.ma as ma

# using numpy.ma.masked_equal() method
gfg = ma.masked_equal([1, 2, 3, 4], 3)

print(gfg)
```

**输出:**

> [1 2 — 4]

**例 2 :**

```py
# import numpy
import numpy.ma as ma

# using numpy.ma.masked_equal() method
gfg = ma.masked_equal([[1, 2, 3, 4],
                       [6, 7, 8, 9]], 6)

print(gfg)
```

**输出:**

> [[1 2 3 4]
> [–7 8 9]]