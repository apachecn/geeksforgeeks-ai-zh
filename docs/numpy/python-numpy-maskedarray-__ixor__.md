# Python | Numpy MaskedArray。_ _ _ _ _ ixor _(

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ ixor _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__ixor__* 我们可以通过掩码数组中作为参数提供的值得到异或运算的元素。__ixor__()方法。

> **语法:**numpy . maskedArray . _ _ ixor _ _($ self，value，/)
> 
> **返回:**返回 self^=value.

**示例#1 :**
在这个示例中，我们可以看到每个元素都通过在 MaskedArray 中作为参数传递的值进行异或运算。__ixor__()方法。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__ixor__() method 
print(gfg.__ixor__(2)) 

```

**Output:**

```
[3 0 1 6 7]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__ixor__() method 
print(gfg.__ixor__(1)) 
```

**Output:**

```
[[0 3 2 5 4]
 [7 4 5 2 3]]

```