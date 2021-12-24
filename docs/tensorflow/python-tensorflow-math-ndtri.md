# python–tensorlow . math . ndtri()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-ndtri/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。 **ndtri()** 用于寻找标准正态的分位数。

> **语法:** tf.math.ndtri(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。此张量允许的数据类型是浮点型或双精度型..
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 返回 x 的逆误差函数

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([.2, .5, .7, 1], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.ndtri(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([0.2 0.5 0.7 1\. ], shape=(4, ), dtype=float64)
Result:  tf.Tensor([-0.84162123  0\.          0.52440051         inf], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([-.1, -.2, -.5, .5, .2, .1], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.ndtri(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([-0.1 -0.2 -0.5  0.5  0.2  0.1], shape=(6, ), dtype=float64)
Result:  tf.Tensor([       -inf        -inf        -inf  0\.         -0.84162123 -1.28155157], shape=(6, ), dtype=float64)
```