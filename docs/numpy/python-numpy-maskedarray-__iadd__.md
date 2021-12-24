# Python | Numpy MaskedArray。_ _ _ _ _ iadd _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ iadd _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__iadd__* 我们可以添加一个特定的值，该值在 MaskedArray 中作为参数提供。__iadd__()方法。数值将被添加到 numpy 数组中的每个元素。

> **语法:** numpy.MaskedArray.__iadd__(其他)
> 
> **返回:**原地添加其他到自我。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都添加了方法 MaskedArray 中作为参数给出的值。__iadd__()。记住一件事，它对双类型值不起作用。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4.7, 5.2]) 

# applying MaskedArray.__iadd__() method 
print(gfg.__iadd__(5)) 
```

**Output:**

```
[  6\.    7\.    8\.    9.7  10.2]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__iadd__() method 
print(gfg.__iadd__(5)) 
```

**Output:**

```
[[ 6  7  8  9 10]
 [11 10  9  8  7]]

```