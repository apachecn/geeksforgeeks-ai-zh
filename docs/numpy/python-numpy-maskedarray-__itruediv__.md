# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ _ itru div _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array _ _/t1]

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__itruediv__* 我们可以定义一个特定的值，该值在 MaskedArray 中作为参数提供。__itruediv__()方法。

> **语法:**numpy . maskedArray . _ _ itruediv _ _(其他)
> 
> **返回:**真除自我被其他原地。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用 MaskedArray 方法中作为参数给出的值进行了划分。__itruediv__()。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2.5, 3, 4.8, 5]) 

# applying MaskedArray.__itruediv__() method 
print(gfg.__itruediv__(2)) 
```

**Output:**

```
[ 0.5   1.25  1.5   2.4   2.5 ]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4.45, 5], 
                [6, 5.5, 4, 3, 2.62]]) 

# applying MaskedArray.__itruediv__() method 
print(gfg.__itruediv__(5)) 
```

**Output:**

```
[[ 0.2    0.4    0.6    0.89   1\.   ]
 [ 1.2    1.1    0.8    0.6    0.524]]

```