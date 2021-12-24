# 如何将 Pytorch 张量转换成 Numpy 数组？

> 原文:[https://www . geesforgeks . org/how-convert-py torch-tensor-to-numpy-array/](https://www.geeksforgeeks.org/how-to-convert-pytorch-tensor-to-numpy-array/)

在本文中，我们将把 Pytorch 张量转换成 NumPy 数组。

**方法 1:使用 numpy()。**

> **语法:** tensor_name.numpy()

**示例 1:** 将一维张量转换为 NumPy 数组

## 蟒蛇 3

```py
# importing torch module
import torch

# import numpy module
import numpy

# create one dimensional tensor with
# float type elements
b = torch.tensor([10.12, 20.56, 30.00, 40.3, 50.4])

print(b)

# convert this into numpy array using
# numpy() method
b = b.numpy()

# display
b
```

**输出:**

```py
tensor([10.1200, 20.5600, 30.0000, 40.3000, 50.4000])
array([10.12, 20.56, 30\.  , 40.3 , 50.4 ], dtype=float32)
```

**示例 2:** 将二维张量转换为 NumPy 数组

## 蟒蛇 3

```py
# importing torch module
import torch

# import numpy module
import numpy

# create two dimensional tensor with
# integer type elements
b = torch.tensor([[1, 2, 3, 4, 5], [3, 4, 5, 6, 7], 
                  [4, 5, 6, 7, 8]])

print(b)

# convert this into numpy array using
# numpy() method
b = b.numpy()

# display
b
```

**输出:**

```py
tensor([[1, 2, 3, 4, 5],
       [3, 4, 5, 6, 7],
       [4, 5, 6, 7, 8]])
array([[1, 2, 3, 4, 5],
      [3, 4, 5, 6, 7],
      [4, 5, 6, 7, 8]])
```

**方法二:使用 numpy.array()方法。**

这也用于将张量转换为 NumPy 数组。

> **语法:** numpy.array(tensor_name)

**示例:**将二维张量转换为 NumPy 数组

## 蟒蛇 3

```py
# importing torch module
import torch

# import numpy module
import numpy

# create two dimensional tensor with 
# integer type elements
b = torch.tensor([[1, 2, 3, 4, 5], [3, 4, 5, 6, 7], 
                  [4, 5, 6, 7, 8]])

print(b)

# convert this into numpy array using 
# numpy.array() method
b = numpy.array(b)

# display
b
```

**输出:**

```py
tensor([[1, 2, 3, 4, 5],
       [3, 4, 5, 6, 7],
       [4, 5, 6, 7, 8]])
array([[1, 2, 3, 4, 5],
      [3, 4, 5, 6, 7],
      [4, 5, 6, 7, 8]])
```