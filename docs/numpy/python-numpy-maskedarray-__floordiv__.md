# Python | Numpy MaskedArray。——《洪水》_

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ flood rdiv _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__floordiv__* 运算符我们可以对作为参数提供给该函数的特定值进行除法运算。

> **语法:**num py . masked array . _ _ _ flood v _ _
> 
> **返回:**将他人分割成自己，返回一个新的屏蔽数组。

**示例#1 :**
在这个示例中，我们可以看到在应用 MaskedArray 之后。__floordiv__()，我们得到了数组中被划分的每个元素的 floor 值。此方法对于数组的正、负和浮点值都很有效。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2.5, 3, 4.8, 5]) 

# applying MaskedArray.__floordiv__() method 
print(gfg.__floordiv__(2)) 
```

**Output:**

```
[0.0 1.0 1.0 2.0 2.0]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4.45, 5], 
                [6, 5.5, 4, 3, 2.62]]) 

# applying MaskedArray.__floordiv__() method 
print(gfg.__floordiv__(3)) 
```

**Output:**

```
[[0.0 0.0 1.0 1.0 1.0]
 [2.0 1.0 1.0 1.0 0.0]]

```