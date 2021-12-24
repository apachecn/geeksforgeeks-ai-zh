# python | num py get ask()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-getmask-method/](https://www.geeksforgeeks.org/python-numpy-getmask-method/)

借助`**numpy.getmask()**`方法，我们可以得到 numpy 数组的掩码矩阵，该矩阵通过`numpy.getmask()`方法显示掩码值。

> **语法:** `numpy.getmask(array)`
> 
> **返回:**返回矩阵的屏蔽值。

**示例#1 :**

在这个例子中我们可以看到，通过使用`numpy.getmask()`方法，我们能够得到一个数组的掩码矩阵。

```
# import numpy
import numpy.ma as ma

gfg = ma.masked_equal([[1, 2], [5, 6]], 5)

# using numpy.getmask() method
print(ma.getmask(gfg))
```

**输出:**

> 【【假假】
> 【真假】】

**例 2 :**

```
# import numpy
import numpy.ma as ma

gfg = ma.masked_equal([11, 12, 13, 14, 15], 12)

# using numpy.getmask() method
print(ma.getmask(gfg))
```

**输出:**

> [假真假假假]