# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ ipow _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ ipow _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__ipow__* 我们可以使用 MaskedArray 中作为参数提供的值为所有元素供电。__ipow__()方法。

> **语法:** numpy.MaskedArray.__ipow__(其他)
> 
> **返回:**将自己提升到另一个力量，就位。

**示例#1 :**
在这个示例中，我们可以看到每个元素都使用 MaskedArray 中作为参数提供的值来供电。__ipow__()方法。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__ipow__() method 
print(gfg.__ipow__(3)) 
```

**Output:**

```
[  1   8  27  64 125]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__ipow__() method 
print(gfg.__ipow__(2)) 
```

**Output:**

```
[[ 1  4  9 16 25]
 [36 25 16  9  4]]

```