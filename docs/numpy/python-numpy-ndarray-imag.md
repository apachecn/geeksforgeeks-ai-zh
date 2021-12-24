# python | num py ndaarray . imag()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-imag/

借助`**Numpy ndarray.imag()**`方法，我们只需使用`ndarray.imag()`方法就可以找到虚数表达式中的虚数。记住虚数的结果数据类型是**“浮点 64”**。

> **语法:** `ndarray.imag()`
> 
> **返回:** *虚数数组，数据类型为“float 64”*

**示例#1 :**
在本例中，我们可以看到，我们使用`ndarray.imag()`方法获得了虚数数组，并且我们还在尝试打印这些虚数的数据类型。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1 + 2j, 2 + 3j])

# applying ndarray.imag() method
geeks = np.imag(gfg)

print(geeks, end ='\n\n')
print(np.imag(geeks).dtype)
```

**Output:**

```py
[ 2\.  3.]

float64

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1 + 2j, 2 + 3j])
gfg = np.sqrt(gfg)

# applying ndarray.imag() method
geeks = np.imag(gfg)

print(geeks, end ='\n\n')
print(np.imag(geeks).dtype)
```

**Output:**

```py
[ 0.78615138  0.89597748]

float64

```