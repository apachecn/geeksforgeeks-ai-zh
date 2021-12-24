# Python | Numpy getmaskarray()方法

> 原文:[https://www . geesforgeks . org/python-numpy-getmaskarray-method/](https://www.geeksforgeeks.org/python-numpy-getmaskarray-method/)

借助`**numpy.getmaskarray()**`方法，我们可以用`numpy.getmaskarray()`方法得到以 numpy 数组形式表示掩码值的掩码矩阵。

> **语法:** `numpy.getmaskarray(array)`
> 
> **返回:**以 numpy 数组的形式返回屏蔽值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`numpy.getmaskarray()`方法，我们能够获得 numpy 数组形式的掩码矩阵。

```py
# import numpy
import numpy.ma as ma

gfg = ma.masked_equal([[1, 2], [5, 6]], 5)

# using numpy.getmaskarray() method
print(ma.getmaskarray(gfg))
```

**输出:**

> 数组([[假假]
> [真假]])

**例 2 :**

```py
# import numpy
import numpy.ma as ma

gfg = ma.masked_equal([11, 12, 13, 14, 15], 12)

# using numpy.getmaskarray() method
print(ma.getmaskarray(gfg))
```

**输出:**

> 数组([假真假假])