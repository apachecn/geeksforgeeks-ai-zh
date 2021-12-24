# Python–PyTorch 地板()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-floor-method/](https://www.geeksforgeeks.org/python-pytorch-floor-method/)

PyTorch `torch.floor()`方法返回一个新的张量，它是输入元素的基底，小于或等于每个元素的最大整数。
![floor method](img/ec60753e8c8ffe5ad4ebc49859a7f8da.png)

> **语法:** `torch.floor(input, out=None)`
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
a = torch.FloatTensor([1.5, 4.2, 6.7, 3.9])
print(a)

# Applying the floor function and 
# storing the result in 'out'
out = torch.floor(a)
print(out)
```

**输出:**

```py
 1.5000
 4.2000
 6.7000
 3.9000
[torch.FloatTensor of size 4]

 1
 4
 6
 3
[torch.FloatTensor of size 4]

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1.59, 4.5999, 6.78, 3.99999])
print(a)

# Applying the floor function and 
# storing the result in 'out'
out = torch.floor(a)
print(out)
```

**输出:**

```py
1.5900
 4.5999
 6.7800
 4.0000
[torch.FloatTensor of size 4]

 1
 4
 6
 3
[torch.FloatTensor of size 4]

```