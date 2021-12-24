# Python | Numpy MaskedArray。_ _ _ _ _ rlshift _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ rlshift _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__rlshift__* 方法我们可以得到被作为参数提供的值右移的元素。

> **语法:**num py . masked array . _ _ _ _ _ rlshift _ _
> 
> **返回:**返回值< <自我。

**示例#1 :**
在这个示例中，我们可以看到每个元素都被作为参数传递的值右移了。

```

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__rlshift__() method 
print(gfg.__rlshift__(2)) 
```

**Output:**

```
[ 4  8 16 32 64]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__rlshift__() method 
print(gfg.__rlshift__(1)) 
```

**Output:**

```
[[ 2  4  8 16 32]
 [64 32 16  8  4]]

```