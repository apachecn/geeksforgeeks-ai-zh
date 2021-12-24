# Python | Numpy MaskedArray。_ _ _ _ _ mul _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ mul _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__mul__* 我们可以乘以一个特定的值，该值在 MaskedArray 中作为参数提供。__mul__()方法。

> **语法:**num py . masked array . _ _ _ _ _ _ _ _
> 
> **返回:**将自身乘以其他，返回一个新的屏蔽数组。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都与方法 MaskedArray 中作为参数给出的值相乘。__mul__()。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__mul__() method 
print(gfg.__mul__(5)) 
```

**Output:**

```
[ 5 10 15 20 25]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__mul__() method 
print(gfg.__mul__(5)) 
```

**Output:**

```
[[ 5 10 15 20 25]
 [30 25 20 15 10]]

```