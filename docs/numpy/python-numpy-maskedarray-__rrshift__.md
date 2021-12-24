# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array _ _/t1]

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__rrshift__* 方法我们可以得到右移了参数值的元素。

> **语法:**num py . masked array . _ _ _ _ _ _ _ _
> 
> **返回:**返回值> >自我。

**示例#1 :**
在这个示例中，我们可以看到每个元素都被作为参数传递的值右移了。

```py

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__rrshift__() method 
print(gfg.__rrshift__(3)) 
```

**Output:**

```py
[1 0 0 0 0]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__rrshift__() method 
print(gfg.__rrshift__(4)) 
```

**Output:**

```py
[[2 1 0 0 0]
 [0 0 0 0 1]]

```