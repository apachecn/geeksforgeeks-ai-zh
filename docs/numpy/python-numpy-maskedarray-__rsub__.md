# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ _ rsub _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ rsub _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__rsub__* 我们可以减去一个特定的值，该值在 MaskedArray 中作为参数提供。__rsub__()方法。数值将从 numpy 数组中的每个元素中减去。

> **语法:**num py . masked array . _ _ _ rsub _ _
> 
> **返回:**从其他中减去自己，返回一个新的屏蔽数组。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都被减去了方法 MaskedArray 中作为参数给出的值。__rsub__()。记住一件事，它对双类型值不起作用。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([11, 22, 23, 24, 25]) 

# applying MaskedArray.__rsub__() method 
print(gfg.__rsub__(5)) 
```

**Output:**

```
[ -6 -17 -18 -19 -20]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[21, 22, 23, 24, 25], 
                [26, 25, 24, 23, 22]]) 

# applying MaskedArray.__rsub__() method 
print(gfg.__rsub__(5)) 
```

**Output:**

```
[[-16 -17 -18 -19 -20]
 [-21 -20 -19 -18 -17]]

```