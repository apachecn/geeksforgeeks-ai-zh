# 张量流–is _ tensor()方法

> 原文:[https://www.geeksforgeeks.org/tensorflow-is_tensor-method/](https://www.geeksforgeeks.org/tensorflow-is_tensor-method/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。
张量被许多张量流运算使用。有时，在使用前检查给定变量是否是张量是很重要的。 **is_tensor()** 方法可以用来检查这一点。

> *   **is _ Tensor:** This method takes variables as input, and returns True if the variables are tensor or tensor-like objects, otherwise it returns false.

**示例 1:** 如果给定变量是 Tensor，则该示例将打印 True，否则将打印 False。

```py
# importing the library
import tensorflow as tf

# Initializing python string
s = "GeeksForGeeks"

# Checking if s is a Tensor
res = tf.is_tensor(s)

# Printing the result
print('Result: ', res)

# Initializing the input tensor
a = tf.constant([ [-5, -7],[ 2, 0]], dtype=tf.float64)

# Checking if a is a Tensor
res = tf.is_tensor(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py

Result:  False
Result:  True

```

**示例 2:** 本示例检查变量是否为张量，如果不是，则将变量转换为张量。

```py
# importing the library
import tensorflow as tf
import numpy as np

# Initializing numpy array
arr = np.array([1, 2, 3])

# Checking if s is a Tensor
if not tf.is_tensor(arr):
  # Converting to tensor
  arr = tf.convert_to_tensor(arr)

# Printing the dtype of resulting tensor
print("Dtype: ",arr.dtype)

# Printing the resulting tensor
print("tensor: ",arr)
```

**输出:**

```py
Dtype:  <dtype: 'int64'>
tensor:  tf.Tensor([1 2 3], shape=(3,), dtype=int64)

```