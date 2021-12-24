# Python–PyTorch log()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-log-method/](https://www.geeksforgeeks.org/python-pytorch-log-method/)

PyTorch `torch.log()`方法给出了一个新的张量，它具有输入张量元素的自然对数。

> **语法:** `torch.log(input, out=None)`
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
a = torch.FloatTensor([5, 6, 7, 4])
print(a)

# Applying the log function and 
# storing the result in 'out'
out = torch.log(a)
print(out)
```

**输出:**

```py
5
 6
 7
 4
[torch.FloatTensor of size 4]

 1.6094
 1.7918
 1.9459
 1.3863
[torch.FloatTensor of size 4]

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1.45, 2.3, 10])
print(a)

# Applying the log function and
# storing the result in 'out'
out = torch.log(a)
print(out)
```

**输出:**

```py
 1.4500
  2.3000
 10.0000
[torch.FloatTensor of size 3]

 0.3716
 0.8329
 2.3026
[torch.FloatTensor of size 3]

```