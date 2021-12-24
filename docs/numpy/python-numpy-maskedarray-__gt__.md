# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ gt _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ gt _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__gt__* 运算符我们可以找到数组中哪个元素大于参数中提供的值。

> **语法:**num py . masked array . _ _ _ _ _ _ _ _
> 
> **返回:**自我>值。

**示例#1 :**
在这个示例中，我们可以看到在应用 MaskedArray 之后。__gt__()，我们得到一个简单的布尔数组，它可以告诉我们数组中的哪个元素比提供的参数大。

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5, 6]) 

# applying MaskedArray.__gt__() method 
print(gfg.__gt__(4)) 
```

**Output:**

```py
[False False False False  True  True]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5, 6], 
                [6, 5, 4, 3, 2, 1]]) 

# applying MaskedArray.__gt__() method 
print(gfg.__gt__(4)) 
```

**Output:**

```py
[[False False False False  True  True]
 [ True  True False False False False]]

```