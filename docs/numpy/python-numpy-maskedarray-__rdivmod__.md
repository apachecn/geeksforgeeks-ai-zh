# Python | Numpy MaskedArray。_ _ _ _ _ rdivmod _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ rdivmod _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__rdivmod__* 我们将得到两个数组，一个数组的元素除以 numpy.ma.__rdivmod__()方法中提供的值，第二个数组的元素执行 mod 运算，其值与 numpy.ma.__rdivmod__()方法中提供的值相同。

> **语法**numpy . mask array。_ _ rdimm _
> 
> **返回:**返回 divmod(值，自身)。

**示例#1 :**
在这个示例中，我们可以通过使用 MaskedArray 看到这一点。__rdivmod__()方法我们得到两个数组。一个是用作为参数传递的值除以，另一个是用 mod 值。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([1, 2, 3, 4, 5]) 

# applying MaskedArray.__rdivmod__() method 
print(gfg.__rdivmod__(3)) 
```

**Output:**

```
(masked_array(data = [3 1 1 0 0],
             mask = [False False False False False],
       fill_value = 999999), masked_array(data = [0 1 0 3 3],
             mask = [False False False False False],
       fill_value = 999999)
)

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.ma.array([[1, 2, 3, 4, 5], 
                [6, 5, 4, 3, 2]]) 

# applying MaskedArray.__rdivmod__() method 
print(gfg.__rdivmod__(3)) 
```

**Output:**

```
(masked_array(data =
 [[3 1 1 0 0]
 [0 0 0 1 1]],
             mask =
 [[False False False False False]
 [False False False False False]],
       fill_value = 999999), masked_array(data =
 [[0 1 0 3 3]
 [3 3 3 0 1]],
             mask =
 [[False False False False False]
 [False False False False False]],
       fill_value = 999999)
)

```