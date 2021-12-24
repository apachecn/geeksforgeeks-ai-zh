# Python | Numpy MaskedArray。_ _ _ _ _ radd _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ radd _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__radd__* 我们可以添加一个特定的值，该值在 MaskedArray 中作为参数提供。__radd__()方法。数值将被添加到 numpy 数组中的每个元素。

> **语法:**num py . masked array . _ _ _ _ _ _ _ _
> 
> **返回:**将自己加到其他，返回一个新的屏蔽数组。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都添加了方法 MaskedArray 中作为参数给出的值。__radd__()。记住一件事，它对双类型值不起作用。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__radd__() method 
print(gfg.__radd__(5)) 
```

**Output:**

```
[ 6  7  8  9 10]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__radd__() method 
print(gfg.__radd__(5)) 
```

**Output:**

```
[[ 6  7  8  9 10]
 [11 10  9  8  7]]

```