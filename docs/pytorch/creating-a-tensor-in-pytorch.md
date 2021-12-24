# 在 Pytorch 中创建张量

> 原文:[https://www.geeksforgeeks.org/creating-a-tensor-in-pytorch/](https://www.geeksforgeeks.org/creating-a-tensor-in-pytorch/)

所有的深度学习都是对张量的计算，张量是一个矩阵的推广，可以在超过 2 个维度上索引。张量可以用 torch.tensor()函数从 Python 列表中创建。

### **张量()方法:**

要用 Pytorch 创建张量，我们可以简单地使用张量()方法:

**语法:**

```py
torch.tensor(Data)
```

**例:**

## 蟒 3

```py
import torch

V_data = [1, 2, 3, 4]
V = torch.tensor(V_data)
print(V)
```

**输出:**

```py
tensor([1, 2, 3, 4])
```

要创建矩阵，我们可以使用:

## python 3

```py
import torch

M_data = [[1., 2., 3.], [4, 5, 6]]
M = torch.tensor(M_data)
print(M)
```

**输出:**

```py
tensor([[1., 2., 3.],
        [4., 5., 6.]])
```

要创建三维张量，您可以使用以下代码模板:

## python 3

```py
import torch

T_data = [[[1., 2.], [3., 4.]],
          [[5., 6.], [7., 8.]]]
T = torch.tensor(T_data)
print(T)
```