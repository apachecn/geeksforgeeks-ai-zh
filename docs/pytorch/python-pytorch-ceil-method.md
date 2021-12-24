# Python–PyTorch ceil()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-ceil-method/](https://www.geeksforgeeks.org/python-pytorch-ceil-method/)

PyTorch `torch.ceil()`方法返回一个新的张量，该张量具有输入元素的上限值，是大于或等于每个元素的最小整数。

> **语法:** `torch.ceil(inp, out=None)`
> 
> **论据**
> 
> *   **inp:** 这是输入张量。
> *   **出:**输出张量。
> 
> **返回:**它返回一个张量。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1.3, -5.6, 7.9, 10.1])
print(a)

# Applying the ceil function and 
# storing the result in 'out'
out = torch.ceil(a)
print(out)
```

**输出:**

```
  1.3000
 -5.6000
  7.9000
 10.1000
[torch.FloatTensor of size 4]
  2
 -5
  8
 11
[torch.FloatTensor of size 4]

```

**例 2:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1.00001, -5.699, 7.100001, 10.0001])
print(a)

# Applying the ceil function and 
# storing the result in 'out'
out = torch.ceil(a)
print(out) 
```

**输出:**

```
 1.0000
 -5.6990
  7.1000
 10.0001
[torch.FloatTensor of size 4]
  2
 -5
  8
 11
[torch.FloatTensor of size 4]

```