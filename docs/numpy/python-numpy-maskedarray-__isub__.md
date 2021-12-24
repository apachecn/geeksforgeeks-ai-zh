# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ _ isb _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ _ _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__isub__* 我们可以减去一个特定的值，该值在 MaskedArray 中作为参数提供。__isub__()方法。numpy 数组中的每个元素都将减去值。

> **语法:** numpy.MaskedArray.__isub__(其他)
> 
> **返回:**原地减去其他到自己。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都被减去了方法 MaskedArray 中作为参数给出的值。__isub__()。记住一件事，它对双类型值不起作用。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4.7, 5.2]) 

# applying MaskedArray.__isub__() method 
print(gfg.__isub__(5)) 
```

**Output:**

```
[-4\.  -3\.  -2\.  -0.3  0.2]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__isub__() method 
print(gfg.__isub__(5)) 
```

**Output:**

```
[[-4 -3 -2 -1  0]
 [ 1  0 -1 -2 -3]]

```