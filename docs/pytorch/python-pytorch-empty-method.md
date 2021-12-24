# Python Pytorch 空()法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-empty-method/](https://www.geeksforgeeks.org/python-pytorch-empty-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。

函数`torch.empty()`返回一个充满未初始化数据的张量。张量的形状由可变参数大小定义。

> **语法** : torch.empty(大小，out =无)
> 
> **参数** :
> **大小**:定义输出张量形状的整数序列
> **out(张量，可选)**:输出张量
> 
> **返回类型**:张量

**代码#1:**

```
# Importing the PyTorch library
import torch

# Applying the empty function and
# storing the resulting tensor in 'a'
a = torch.empty([3, 4])
print("a = ", a)

b = torch.empty([2, 3])
print("b = ", b)
```

**输出:**

```
a =  tensor([[2.0283e-19, 6.9772e+22, 1.8943e+23, 1.1432e-32],
        [1.3563e-19, 1.8888e+31, 8.9066e-15, 1.8888e+31],
        [6.4639e-04, 6.8608e+22, 1.7753e+28, 2.0535e-19]])
b =  tensor([[0., 0., 0.],
        [0., 0., 0.]])

```