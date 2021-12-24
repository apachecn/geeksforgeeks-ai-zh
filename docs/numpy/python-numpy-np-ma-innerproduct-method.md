# python | num py NP . ma . intraproduct()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-ma-inner product-method/](https://www.geeksforgeeks.org/python-numpy-np-ma-innerproduct-method/)

借助`**np.ma.innerproduct()**`方法，我们可以用`np.ma.innerproduct()`方法计算两个列表的向量乘积。

> **语法:** `np.ma.innerproduct()`
> **返回:**返回两个列表的向量乘积。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.ma.innerproduct()`方法，我们能够得到两个向量的内积的值。

```py
# import numpy
import numpy.ma as ma

# using np.ma.innerproduct() method
gfg = ma.innerproduct([1, 2, 3], [5, 5, 5])

print(gfg)
```

**输出:**

> Thirty

**例 2 :**

```py
# import numpy
import numpy.ma as ma

# using np.ma.innerproduct() method
gfg = ma.innerproduct([[1, 2, 3], [7, 8, 9]], [5, 5, 5])

print(gfg)
```

**输出:**

> [ 30 120]