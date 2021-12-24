# Python | Numpy MaskedArray。_ _ _ _ _ error _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ error _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__ror__* 方法我们可以用作为参数提供的值获得元素**或**。

> **语法:**num py . masked array . _ _ _ error _ _
> 
> **返回:**返回值|自我。

**示例#1 :**
在这个示例中，我们可以看到每个元素都是**或**，其值作为参数传递。

```

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__ror__() method 
print(gfg.__ror__(2)) 
```

**Output:**

```
[3 2 3 6 7]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__ror__() method 
print(gfg.__ror__(1)) 
```

**Output:**

```
[[1 3 3 5 5]
 [7 5 5 3 3]]

```