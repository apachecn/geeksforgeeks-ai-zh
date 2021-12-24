# Python PyTorch zeross()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-zeros-method/](https://www.geeksforgeeks.org/python-pytorch-zeros-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。

函数`torch.zeros()`返回一个由标量值 0 填充的张量，其形状由变量参数大小定义。

> **语法**:torch . zero(大小，out =无)
> 
> **参数** :
> **大小**:定义输出张量形状的整数序列
> **out(张量，可选)**:输出张量
> 
> **返回类型**:标量值为 0 的张量，形状与**大小**相同。

**代码#1:**

```
# Importing the PyTorch library
import torch

# Applying the zeros function and
# storing the resulting tensor in 't'
a = torch.zeros([3, 4])
print("a = ", a)

b = torch.zeros([1, 5])
print("b = ", b)

c = torch.zeros([5, 1])
print("c = ", c)

d = torch.zeros([3, 3, 2])
print("d = ", d)
```

**输出:**

```
a =  tensor([[0., 0., 0., 0.],
        [0., 0., 0., 0.],
        [0., 0., 0., 0.]])
b =  tensor([[0., 0., 0., 0., 0.]])
c =  tensor([[0.],
        [0.],
        [0.],
        [0.],
        [0.]])
d =  tensor([[[0., 0.],
         [0., 0.],
         [0., 0.]],

        [[0., 0.],
         [0., 0.],
         [0., 0.]],

        [[0., 0.],
         [0., 0.],
         [0., 0.]]])

```