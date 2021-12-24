# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ _ 年 _ _ _ _ 月 _ _ _ _ 日〔t1〕

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ _ _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__ior__* 我们可以通过在 MaskedArray 中作为参数提供的值来获取 or 元素。__ior__()方法。

> **语法:**numpy . maskedArray . _ _ ior _ _($ self，value，/)
> 
> **返回:**返回自身| =值。

**示例#1 :**
在这个示例中，我们可以看到，每个元素都通过在 MaskedArray 中作为参数传递的值进行 OR 运算。__ior__()方法。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__ior__() method 
print(gfg.__ior__(2)) 

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

# applying MaskedArray.__ior__() method 
print(gfg.__ior__(1)) 
```

**Output:**

```
[[1 3 3 5 5]
 [7 5 5 3 3]]

```