# Python–PyTorch is _ tensor()方法

> 原文:[https://www . geesforgeks . org/python-py torch-is _ tensor-method/](https://www.geeksforgeeks.org/python-pytorch-is_tensor-method/)

如果传递的对象是 PyTorch 张量，则 PyTorch `torch.is_tensor()`方法返回 True。

> **语法:** `torch.is_tensor(object)`
> 
> **论据**
> 
> *   **对象:**这是待测的输入张量。
> 
> **返回:**返回真或假。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatTensor([1, 4, 6, 9])
print(a)

# Applying the is_tensor function and 
# storing the result in 'out'
out = torch.is_tensor(a)
print(out)
```

**输出:**

```
1
 4
 6
 9
[torch.FloatTensor of size 4]
True

```

**例 2:**

```
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(4, 6)
print(a)

# Applying the is_tensor function and 
# storing the result in 'out'
out = torch.is_tensor(a)
print(out)
```

**输出:**

```
 0.7491 -1.5987 -0.9733  0.0436 -0.3093  2.0007
 0.5679 -0.0092 -0.2573  0.9173  2.9849 -2.0159
-1.9215 -0.9131 -0.8244  0.4160 -0.3855  0.7033
 1.7367 -1.1454 -1.4369 -0.9856 -0.9076  0.6267
[torch.FloatTensor of size 4x6]
True

```