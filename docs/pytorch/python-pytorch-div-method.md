# Python–PyTorch div()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-div-method/](https://www.geeksforgeeks.org/python-pytorch-div-method/)

PyTorch `torch.div()`方法用一个常数划分输入的每个元素，并返回一个新的修正张量。
![Clamp method](img/ec65d170fe2613ccc4bcc76cca13d131.png)

> **语法:** `torch.div(inp, other, out=None)`
> 
> **论据**
> 
> *   **inp:** 这是输入张量。
> *   **其他:**这是要分配给输入 inp 的每个元素的数字。
> *   **出:**输出张量。
> 
> **返回:**它返回一个张量。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1, 4, 6, 8, 10, 14])
print(a)

# Applying the div function and 
# storing the result in 'out'
out = torch.div(a, 0.5)
print(out)
```

**输出:**

```
1
  4
  6
  8
 10
 14
[torch.FloatTensor of size 6]
  2
  8
 12
 16
 20
 28
[torch.FloatTensor of size 6]

```

**例 2:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(6)
print(a)

# Applying the div function and 
# storing the result in 'out'
out = torch.div(a, 0.3)
print(out)
```

**输出:**

```
 -0.8453
-0.1101
 0.9431
-0.3041
 1.4305
-0.0390
[torch.FloatTensor of size 6]
-2.8176
-0.3669
 3.1436
-1.0137
 4.7683
-0.1300
[torch.FloatTensor of size 6]

```