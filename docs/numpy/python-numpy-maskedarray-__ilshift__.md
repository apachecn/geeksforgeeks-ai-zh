# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ ilshift _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__ilshift__* 我们可以通过 MaskedArray 中作为参数提供的值来获得左移的元素。__ilshift__()方法。

> **语法:**numpy . maskedArray . _ _ ilshift _ _(其他)
> 
> **回归:**回归自我< < =值。

**示例#1 :**
在这个示例中，我们可以看到每个元素都被作为参数在 MaskedArray 中传递的值右移。__ilshift__()方法。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__ilshift__() method 
print(gfg.__ilshift__(2)) 
```

**Output:**

```
[ 4  8 12 16 20]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__ilshift__() method 
print(gfg.__ilshift__(1)) 
```

**Output:**

```
[[ 2  4  6  8 10]
 [12 10  8  6  4]]

```