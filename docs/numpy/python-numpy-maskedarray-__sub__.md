# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ sub _ _

> 原文:[https://www . geeksforgeeks . org/python-numpy-masked array-_ _ sub _ _/](https://www.geeksforgeeks.org/python-numpy-maskedarray-__sub__/)

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__sub__* 我们可以减去一个特定的值，该值在 MaskedArray 中作为参数提供。__sub__()方法。数值将从 numpy 数组中的每个元素中减去。

> **语法:** numpy.MaskedArray.__sub__
> 
> **返回:**从自身减去他人，返回一个新的屏蔽数组。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都被减去了方法 MaskedArray 中作为参数给出的值。__sub__()。记住一件事，它对双类型值不起作用。

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([11, 22, 23, 24, 25]) 

# applying MaskedArray.__sub__() method 
print(gfg.__sub__(5)) 
```

**Output:**

```py
[ 6 17 18 19 20]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[21, 22, 23, 24, 25], 
                [26, 25, 24, 23, 22]]) 

# applying MaskedArray.__sub__() method 
print(gfg.__sub__(5)) 
```

**Output:**

```py
[[16 17 18 19 20]
 [21 20 19 18 17]]

```