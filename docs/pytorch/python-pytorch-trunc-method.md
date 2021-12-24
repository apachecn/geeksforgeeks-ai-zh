# Python–PyTorch trunc()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-trunc-method/](https://www.geeksforgeeks.org/python-pytorch-trunc-method/)

PyTorch `torch.trunc()`方法在去掉数字的小数部分后，返回一个带有输入/的元素的截断整数值的新张量。

> **语法:** `torch.trunc(input, out=None)`
> 
> **论据**
> 
> *   **输入:**这是输入张量。
> *   **出:**输出张量。
> 
> **返回:**它返回一个张量。

Let’s see this concept with the help of few examples:**Example 1:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(6)
print(a)

# Applying the trunc function and 
# storing the result in 'out'
out = torch.trunc(a)
print(out)
```

**输出:**

```py
 1.1257
 0.4493
-0.7309
 1.5523
-0.2877
 0.1155
[torch.FloatTensor of size 6]
 1
 0
-0
 1
-0
 0
[torch.FloatTensor of size 6]

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1.5, 3.9, -6.9, 3.678])
print(a)

# Applying the trunc function and 
# storing the result in 'out'
out = torch.trunc(a)
print(out)
```

**输出:**

```py
 1.5000
 3.9000
-6.9000
 3.6780
[torch.FloatTensor of size 4]
 1
 3
-6
 3
[torch.FloatTensor of size 4]

```