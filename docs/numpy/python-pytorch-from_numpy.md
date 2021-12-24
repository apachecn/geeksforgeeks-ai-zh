# python pytorch from _ num py()

> 原文:[https://www.geeksforgeeks.org/python-pytorch-from_numpy/](https://www.geeksforgeeks.org/python-pytorch-from_numpy/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。

函数`torch.from_numpy()`支持在 PyTorch 中将 numpy 数组转换为张量。它希望输入是 numpy 数组(numpy.ndarray)。输出类型是张量。返回的张量和数组共享相同的内存。返回的张量不可调整大小。

它目前接受数据类型为 numpy.float64、numpy.float32、numpy.float16、numpy.int64、numpy.int32、numpy.int16、numpy.int8、numpy.uint8 和 numpy.bool 的 ndarray。

> **语法** : torch.sinh(ndarray)
> 
> **参数**:
> **ndaarray**:输入 Numpy 数组(numpy . ndarray)
> 
> **返回类型**:与 x 类型相同的张量。

**代码#1:**

```py
# Importing the PyTorch library
import torch
import numpy

# A numpy array of size 6
a = numpy.array([1.0, -0.5, 3.4, -2.1, 0.0, -6.5])
print(a)

# Applying the from_numpy function and
# storing the resulting tensor in 't'
t = torch.from_numpy(a)
print(t)
```

**输出:**

```py
[ 1\.  -0.5  3.4 -2.1  0\.  -6.5]
tensor([ 1.0000, -0.5000,  3.4000, -2.1000,  0.0000, -6.5000],
       dtype=torch.float64)

```

对张量的修改将反映在数组中，反之亦然。