# Python–PyTorch add()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-add-method/](https://www.geeksforgeeks.org/python-pytorch-add-method/)

PyTorch `torch.add()`方法为输入张量的每个元素添加一个常量值，并返回一个新的修改后的张量。

> **语法:** `torch.add(inp, c, out=None)`
> 
> **论据**
> 
> *   **inp:** 这是输入张量。
> *   **c:** 要加到张量每个元素上的值。
> *   **out:** 这是可选参数，是输出张量。
> 
> **返回:**它返回一个张量。

Let’s see this concept with the help of few examples:**Example 1:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size 6
a = torch.randn(6) 
print(a) 

# Applying the add function and 
# storing the result in 'b' 
b = torch.add(a, 5) 
print(b)
```

**输出:**

```py
0.2403
 1.3826
-0.1763
-1.5177
-0.0555
 1.4558
[torch.FloatTensor of size 6]
 5.2403
 6.3826
 4.8237
 3.4823
 4.9445
 6.4558
[torch.FloatTensor of size 6]

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size 6
a = torch.FloatTensor([1, 3, 8, 4, 10]) 
print(a) 

# Applying the add function and 
# storing the result in 'b' 
b = torch.add(a, 5) 
print(b) 
```

**输出:**

```py
 1
  3
  8
  4
 10
[torch.FloatTensor of size 5]
  6
  8
 13
  9
 15
[torch.FloatTensor of size 5]

```