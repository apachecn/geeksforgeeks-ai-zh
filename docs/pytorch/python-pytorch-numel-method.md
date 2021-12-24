# Python–PyTorch numel()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-numel-method/](https://www.geeksforgeeks.org/python-pytorch-numel-method/)

PyTorch `torch.numel()`方法返回输入张量中元素的总数。

> **语法:** `torch.numel(input)`
> 
> **论据**
> 
> *   **输入:**这是输入张量。
> 
> **Return:** 返回输入张量的长度。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(4, 6)
print(a)

# Applying the numel function and 
# storing the result in 'out'
out = torch.numel(a)
print(out)
```

**输出:**

```
-0.8263  0.9807 -1.4688  0.2117 -0.8356 -0.0228
-0.8815  1.3652 -0.1892 -1.1241  0.2755  1.3006
 0.0559  0.2389  0.7944  2.6587 -2.0908  1.2973
-0.2056  0.4110  0.2163  0.3091  0.5559 -0.2468
[torch.FloatTensor of size 4x6]
24

```

**例 2:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1, 4, 6, 8])
print(a)

# Applying the numel function and 
# storing the result in 'out'
out = torch.numel(a)
print(out)
```

**输出:**

```
 1
 4
 6
 8
[torch.FloatTensor of size 4]
4

```