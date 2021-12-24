# python \ numpy 掩码数组。__ 诉 _

案

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ imod _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__imod__* 我们可以得到数组中的每个元素都是用二进制运算符操作的，即 mod(%)。请记住，我们可以在数组中使用任何类型的值，mod 的值将作为 MaskedArray 中的参数应用。__imod__()方法。

> **语法:** numpy.MaskedArray.__imod__(其他)
> 
> **返回:**返回自身% =值。

**示例#1 :**
在这个示例中，我们可以看到通过 MaskedArray 传递的值。__imod__()方法用于对数组的每个元素执行 mod 操作。

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2.5, 3, 7, 5]) 

# applying MaskedArray.__imod__() method 
print(gfg.__imod__(2)) 
```

**Output:**

```py
[1.0 0.5 1.0 1.0 1.0]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[14, 22, 31, 47, 54], 
                [64, 53.5, 44, 36, 21]]) 

# applying MaskedArray.__imod__() method 
print(gfg.__imod__(5)) 
```

**Output:**

```py
[[4.0 2.0 1.0 2.0 4.0]
 [4.0 3.5 4.0 1.0 1.0]]

```