# Python–使用 Pytorch 进行矩阵乘法

> 原文:[https://www . geesforgeks . org/python-matrix-乘法-using-pytorch/](https://www.geeksforgeeks.org/python-matrix-multiplication-using-pytorch/)

矩阵乘法是科学计算的一个组成部分。当矩阵的大小很大时，它就变得复杂了。容易计算两个矩阵乘积的方法之一是使用 PyTorch 提供的方法。本文介绍如何使用 PyTorch 执行矩阵乘法。

**PyTorch 和张量:**

这是一个可以用于基于神经网络的深度学习项目的包。这是一个由脸书人工智能研究团队开发的开源图书馆。它可以用它的图形处理器的能力来代替 NumPy。这个库提供的重要类之一是**张量**。无非是 NumPy 包提供的 n 维数组。PyTorch 中有太多的方法可以应用到 Tensor 中，这使得计算变得更快更容易。张量只能包含相同数据类型的元素。

**用 PyTorch 进行矩阵乘法:**

PyTorch 中的方法期望输入是张量，PyTorch 和张量可用于矩阵乘法的方法是:

1.  torch.mm().

2.  torch.bmm()
3.  @ symbol.

## **torch.mm():**

该方法通过取一个 *m×n* 张量和一个 *n×p* 张量来计算矩阵乘法。它只能处理二维矩阵，不能处理一维矩阵。此功能不支持广播。广播只不过是当张量的形状不同时对待它们的方式。较小的张量被广播以适合更宽或更大的张量的形状用于操作。下面给出了函数的语法。

> **torch.mm(Tensor_1，Tensor_2，out=None)**

参数是两个张量，第三个是可选参数。另一个用来保存输出值的张量可以在这里给出。

**示例-1:****相同维度的矩阵**

这里两个输入具有相同的维度。因此，输出也将具有相同的维度。

## 蟒 3

```
import torch as t

mat_1 = torch.tensor([[1, 2, 3],
                      [4, 3, 8],
                      [1, 7, 2]])

mat_2 = torch.tensor([[2, 4, 1],
                      [1, 3, 6],
                      [2, 6, 5]])

torch.mm(mat_1, mat_2, out=None)
```