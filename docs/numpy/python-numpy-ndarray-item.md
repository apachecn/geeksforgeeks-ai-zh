# python | num py ndaarray . item()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-item/

借助`**numpy.ndarray.item()**`方法，我们可以获取 numpy 数组上给定索引处的数据元素。请记住，我们可以给出一维参数的索引，也可以是二维的。

> **参数:**
> ***参数:**参数(变量编号和类型)
> - >无:此参数仅在数组大小为 1 时有效。
> - > int_type:此参数被解释为数组中的平面索引，指定要返回哪个元素。
> ->int _ type 的元组:通过指定要返回的元素，该参数被解释为二维数组。
> 
> **返回:**物品的副本

**示例#1 :**
在这个示例中，我们可以看到通过在`ndarray.item()`方法中指定参数，我们可以拥有元素，如果它存在于这个索引上的话。

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.item() method
print(gfg.item(2))
```

**Output:**

```
3

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.item() method
print(gfg.item((1, 2)))
```

**Output:**

```
4

```