# Python | PyTorch tan()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-tan-method/](https://www.geeksforgeeks.org/python-pytorch-tan-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。
torch . tan()函数为 PyTorch 中的*切线*函数提供支持。它需要弧度形式的输入，输出在[-∞，∞]范围内。输入类型是张量，如果输入包含多个元素，则计算元素方向的切线。

> **语法** : torch.tan(x，out=None)
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
a = torch.FloatTensor([1.0, -0.5, 3.4, -2.1, 0.0, -6.5])
print(a)

# Applying the tan function and
# storing the result in 'b'
b = torch.tan(a)
print(b)
```

**输出:**

```py
 1.0000
-0.5000
 3.4000
-2.1000
 0.0000
-6.5000
[torch.FloatTensor of size 6]

 1.5574
-0.5463
 0.2643
 1.7098
 0.0000
-0.2203
[torch.FloatTensor of size 6]
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

# Applying the tangent function and
# storing the result in 'b'
b = torch.tan(torch.FloatTensor(a))

print(b)

# Plotting
plt.plot(a, b.numpy(), color = 'red', marker = "o")
plt.title("torch.tan")
plt.xlabel("X")
plt.ylabel("Y")

plt.show()
```

**输出:**

```py
-1.5574
-1.1549
-0.8670
-0.6430
-0.4569
-0.2938
-0.1438
 0.0000
 0.1438
 0.2938
 0.4569
 0.6430
 0.8670
 1.1549
 1.5574
[torch.FloatTensor of size 15]
```

![](img/7a721ba05c513bd45d3e813d1d37d12d.png)