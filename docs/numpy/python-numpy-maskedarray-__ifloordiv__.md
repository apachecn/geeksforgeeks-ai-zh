# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ _ ifordiv _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array _ _/t1]

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__ifloordiv__* 我们可以获得特定值的楼层划分，该值在 MaskedArray 中作为参数提供。__ifloordiv__()方法。

> **语法:**numpy . maskedArray . _ _ ifloordiv _ _(其他)
> 
> **返回:**楼层自己除以其他原地。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用 MaskedArray 方法中作为参数给出的值进行了划分。__ifloordiv__()。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([10, 20.5, 30, 4.8, 50]) 

# applying MaskedArray.__ifloordiv__() method 
print(gfg.__ifloordiv__(2)) 
```

**Output:**

```
[  5\.  10\.  15\.   2\.  25.]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[10, 20, 30, 4.45, 50], 
                [6, 5.5, 4, 3, 2.62]]) 

# applying MaskedArray.__ifloordiv__() method 
print(gfg.__ifloordiv__(5)) 
```

**Output:**

```
[[  2\.   4\.   6\.   0\.  10.]
 [  1\.   1\.   0\.   0\.   0.]]

```