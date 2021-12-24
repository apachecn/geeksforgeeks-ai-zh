# Python | PyTorch cosh()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-cosh-method/](https://www.geeksforgeeks.org/python-pytorch-cosh-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。
函数 torch.cosh()为 PyTorch 中的*双曲余弦*函数提供支持。它需要弧度形式的输入。输入类型是张量，如果输入包含一个以上的元素，则按元素计算双曲余弦。

> **语法** : torch.cosh(x，out=None)
> **参数** :
> **x** :输入张量
> **名称**(可选):输出张量
> **返回类型**:与 x 类型相同的张量。

**代码#1:**

## 蟒蛇 3

```
# Importing the PyTorch library
import torch

# A constant tensor of size 6
a = torch.FloatTensor([1.0, -0.5, 3.4, -2.1, 0.0, -6.5])
print(a)

# Applying the cosh function and
# storing the result in 'b'
b = torch.cosh(a)
print(b)
```

**输出:**

```
 1.0000
-0.5000
 3.4000
-2.1000
 0.0000
-6.5000
[torch.FloatTensor of size 6]

   1.5431
   1.1276
  14.9987
   4.1443
   1.0000
 332.5716
[torch.FloatTensor of size 6]
```

**代码#2:** 可视化

## 蟒蛇 3

```
# Importing the PyTorch library
import torch

# Importing the NumPy library
import numpy as np

# Importing the matplotlib.pyplot function
import matplotlib.pyplot as plt

# A vector of size 15 with values from -1 to 1
a = np.linspace(-1, 1, 15)

# Applying the hyperbolic cosine function and
# storing the result in 'b'
b = torch.cosh(torch.FloatTensor(a))

print(b)

# Plotting
plt.plot(a, b.numpy(), color = 'red', marker = "o")
plt.title("torch.cosh")
plt.xlabel("X")
plt.ylabel("Y")

plt.show()
```

**输出:**

```
 1.5431
 1.3904
 1.2661
 1.1678
 1.0933
 1.0411
 1.0102
 1.0000
 1.0102
 1.0411
 1.0933
 1.1678
 1.2661
 1.3904
 1.5431
[torch.FloatTensor of size 15]
```

![](img/1fb52dbdbce52474d0dd238eeebb617a.png)