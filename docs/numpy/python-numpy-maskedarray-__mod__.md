# Python | Numpy MaskedArray。_ _ _ _ _ mod _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array _ _/t1]

**什么是面具？**
一个布尔数组，用于为一个操作只选择某些元素

```py
# A mask example
import numpy as np
x = np.arange(5)
print(x)
mask = (x > 2)
print(mask)
x[mask] = -1
print(x)
```

**输出:**

```py
[0 1 2 3 4]
[False False False  True  True]
[ 0  1  2 -1 -1]

```

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__mod__* 掩码数组中的每个元素都是用二进制运算符操作的，即 mod(%)。请记住，我们可以在数组中使用任何类型的值，mod 的值将作为 MaskedArray 中的参数应用。__mod__()。

> **语法:**num py . masked array . _ _ _ _ _ _ _ _
> 
> **返回:**返回自身%值。

**示例#1 :**
我们可以看到通过 MaskedArray 传递的值。__mod__()方法用于对数组的每个元素执行 mod 操作。

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2.5, 3, 4.8, 5]) 

# applying MaskedArray.__mod__() method 
print(gfg.__mod__(2)) 
```

**Output:**

```py
[1.0 0.5 1.0 0.7999999999999998 1.0]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4.45, 5], 
                [6, 5.5, 4, 3, 2.62]]) 

# applying MaskedArray.__mod__() method 
print(gfg.__mod__(3)) 
```

**Output:**

```py
[[1.0 2.0 0.0 1.4500000000000002 2.0]
 [0.0 2.5 1.0 0.0 2.62]]

```