# Python Pytorch 全()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-full-method/](https://www.geeksforgeeks.org/python-pytorch-full-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。

函数`torch.full()`返回填充了 fill_value 的大小为**大小为**的张量。

> **语法**:torch . one(大小，fill_value，out =无)
> 
> **参数** :
> **大小**:定义输出张量形状的整数序列
> **fill_value** :填充输出张量的数字。
> **输出(张量，可选)**:输出张量
> 
> **返回类型**:张量

**代码#1:**

```
# Importing the PyTorch library
import torch

# Applying the full function and
# storing the resulting tensor in 'a'
a = torch.full([3, 4], 3)
print("a = ", a)

b = torch.full([2, 5], 3.5)
print("b = ", b)
```

**输出:**

```
a =  tensor([[3., 3., 3., 3.],
        [3., 3., 3., 3.],
        [3., 3., 3., 3.]])
b =  tensor([[3.5000, 3.5000, 3.5000, 3.5000, 3.5000],
        [3.5000, 3.5000, 3.5000, 3.5000, 3.5000]])

```