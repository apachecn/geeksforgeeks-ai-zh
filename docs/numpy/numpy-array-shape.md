# NumPy 阵列形状

> 原文:[https://www.geeksforgeeks.org/numpy-array-shape/](https://www.geeksforgeeks.org/numpy-array-shape/)

数组的形状可以定义为每个维度中的元素数量。Dimension 是索引或下标的数量，我们需要它来指定数组中的一个元素。

## **如何得到数组的形状？**

在 NumPy 中，我们将使用一个名为 shape 的属性，它返回一个元组，元组的元素给出相应数组维度的长度。

> **语法:**numpy . shape(Array _ name)
> **参数:**数组作为参数传递。
> **返回:**一个元组，其元素给出相应数组维度的长度。

**例 1:** (打印多维数组的形状)

## 蟒蛇 3

```py
import numpy as npy

# creating a 2-d array
arr1 = npy.array([[1, 3, 5, 7], [2, 4, 6, 8]])

# creating a 3-d array
arr2 = npy.array([[1, 3, 5, 7], [2, 4, 6, 8], 
                  [3, 6, 9, 12]])

# printing the shape of arrays
# first element of tuple gives 
# dimension of arrays second 
# element of tuple gives number 
# of element of each dimension
print(arr1.shape)
print(arr2.shape)
```

**输出:**

```py
(2, 4)
(3, 4)

```

上面的示例返回(2，4)和(3，4)，这意味着 arr1 有 2 个维度，每个维度有 4 个元素。类似地，arr2 有 3 个维度，每个维度有 4 个元素。

**示例 2:** (使用值为 2、4、6、8、10 的向量使用 ndmin 创建数组，并验证最后一个维度的值)

## 蟒蛇 3

```py
import numpy as npy

# creating an array of 6 dimension
# using ndim
arr = npy.array([2, 4, 6, 8, 10], ndmin=6)

# printing array
print(arr)

# verifying the value of last dimension
# as 5
print('shape of an array :', arr.shape)
```

**输出:**

```py
[[[[[[ 2  4  6  8 10]]]]]]
shape of an array : (1, 1, 1, 1, 1, 5)

```

在上面的例子中，我们验证了维度的最后一个值为 5。