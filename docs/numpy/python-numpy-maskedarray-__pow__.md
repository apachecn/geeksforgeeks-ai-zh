# Python | Numpy MaskedArray。_ _ _ _ _ pow _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ pow _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__pow__* 方法我们可以使用作为参数提供的值为元素供电。

> **语法:** numpy.MaskedArray.__pow__
> 
> **回归:**提升自我，给对方力量，掩盖潜在的南斯。

**示例#1 :**
在这个示例中，我们可以看到在应用 MaskedArray 之后。__pow__()，我们可以看到每个元素都使用作为参数提供的值来供电。

```py

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__pow__() method 
print(gfg.__pow__(3)) 
```

**Output:**

```py
[  1   8  27  64 125]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__pow__() method 
print(gfg.__pow__(2)) 
```

**Output:**

```py
[[ 1  4  9 16 25]
 [36 25 16  9  4]]

```