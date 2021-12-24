# python–tensorlow . math . true div()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-true div/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**truediv()** 用于计算元素方向 x/y。

> **语法:**tensorlow . math . true div(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是数值型张量。
> *   **y:** 是数值型张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ -5, -7, 2, 5, 7], dtype = tf.float64)
b = tf.constant([ 1, 3, 9, 4, 7], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.truediv(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([-5\. -7\.  2\.  5\.  7.], shape=(5, ), dtype=float64)
b:  tf.Tensor([1\. 3\. 9\. 4\. 7.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([-5\.         -2.33333333  0.22222222  1.25        1\.        ], shape=(5, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import numpy as np

# Initializing the input tensor
a = tf.constant([ -5, -7, 2, 5, 7], dtype = tf.float64)
b = tf.constant([ 0, 3, 9, 4, np.inf], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.truediv(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([-5\. -7\.  2\.  5\.  7.], shape=(5, ), dtype=float64)
b:  tf.Tensor([ 0\.  3\.  9\.  4\. inf], shape=(5, ), dtype=float64)
Result:  tf.Tensor([       -inf -2.33333333  0.22222222  1.25        0\.        ], shape=(5, ), dtype=float64)

```