# python | num py ndaarray。_ _ _ ABS _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ ABS _/

借助`**Numpy ndarray.__abs__()**`，可以找到数组中每个元素的**绝对值**。假设我们有一个值 **1.34** ，借助`ndarray.__abs__()`它会转换成 **1** 。

> **语法:**n 数组。__abs__(自我)
> 
> **返回:**楼层(自)

**示例#1 :**
在这个示例中，我们可以看到在应用`ndarray.__abs__()`之后，我们得到了一个简单的数组，它可以包含一个数组中所有元素的绝对值。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1.45, 2.32, 3.98, 4.41, 5.55, 6.12])

# applying ndarray.____() method
print(gfg.__abs__())
```

**Output:**

```
[ 1  2  3  4  5  6]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1.22, 2.25, -3.21, 4.45, 5.56, 6],
                [-6.65, 5.55, 4.32, 3.33, 2.12, -1.05]])

# applying ndarray.__abs__() method
print(gfg.__abs__())
```

**Output:**

```
[[ 1  2  3  4  5  6 ]
 [ 6  5  4  3  2  1]]

```