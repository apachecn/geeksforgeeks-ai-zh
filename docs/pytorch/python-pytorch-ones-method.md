# Python Pytorch one()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-ones-method/](https://www.geeksforgeeks.org/python-pytorch-ones-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。

函数`torch.ones()`返回一个由标量值 1 填充的张量，其形状由变量参数大小定义。

> **语法**:torch . one(大小，out =无)
> 
> **参数** :
> **大小**:定义输出张量形状的整数序列
> **out(张量，可选)**:输出张量
> 
> **返回类型**:标量值为 1 的张量，形状与**大小**相同。

**代码#1:**

```
# Importing the PyTorch library
import torch

# Applying the ones function and
# storing the resulting tensor in 't'
a = torch.ones([3, 4])
print("a = ", a)

b = torch.ones([1, 5])
print("b = ", b)

c = torch.ones([5, 1])
print("c = ", c)

d = torch.ones([3, 3, 2])
print("d = ", d)
```

**输出:**

```
a =  tensor([[1., 1., 1., 1.],
        [1., 1., 1., 1.],
        [1., 1., 1., 1.]])
b =  tensor([[1., 1., 1., 1., 1.]])
c =  tensor([[1.],
        [1.],
        [1.],
        [1.],
        [1.]])
d =  tensor([[[1., 1.],
         [1., 1.],
         [1., 1.]],

        [[1., 1.],
         [1., 1.],
         [1., 1.]],

        [[1., 1.],
         [1., 1.],
         [1., 1.]]])

```