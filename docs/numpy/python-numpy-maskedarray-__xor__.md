# Python | Numpy MaskedArray。_ _ _ _ _ _ _ _ xorg _ _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ xorg _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__xor__* 方法我们可以通过作为参数提供的值得到 **XOR** 的元素。

> **语法:**numpy . maskedArray . _ _ xor _ _($ self，value，/)
> 
> **返回:**返回 self^value.

**示例#1 :**
在这个示例中，我们可以看到每个元素都与作为参数传递的值**异或**。

```

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__xor__() method 
print(gfg.__xor__(2)) 
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

# applying MaskedArray.__xor__() method 
print(gfg.__xor__(1)) 
```

**Output:**

```
[[0 3 2 5 4]
 [7 4 5 2 3]]

```