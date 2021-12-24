# Python | PyTorch acos()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-acos-method/](https://www.geeksforgeeks.org/python-pytorch-acos-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。
函数 torch.acos()为 PyTorch 中的*反余弦*函数提供支持。它期望输入在[-1，1]范围内，并以弧度形式给出输出。如果输入不在[-1，1]范围内，则返回 *nan* 。输入类型是张量，如果输入包含一个以上的元素，则计算元素方向的反余弦。

> **语法** : torch.acos(x，out=None)
> **参数** :
> **x** :输入张量
> **名称**(可选):输出张量
> **返回类型**:与 x 类型相同的张量。

**代码#1:**

## 蟒蛇 3

```py
# Importing the PyTorch library
import torch

# A constant tensor of size 6
a = torch.FloatTensor([1.0, -0.5, 3.4, 0.2, 0.0, -2])
print(a)

# Applying the inverse cos function and
# storing the result in 'b'
b = torch.acos(a)
print(b)
```

**输出:**

```py
tensor([ 1.0000, -0.5000,  3.4000,  0.2000,  0.0000, -2.0000])
tensor([0.0000, 2.0944,    nan, 1.3694, 1.5708,    nan])
```

**代码#2:** 可视化

## 蟒蛇 3

```py
# Importing the PyTorch library
import torch

# Importing the NumPy library
import numpy as np

# Importing the matplotlib.pyplot function
import matplotlib.pyplot as plt

# A vector of size 15 with values from -1 to 1
a = np.linspace(-1, 1, 15)

# Applying the inverse cosine function and
# storing the result in 'b'
b = torch.acos(torch.FloatTensor(a))

print(b)

# Plotting
plt.plot(a, b.numpy(), color = 'red', marker = "o")
plt.title("torch.acos")
plt.xlabel("X")
plt.ylabel("Y")

plt.show()
```

**输出:**

```py
tensor([3.1416, 2.6005, 2.3664, 2.1790, 2.0137, 1.8605, 1.7141, 1.5708, 1.4274,
        1.2810, 1.1279, 0.9626, 0.7752, 0.5411, 0.0000])
```

![](img/ae279f8301f6c5341632d496eac6638e.png)