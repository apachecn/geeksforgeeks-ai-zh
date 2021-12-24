# Python | Numpy MaskedArray。_ _ _ _ _ 免疫 __

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ immol _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__imul__* 我们可以将 MaskedArray 中作为参数提供的特定值相乘。__imul__()方法。数值将乘以 numpy 数组中的每个元素。

> **语法:** numpy.MaskedArray.__imul__(其他)
> 
> **返回:**将自身乘以其他原地。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都与方法 MaskedArray 中作为参数给出的值相乘。__imul__()。记住一件事，它对双类型值不起作用。

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4.7, 5.2]) 

# applying MaskedArray.__imul__() method 
print(gfg.__imul__(5)) 
```

**Output:**

```py
[  5\.   10\.   15\.   23.5  26\. ]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__imul__() method 
print(gfg.__imul__(5)) 
```

**Output:**

```py
[[ 5 10 15 20 25]
 [30 25 20 15 10]]

```