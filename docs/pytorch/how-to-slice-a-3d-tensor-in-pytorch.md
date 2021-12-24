# 如何在 Pytorch 中切片 3D 张量？

> 原文:[https://www . geesforgeks . org/如何切片-a-3d-tensor-in-pytorch/](https://www.geeksforgeeks.org/how-to-slice-a-3d-tensor-in-pytorch/)

在本文中，我们将讨论如何在 Pytorch 中切片三维张量。

让我们创建一个三维张量进行演示。我们可以使用 torch.tensor()函数创建一个向量

> **语法:** torch.tensor([value1，value2，。值 n])

**代码:**

## 蟒蛇 3

```
# import torch module
import torch

# create an 3 D tensor with 8 elements each
a = torch.tensor([[[1, 2, 3, 4, 5, 6, 7, 8],
                   [10, 11, 12, 13, 14, 15, 16, 17]],

                  [[71, 72, 73, 74, 75, 76, 77, 78],
                   [81, 82, 83, 84, 85, 86, 87, 88]]])

# display actual  tensor
print(a)
```

**输出:**

```
tensor([[[ 1,  2,  3,  4,  5,  6,  7,  8],
        [10, 11, 12, 13, 14, 15, 16, 17]],
       [[71, 72, 73, 74, 75, 76, 77, 78],
        [81, 82, 83, 84, 85, 86, 87, 88]]])
```

### 切片三维张量

**切片:**切片是指通过使用“:”切片操作符选择张量中存在的元素。我们可以通过使用特定元素的索引来分割元素。

**注意:**索引从 0 开始

> **语法:**张量【张量 _ 位置 _ 开始:张量 _ 位置 _ 结束，张量 _ 维度 _ 开始:张量 _ 维度 _ 结束，张量 _ 值 _ 开始:张量 _ 值 _ 结束】
> 
> **参数:**
> 
> *   **张量 _ 位置 _ 开始:**指定开始迭代的张量
> *   **张量 _ 位置 _ 结束:**指定停止迭代的张量
> *   **张量 _ 维度 _ 开始:**指定在给定位置开始张量迭代的张量
> *   **张量 _dimension_stop:** 指定在给定位置停止张量迭代的张量
> *   **张量 _value_start:** 指定张量的起始位置，以迭代维度中给定的元素
> *   **张量 _value_stop:** 指定张量的结束位置，以迭代维度中给定的元素

**示例 1:** Python 代码访问 1 维的所有张量，只得到该维的 7 个值

## 蟒蛇 3

```
# access  all the tensors of 1 
# dimension and get only 7 values 
# in that dimension
print(a[0:1, 0:1, :7])
```

**输出:**

```
tensor([[[1, 2, 3, 4, 5, 6, 7]]])
```

**例 2:** Python 代码访问所有维度的所有张量，每个维度只得到 3 个值

## 蟒蛇 3

```
# access  all the tensors of all
# dimensions and get only 3 values 
# in each dimension
print(a[0:1, 0:2, :3])
```

**输出:**

```
tensor([[[ 1,  2,  3],
        [10, 11, 12]]])
```

**示例 3:** 访问所有张量上一维的 8 个元素

## 蟒蛇 3

```
# access 8 elements in 1 dimension
# on all tensors
print(a[0:2, 1, 0:8])
```

**输出:**

```
tensor([[10, 11, 12, 13, 14, 15, 16, 17],
       [81, 82, 83, 84, 85, 86, 87, 88]])
```