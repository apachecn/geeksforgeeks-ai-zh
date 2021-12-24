# 如何获取 Pytorch 张量的数据类型？

> 原文:[https://www . geeksforgeeks . org/如何获取数据类型的 pytorch-tensor/](https://www.geeksforgeeks.org/how-to-get-the-data-type-of-a-pytorch-tensor/)

在本文中，我们将创建一个张量并获取数据类型。Pytorch 用于处理张量。张量是多维数组。PyTorch 加速了张量的科学计算，因为它具有各种内置功能。

### **矢量:**

向量是包含多种数据类型元素的一维张量。我们可以使用 PyTorch 创建一个向量。Python torch 模块中有 Pytorch，所以我们需要导入它

**语法:**

```py
import pytorch
```

### 一维张量的产生:

使用 **torch.tensor()方法创建一维向量。**

**语法:**

```py
torch.tensor([element1,element2,.,element n],dtype)
```

**参数:**

*   **数据类型:**指定数据类型。

```py
dtype=torch.datatype
```

**示例:** Python 程序创建未指定数据类型的张量元素。

## 蟒蛇 3

```py
# importing torch module
import torch

# create one dimensional tensor with
# integer type elements
a = torch.tensor([10, 20, 30, 40, 50])
print(a)

# create one dimensional tensor with 
# float type elements
b = torch.tensor([10.12, 20.56, 30.00, 40.3, 50.4])
print(b)
```

**输出:**

```py
tensor([10, 20, 30, 40, 50])
tensor([10.1200, 20.5600, 30.0000, 40.3000, 50.4000])
```

### **支持的数据类型:**

vector 支持以下数据类型:

<figure class="table">

| **数据类型** | **描述** |
| --- | --- |
| int8 | 8 字节整数类型 |
| uint8 | 8 字节的无符号整数类型 |
| int16 | 16 字节的整数类型 |
| int32 | 32 字节的整数类型 |
| int64 | 64 字节的整数类型 |
| 漂浮物 | 浮点型数据(十进制) |
| 两倍 | 浮点型(64 位)十进制数据 |
| 弯曲件 | 布尔类型:如果值大于 0，则返回真，否则返回假 |

</figure>

我们可以通过 ***dtype 命令:*** 得到数据类型

**语法:**

```py
tensor_name.dtype
```

**示例 1:** Python 程序创建整数数据类型的张量并显示数据类型

## 蟒蛇 3

```py
# import torch
import torch

# create a tensor with unsigned integer type of 8 bytes size
a = torch.tensor([100, 200, 2, 3, 4], dtype=torch.uint8)
# display tensor
print(a)
# display data type
print(a.dtype)

# create a tensor with  integer type of 8 bytes size
a = torch.tensor([1, 2, -6, -8, 0], dtype=torch.int8)

# display tensor
print(a)

# display data type
print(a.dtype)

# create a tensor with  integer type of 16 bytes size
a = torch.tensor([1, 2, -6, -8, 0], dtype=torch.int16)

# display tensor
print(a)

# display data type
print(a.dtype)

# create a tensor with  integer type of 32 bytes size
a = torch.tensor([1, 2, -6, -8, 0], dtype=torch.int32)

# display tensor
print(a)

# display data type
print(a.dtype)

# create a tensor with  integer type of 64 bytes size
a = torch.tensor([1, 2, -6, -8, 0], dtype=torch.int64)

# display tensor
print(a)

# display data type
print(a.dtype)
```

**输出:**

```py
tensor([100, 200,   2,   3,   4], dtype=torch.uint8)
torch.uint8
tensor([ 1,  2, -6, -8,  0], dtype=torch.int8)
torch.int8
tensor([ 1,  2, -6, -8,  0], dtype=torch.int16)
torch.int16
tensor([ 1,  2, -6, -8,  0], dtype=torch.int32)
torch.int32
tensor([ 1,  2, -6, -8,  0])
torch.int64
```

**示例 2:** 创建浮点类型并显示数据类型。

## 蟒蛇 3

```py
# import torch
import torch

# create a tensor with  float type
a = torch.tensor([100, 200, 2, 3, 4], dtype=torch.float)

# display tensor
print(a)

# display data type
print(a.dtype)

# create a tensor with  double type
a = torch.tensor([1, 2, -6, -8, 0], dtype=torch.double)

# display tensor
print(a)

# display data type
print(a.dtype)
```

**输出:**

```py
tensor([100., 200.,   2.,   3.,   4.])
torch.float32
tensor([ 1.,  2., -6., -8.,  0.], dtype=torch.float64)
torch.float64
```

**示例 3:** 创建布尔类型的张量

## 蟒蛇 3

```py
# import torch
import torch

# create a tensor with  bool type
a = torch.tensor([100, 200, 2, 3, 4], dtype=torch.bool)

# display tensor
print(a)

# display data type
print(a.dtype)

# create a tensor with  bool type
a = torch.tensor([0, 0, 0, 1, 2], dtype=torch.bool)

# display tensor
print(a)

# display data type
print(a.dtype)
```

**输出:**

```py
tensor([True, True, True, True, True])
torch.bool
tensor([False, False, False,  True,  True])
torch.bool
```