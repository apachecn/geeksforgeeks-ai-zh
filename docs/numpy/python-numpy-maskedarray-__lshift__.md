# Python | Numpy MaskedArray。_ _ _ _ _ lshift _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ _ _ _ _ _ lshift _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。_ _ lsshift _ _*方法我们可以得到左移了作为参数提供的值的元素。

> **语法:**numpy . maskedArray . _ _ lsshift _ _
> 
> **返回:**返回自身< <值。

**示例#1 :**
在这个示例中，我们可以看到每个元素都被作为参数传递的值向左移动了。

```

# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__lshift__() method 
print(gfg.__lshift__(2)) 
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

# applying MaskedArray.__lshift__() method 
print(gfg.__lshift__(1)) 
```

**Output:**

```
[[ 2  4  6  8 10]
 [12 10  8  6  4]]

```