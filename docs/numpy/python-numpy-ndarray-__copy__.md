# python | num py ndaarray。_ _ _ copy _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ _ _ _ copy _/

借助`**Numpy ndarray.__copy__()**`方法，我们可以复制 **numpy 数组**中存在的所有数据元素。如果更改副本中的任何数据元素，将不会影响原始 numpy 数组。

> 语法:`numpy.__copy__()`
> 
> 返回:所有数据元素的副本

**示例#1 :**
在这个示例中，我们可以看到借助于`numpy.__copy__()`方法，我们正在复制一个元素。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__copy__() method
geeks = gfg.__copy__()

print(geeks)
```

**Output:**

```
[1 2 3 4 5]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__copy__() method
geeks = gfg.__copy__()

# Change the data element
geeks[0][2] = 10

print(gfg, end ='\n\n')
print(geeks)
```

**Output:**

```
[[1 2 3 4 5]
 [6 5 4 3 2]]

[[ 1  2 10  4  5]
 [ 6  5  4  3  2]]

```