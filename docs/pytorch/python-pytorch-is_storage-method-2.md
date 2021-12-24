# Python–PyTorch is _ storage()方法

> 原文:[https://www . geesforgeks . org/python-py torch-is _ storage-method-2/](https://www.geeksforgeeks.org/python-pytorch-is_storage-method-2/)

如果对象是 PyTorch 存储对象，PyTorch `torch.is_storage()`方法返回 True。

> **语法:** `torch.is_storage(object)`
> 
> **论据**
> 
> *   **对象:**这是待测的输入张量。
> 
> **返回:**返回真或假。

Let’s see this concept with the help of few examples:**Example 1:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.FloatStorage(6)
print(a)

# Applying the is_tensor function and 
# storing the result in 'out'
out = torch.is_storage(a)
print(out)
```

**输出:**

```py
-30587.265625
 4.555761437366413e-41
 3.906847023468105e-37
 0.0
 4.484155085839415e-44
 0.0
[torch.FloatStorage of size 6]
True

```

**例 2:**

```py
# Importing the PyTorch library 
import torch 

# A constant tensor of size n
a = torch.randn(4, 6)
print(a)

# Applying the is_tensor function and 
# storing the result in 'out'
out = torch.is_storage(a)
print(out)
```

**输出:**

```py
0.4837 -0.3108  0.5945 -0.5967  1.0831  0.0967
-0.0174  0.4937  0.9900 -0.0532 -0.4830 -0.4711
 1.3607 -1.0815  0.4421 -0.2668 -0.5778 -0.0482
-2.0869 -0.8338  1.2260 -0.8849  0.7303 -1.0050
[torch.FloatTensor of size 4x6]
False

```