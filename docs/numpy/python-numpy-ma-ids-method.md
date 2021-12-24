# Python | numpy.ma.ids()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-ma-ids-method/](https://www.geeksforgeeks.org/python-numpy-ma-ids-method/)

借助`**numpy.ma.ids()**`方法，我们可以利用`numpy.ma.ids()`方法得到有数据的掩码数组的地址。

> **语法:** `numpy.ma.ids(array, mask)`
> **返回:**返回蒙面阵的地址。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.ma.ids()`方法，我们能够获得目标掩码数组的地址。

```
# import numpy.ma
import numpy.ma as ma

# using numpy.ma.ids() method
gfg = ma.array([1, 2, 4, 8], mask =[1, 0, 0, 1])

print(gfg.ids())
```

**输出:**

> (2172543392448, 2172542026240)

**例 2 :**

```
# import numpy.ma
import numpy.ma as ma

# using numpy.ma.ids() method
gfg = ma.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]], 
         mask =[[1, 0, 0], [0, 1, 0], [0, 0, 1]])

print(gfg.ids())
print(gfg)
```

**输出:**

> (2172299359856, 2172543392224)
> 
> masked _ array(
> data =[[–，2，3]，
> [4，–，6]，
> [7，8，–]，
> mask=[[ True，False，False]，
> [False，True，False]，
> [False，False，True]，
> fill_value=999999)