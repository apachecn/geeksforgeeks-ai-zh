# py torch 中的一维张量

> 原文:[https://www . geesforgeks . org/一维张量 in-pytorch/](https://www.geeksforgeeks.org/one-dimensional-tensor-in-pytorch/)

在本文中，我们将讨论 Python 中的一维张量。我们将研究以下概念:

1.  Creation of one-dimensional tensor
2.  Elements of access tensor
3.  The size of tensor
4.  The data type of the element of tensor.
5.  Tensor view
6.  Floating point tensor

### **简介**

Pytorch 用于处理张量。张量是多维数组。PyTorch 加速了张量的科学计算，因为它具有各种内置功能。

### **矢量:**

向量是包含多种数据类型元素的一维张量。我们可以使用 PyTorch 创建向量。Pytorch 在 Python torch 模块中提供。所以我们需要导入它。

**语法** :

```py
import pytorch
```

## 一维张量的产生:

使用 ***torch.tensor()方法创建一维向量。**T3】*

**语法:**

```py
torch.tensor([element1,element2,.,element n])
```

其中元素是张量的输入元素

**示例:** Python 程序创建张量元素

T5】Python 3

```py
# importing torch module
import torch

# create one dimensional tensor with integer type elements
a = torch.tensor([10, 20, 30, 40, 50])
print(a)

# create one dimensional tensor with float type elements
b = torch.tensor([10.12, 20.56, 30.00, 40.3, 50.4])
print(b)
```

**输出:**

```py
tensor([10, 20, 30, 40, 50])
tensor([10.1200, 20.5600, 30.0000, 40.3000, 50.4000])
```

## 访问张量的元素:

我们可以使用元素的索引来访问张量向量中的元素。

**语法:**

```py
tensor_name([index])
```

其中索引是元素在张量中的位置:

*   Index starts from the first 0
*   Index starts from the last one -1

**示例:**使用索引访问元素的 Python 程序。

## 蟒 3

```py
# importing torch module
import torch

# create one dimensional tensor with integer type elements
a = torch.tensor([10, 20, 30, 40, 50])

# get 0 and 1 index elements
print(a[0], a[1])

# get 4 th index  element
print(a[4])

# get 4 index element from last
print(a[-4])

# get 2 index element from last
print(a[-2])
```

**输出:**

```py
tensor(10) tensor(20)
tensor(50)
tensor(20)
tensor(40)
```

我们可以使用**:“运算符**一次访问 n 个元素，这被称为**切片。**

**语法:**

```py
tensor([start_index:end_index])
```

其中 ***start_index*** 为起始指数， ***end_index*** 为终止指数。

**示例:** Python 程序访问多个元素。

## 蟒 3

```py
# importing torch module
import torch

# create one dimensional tensor with integer type elements
a = torch.tensor([10, 20, 30, 40, 50])

# access elements from 1 to 4
print(a[1:4])

# access from 4
print(a[4:])

# access from last
print(a[-1:])
```

**输出:**

```py
tensor([20, 30, 40])
tensor([50])
tensor([50])
```

## 张量大小:

这用于使用 ***大小()方法获取张量中的长度(元素数量)。**T3】*

**语法:**

```py
tensor.size()
```

**示例:** Python 程序获取张量大小。

## 蟒 3

```py
# importing torch module
import torch

# create one dimensional tensor integer type elements
a = torch.FloatTensor([10, 20, 30, 40, 50])

# size of tensor
print(a.size())

# create one dimensional tensor integer type elements
b = torch.FloatTensor([10, 20, 30, 40, 50, 45, 67, 43])

# size of tensor
print(b.size())
```

**输出:**

```py
torch.Size([5])
torch.Size([8])
```

## 张量元素的数据类型:

我们可以得到张量数据元素的数据类型。然后 ***dtype()*** 用来得到张量的数据类型

**语法:**

```py
tensor_vector.dtype
```

其中 ***张量 _ 向量*** 是一维张量向量。

**例:**

## 蟒 3

```py
# importing torch module
import torch

# create one dimensional tensor with integer type elements
a = torch.tensor([10, 20, 30, 40, 50])

# get data type of vector a
print(a.dtype)

# create one dimensional tensor with float type elements
b = torch.tensor([10.12, 20.56, 30.00, 40.3, 50.4])

# get data type of vector b
print(b.dtype)
```

**输出:**

```py
torch.int64
torch.float32
```

## 张量视图:

***视图()*** 用于查看二维格式即行和列的张量。我们必须指定要查看的行数和列数。

**语法:**

```py
tensor.view(no_of_rows,no_of_columns)
```

其中，

*   ***Tensor*** is an input one-dimensional tensor.
*   ***No _ of _ rows*** is the total number of rows to be viewed for this tensor.
*   ***No _ of _ columns*** is the total number of columns to be viewed for this tensor.

**示例:** Python 程序创建一个包含 10 个元素的张量，视图包含 5 行 2 列，反之亦然。

## 蟒 3

```py
# importing torch module
import torch

# create one dimensional tensor 10 elements
a = torch.FloatTensor([10, 20, 30, 40, 50, 1, 2, 3, 4, 5])

# view tensor in 5 rows and 2 columns
print(a.view(5, 2))

# view tensor in 2 rows and 5 columns
print(a.view(2, 5))
```

**输出:**

```py
tensor([[10., 20.],
       [30., 40.],
       [50.,  1.],
       [ 2.,  3.],
       [ 4.,  5.]])
tensor([[10., 20., 30., 40., 50.],
       [ 1.,  2.,  3.,  4.,  5.]])
```

## 浮点张量:

这个张量用于定义浮点类型的元素。我们可以通过使用*floating Tensor*属性，使用整数元素创建浮点张量。

**语法** :

```py
torch.FloatTensor([element1,element 2,.,element n])
```

**示例:** Python 程序创建浮点张量并获取元素。

## 蟒 3

```py
# importing torch module
import torch

# create one dimensional Float Tensor  with 
# integer type elements
a = torch.FloatTensor([10, 20, 30, 40, 50])

# display data type
print(a.dtype)

# access elements from 0 to 3
print(a[0:3])

# access from 4
print(a[4:])
```

**输出:**

```py
torch.float32
tensor([10., 20., 30.])
tensor([50.])
```