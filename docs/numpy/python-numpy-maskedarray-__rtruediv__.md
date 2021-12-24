# Python | Numpy MaskedArray。_ _ _ _ _ 巨噬细胞 __

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array _ _/t1]

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__rtruediv__* 我们可以划分一个特定的值，该值在 MaskedArray 中作为参数提供。__rtruediv__()方法。

> **语法:**num py . masked array . _ _ _ rtruediv _ _
> 
> **返回:**将自己分割成他人，返回一个新的屏蔽阵。

**示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都用 MaskedArray 方法中作为参数给出的值进行了划分。__rtruediv__()。

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([22, 33, 44, 55, 77]) 

# applying MaskedArray.__rtruediv__() method 
print(gfg.__rtruediv__(11)) 
```

**Output:**

```py
[0.5 0.3333333333333333 0.25 0.2 0.14285714285714285]

```

**例 2:**

```py
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[10, 20, 30, 40, 50], 
                [110, 220, 330, 440, 550]]) 

# applying MaskedArray.__rtruediv__() method 
print(gfg.__rtruediv__(10)) 
```

**Output:**

```py
[[1.0 0.5 0.3333333333333333 0.25 0.2]
 [0.09090909090909091 0.045454545454545456 0.030303030303030304
  0.022727272727272728 0.01818181818181818]]

```