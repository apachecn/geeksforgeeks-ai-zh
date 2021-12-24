# python \ numpy 掩码数组。-= ytet-伊甸园字幕组=-翻译

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ true div _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__truediv__* 我们可以划分一个特定的值，该值在 MaskedArray 中作为参数提供。__truediv__()方法。

> **语法:**num py . masked array . _ _ _ true div _ _
> 
> **返回:**将他人分割成自己，返回一个新的屏蔽数组。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用 MaskedArray 方法中作为参数给出的值进行了划分。__truediv__()。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([22, 33.7, 44.5, 55, 77]) 

# applying MaskedArray.__truediv__() method 
print(gfg.__truediv__(11)) 
```

**Output:**

```
[2.0 3.063636363636364 4.045454545454546 5.0 7.0]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[10, 20, 30, 40, 50], 
                [11, 22, 33, 44, 55]]) 

# applying MaskedArray.__truediv__() method 
print(gfg.__truediv__(5)) 
```

**Output:**

```
[[2.0 4.0 6.0 8.0 10.0]
 [2.2 4.4 6.6 8.8 11.0]]

```