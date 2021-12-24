# python | num py ndaarray . real()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-real/

借助`**Numpy ndarray.real()**`方法，我们只需使用`ndarray.real()`方法就可以在一个虚数表达式中找到实值。记住真实值的结果数据类型是**“浮点 64”**。

> **语法:** `ndarray.real()`
> 
> **返回:** *实数值数组，数据类型为“float 64”*

**示例#1 :**
在这个示例中，我们可以看到我们使用`ndarray.real()`方法获得了实值数组，并且我们还在尝试打印这些实值的数据类型。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1 + 2j, 2 + 3j])

# applying ndarray.real() method
geeks = np.real(gfg)

print(geeks, end ='\n\n')
print(np.real(geeks).dtype)
```

**Output:**

```py
[ 1\.  2.]

'float64'

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1 + 2j, 2 + 3j])
gfg = np.sqrt(gfg)

# applying ndarray.real() method
geeks = np.real(gfg)

print(geeks, end ='\n\n')
print(np.real(geeks).dtype)
```

**Output:**

```py
[ 1.27201965  1.67414923]

float64

```