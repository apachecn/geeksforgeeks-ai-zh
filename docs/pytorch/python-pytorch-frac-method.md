# Python–PyTorch frac()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-frac-method/](https://www.geeksforgeeks.org/python-pytorch-frac-method/)

PyTorch `torch.frac()`方法计算输入中每个元素的小数部分。

> **语法:** `torch.frac(input, out=None)`
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
a = torch.FloatTensor([-5.4, 6.6, -7.1099, 4.4567])
print(a)

# Applying the frac function and 
# storing the result in 'out'
out = torch.frac(a)
print(out)
```

**输出:**

```py
-5.4000
 6.6000
-7.1099
 4.4567
[torch.FloatTensor of size 4]

-0.4000
 0.6000
-0.1099
 0.4567
[torch.FloatTensor of size 4]

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(6)
print(a)

# Applying the frac function and 
# storing the result in 'out'
out = torch.frac(a)
print(out)
```

**输出:**

```py
-0.5260
-1.8843
 0.8062
 1.2264
-0.1505
-0.3217
[torch.FloatTensor of size 6]

-0.5260
-0.8843
 0.8062
 0.2264
-0.1505
-0.3217
[torch.FloatTensor of size 6]

```