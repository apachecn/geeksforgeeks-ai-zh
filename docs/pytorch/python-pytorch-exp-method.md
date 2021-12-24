# Python–PyTorch exp()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-exp-method/](https://www.geeksforgeeks.org/python-pytorch-exp-method/)

PyTorch `torch.exp()`方法在得到输入张量元素的指数后返回一个新的张量。
![exp method](img/e8682b9011ae1bdee5775d20d75ee506.png)

> **语法:** `torch.exp(input, out=None)`
> 
> **论据**
> 
> *   **输入:**这是输入张量。
> *   **出:**输出张量。
> 
> **返回:**它返回一个张量。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(6)
print(a)

# Applying the exp function and 
# storing the result in 'out'
out = torch.exp(a)
print(out)
```

**输出:**

```
1.0532
-1.9300
 0.6392
-0.7519
 0.9133
 0.3998
[torch.FloatTensor of size 6]
 2.8667
 0.1451
 1.8949
 0.4715
 2.4925
 1.4915
[torch.FloatTensor of size 6]

```

**例 2:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1, 4, 6, 3])
print(a)

# Applying the exp function and 
# storing the result in 'out'
out = torch.exp(a)
print(out)
```

**输出:**

```
 1
 4
 6
 3
[torch.FloatTensor of size 4]
   2.7183
  54.5981
 403.4288
  20.0855
[torch.FloatTensor of size 4]

```