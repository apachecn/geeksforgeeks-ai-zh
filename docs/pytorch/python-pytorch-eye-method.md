# 蟒蛇皮火炬眼()法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-eye-method/](https://www.geeksforgeeks.org/python-pytorch-eye-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。

函数`torch.eye()`返回一个二维张量，大小为 **n*m** ，对角线上为 1，其他地方为 0。

> **语法** : torch.eye(n，m，out =无)
> 
> **参数** :
> **n** :行数
> **m** :列数。默认–n
> **输出(张量，可选)**:输出张量
> 
> **返回类型**:二维张量

**代码#1:**

```
# Importing the PyTorch library
import torch

# Applying the eye function and
# storing the resulting tensor in 'a'
a = torch.eye(3, 4)
print("a = ", a)

b = torch.eye(3, 3)
print("b = ", b)

c = torch.eye(5, 1)
print("c = ", c)
```

**输出:**

```
a =  tensor([[1., 0., 0., 0.],
        [0., 1., 0., 0.],
        [0., 0., 1., 0.]])
b =  tensor([[1., 0., 0.],
        [0., 1., 0.],
        [0., 0., 1.]])
c =  tensor([[1.],
        [0.],
        [0.],
        [0.],
        [0.]])

```