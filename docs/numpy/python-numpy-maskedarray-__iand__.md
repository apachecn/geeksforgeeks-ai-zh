# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ iand _ _(

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ iand _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。_ _ and _ _*我们可以通过在 MaskedArray 中作为参数提供的值来获得 and 元素。_ _ iand _ _()方法。

> **语法:**numpy . maskedarray . _ _ and _ _($ self，value，/)
> 
> **返回:**返回自身&=值。

**示例#1 :**
在这个示例中，我们可以看到每个元素都由作为参数在 MaskedArray 中传递的值进行 and 运算。_ _ iand _ _()方法。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__iand__() method 
print(gfg.__iand__(2)) 

```

**Output:**

```
[0 2 2 0 0]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__iand__() method 
print(gfg.__iand__(1)) 
```

**Output:**

```
[[1 0 1 0 1]
 [0 1 0 1 0]]

```