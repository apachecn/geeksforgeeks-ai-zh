# Python | Numpy MaskedArray。_ _ _ _ ABS _

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-masked array-_ _ ABS _/

`**numpy.ma.MaskedArray class**`是 ndarray 的一个子类，设计用于处理缺少数据的数值数组。借助 Numpy *MaskedArray。__abs__* 运算符我们可以找到数组中每个元素的绝对值。假设我们有一个值 31.74，在 MaskedArray 的帮助下。__abs__()它将被转换为 31。

> **语法:**num py . masked array . _ _ _ _ _ _ _ _
> 
> **返回:**楼层(自)

**示例#1 :**
在这个示例中，我们可以看到在应用 MaskedArray 之后。__abs__()，我们得到一个简单的数组，它可以包含一个数组中所有元素的绝对值。

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.array([1.45, 2.32, 3.98, 4.41, 5.55, 6.12]) 

# applying MaskedArray.____() method 
print(np.ma.MaskedArray.__abs__(gfg)) 
```

**Output:**

```
[ 1  2  3  4  5  6]

```

**例 2:**

```
# import the important module in python 
import numpy as np 

# make an array with numpy 
gfg = np.array([[1.22, 2.25, -3.21, 4.45, 5.56, 6], 
                [-6.65, 5.55, 4.32, 3.33, 2.12, -1.05]]) 

# applying MaskedArray.__abs__() method 
print(np.ma.MaskedArray.__abs__(gfg)) 
```

**Output:**

```
[[ 1  2  3  4  5  6 ]
 [ 6  5  4  3  2  1]]

```