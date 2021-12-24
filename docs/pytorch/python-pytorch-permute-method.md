# Python–Pytorch permute()方法

> 原文:[https://www . geesforgeks . org/python-py torch-permute-method/](https://www.geeksforgeeks.org/python-pytorch-permute-method/)

PyTorch **torch.permute()** 根据所需的排序重新排列原始张量，并返回一个新的多维旋转张量。返回张量的大小与原始张量的大小相同。

> **语法:** torch.permute(*dims)
> 
> **参数:**
> 
> *   **dims:** 张量维度的期望排序中的索引序列(索引从零开始)。
> 
> **返回:**具有所需维度顺序的张量。

让我们借助几个例子来看看这个概念:

**示例 1:** 创建大小为 2 × 4 的二维张量，然后进行置换。

## 蟒蛇 3

```py
# import pytorch library
import torch

# create a tensor of size 2 x 4
input_var = torch.randn(2,4)

# print size
print(input_var.size())

print(input_var)

# dimensions permuted
input_var = input_var.permute(1, 0)

# print size
print(input_var.size())

print(input_var)
```

**输出:**

```py
torch.Size([2, 4])
tensor([[ 0.9801,  0.5296,  0.5449, -1.1481],
        [-0.6762, -0.1161,  0.6360, -0.5371]])
torch.Size([4, 2])
tensor([[ 0.9801, -0.6762],
        [ 0.5296, -0.1161],
        [ 0.5449,  0.6360],
        [-1.1481, -0.5371]])
```

**示例 2:** 创建大小为 3 × 5 × 2 的三维张量，然后进行置换。

## 蟒蛇 3

```py
# import pytorch library
import torch

# creating a tensor with random 
# values of dimension 3 X 5 X 2
input_var = torch.randn(3, 5, 2)

# print size
print(input_var.size())

print(input_var)

# dimensions permuted
input_var = input_var.permute(2, 0, 1)

# print size
print(input_var.size())

print(input_var)
```

**输出:**

```py
torch.Size([3, 5, 2])
tensor([[[ 0.2059, -0.7165],
         [-1.1305,  0.5886],
         [-0.1247, -0.4969],
         [-0.5788,  0.0159],
         [ 1.4304,  0.6014]],

        [[ 2.4882, -0.3910],
         [-0.5558,  0.6903],
         [-0.4219, -0.5498],
         [-0.5346, -0.0703],
         [ 1.1497, -0.3252]],

        [[-0.5075,  0.5752],
         [ 1.3738, -0.3321],
         [-0.3317, -0.9209],
         [-1.6677, -1.1471],
         [-0.9269, -0.6493]]])
torch.Size([2, 3, 5])
tensor([[[ 0.2059, -1.1305, -0.1247, -0.5788,  1.4304],
         [ 2.4882, -0.5558, -0.4219, -0.5346,  1.1497],
         [-0.5075,  1.3738, -0.3317, -1.6677, -0.9269]],

        [[-0.7165,  0.5886, -0.4969,  0.0159,  0.6014],
         [-0.3910,  0.6903, -0.5498, -0.0703, -0.3252],
         [ 0.5752, -0.3321, -0.9209, -1.1471, -0.6493]]])

```