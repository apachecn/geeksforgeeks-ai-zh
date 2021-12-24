# Python–PyTorch fmod()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-fmod-method/](https://www.geeksforgeeks.org/python-pytorch-fmod-method/)

PyTorch `torch.fmod()`方法给出了除数除法的元素余项。除数可以是数字或张量。

> **语法:** `torch.fmod(input, div, out=None)`
> 
> **论据**
> 
> *   **输入:**这是输入张量。
> *   **div:** 这可能是一个数或一个张量。
> *   **出:**输出张量。
> 
> **返回:**它返回一个张量。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([5, 6, 7, 4])
print(a)

# Applying the fmod function and 
# storing the result in 'out'
out = torch.fmod(a, 3)
print(out)
```

**输出:**

```
5
 6
 7
 4
[torch.FloatTensor of size 4]
 2
 0
 1
 1
[torch.FloatTensor of size 4]

```

**例 2:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([5, 6, 7, 4])
b = torch.FloatTensor([2, 3, 4, 1])
print(a, b)

# Applying the fmod function and 
# storing the result in 'out'
out = torch.fmod(a, b)
print(out)
```

**输出:**

```
5
 6
 7
 4
[torch.FloatTensor of size 4]
 2
 3
 4
 1
[torch.FloatTensor of size 4]

 1
 0
 3
 0
[torch.FloatTensor of size 4]

```