# python \ numpy 掩码数组。_ _ rxor _

的缩写形式

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array _ _/t1]

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__rxor__* 方法我们可以得到**与作为参数提供的值进行异或**的元素。

> **语法:**numpy . maskearray . _ _ rxor _ _($ self，value，/)
> 
> **返回:**返回 value^self.

**示例#1 :**
在这个示例中，我们可以看到每个元素都与作为参数传递的值**异或**。

```

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__rxor__() method 
print(gfg.__rxor__(2)) 
```

**Output:**

```
[3 0 1 6 7]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__rxor__() method 
print(gfg.__rxor__(1)) 
```

**Output:**

```
[[0 3 2 5 4]
 [7 4 5 2 3]]

```