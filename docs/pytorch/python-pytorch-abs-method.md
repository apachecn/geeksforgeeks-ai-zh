# Python–PyTorch ABS()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-abs-method/](https://www.geeksforgeeks.org/python-pytorch-abs-method/)

PyTorch `torch.abs()`方法计算给定输入张量的元素绝对值。

> **语法:** `torch.abs(inp, out=None) ? Tensor`
> 
> **论据**
> 
> *   **inp:** 这是输入张量。
> *   **out:** 这是可选参数，是输出张量。
> 
> **Return:** 它返回一个具有输入 inp 绝对值的张量。

Let’s see this concept with the help of few examples:**Example 1:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size 1 
a = torch.FloatTensor([-15]) 
print(a) 

# Applying the abs function and 
# storing the result in 'b' 
b = torch.abs(a) 
print(b) 
```

**输出:**

```py
-15
[torch.FloatTensor of size 1]
 15
[torch.FloatTensor of size 1]

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n 
a = torch.FloatTensor([15, -5, 3, -2]) 
print(a) 

# Applying the abs function and 
# storing the result in 'b' 
b = torch.abs(a) 
print(b) 
```

**输出:**

```py
 15
 -5
  3
 -2
[torch.FloatTensor of size 4]
 15
  5
  3
  2
[torch.FloatTensor of size 4]

```