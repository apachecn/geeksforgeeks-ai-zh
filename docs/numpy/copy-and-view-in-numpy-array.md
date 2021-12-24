# 在 NumPy 数组中复制和查看

> 原文:[https://www.geeksforgeeks.org/copy-and-view-in-numpy-array/](https://www.geeksforgeeks.org/copy-and-view-in-numpy-array/)

在使用 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 时，您可能已经看到一些函数返回副本，而一些函数返回视图。拷贝和视图的主要区别在于拷贝是新阵列，而视图是原始阵列的视图。换句话说，可以说副本物理存储在另一个位置，视图与原始阵列具有相同的内存位置。

**无复制:**正常分配不会复制数组对象。相反，它使用与原始数组完全相同的 id 来访问它。此外，任何一方的变化都会反映到另一方身上。

**Example:** (No Copy by Assigning)

```
import numpy as np

# creating array
arr = np.array([2, 4, 6, 8, 10])

# assigning arr to nc
nc = arr

# both arr and nc have same id
print("id of arr", id(arr))
print("id of nc", id(nc))

# updating nc
nc[0]= 12

# printing the values
print("original array- ", arr)
print("assigned array- ", nc)
```

**输出:**

```
id of arr 26558736
id of nc 26558736
original array-  [12  4  6  8 10]
assigned array-  [12  4  6  8 10]

```

**查看:**这也叫浅抄。视图只是原始数组的视图，视图不拥有数据。当我们更改视图时，它会影响原始数组，当我们更改原始数组时，它会影响视图。

**示例:**(制作视图并更改原始数组)

```
import numpy as np

# creating array
arr = np.array([2, 4, 6, 8, 10])

# creating view 
v = arr.view()

# both arr and v have different id
print("id of arr", id(arr))
print("id of v", id(v))

# changing original array
# will effect view
arr[0] = 12

# printing array and view
print("original array- ", arr)
print("view- ", v)
```

```
id of arr 30480448
id of v 30677968
original array-  [12  4  6  8 10]
view-  [12  4  6  8 10]

```

**副本:**这也称为深度副本。拷贝是一个全新的阵列，拷贝拥有数据。当我们对副本进行更改时，它不会影响原始阵列，而当对原始阵列进行更改时，它不会影响副本。

**示例:**(制作副本并更改原始数组)

```
import numpy as np

# creating array
arr = np.array([2, 4, 6, 8, 10])

# creating copy of array
c = arr.copy()

# both arr and c have different id
print("id of arr", id(arr))
print("id of c", id(c))

# changing original array
# this will not effect copy
arr[0] = 12

# printing array and copy
print("original array- ", arr)
print("copy- ", c)
```

**输出:**

```
id of arr 35406048
id of c 32095936
original array-  [12  4  6  8 10]
copy-  [ 2  4  6  8 10]

```

**数组拥有它的数据:**
要检查数组是否在视图和副本中拥有它的数据，我们可以使用每个 NumPy 数组都有属性 **base** ，如果数组拥有数据，该属性将返回 **None** 。否则，基本属性指的是原始对象。
**示例:**

```
import numpy as np

# creating array
arr = np.array([2, 4, 6, 8, 10])

# creating copy of array
c = arr.copy()

# creating view of array
v = arr.view()

# printing base attribute of copy and view
print(c.base)
print(v.base)
```