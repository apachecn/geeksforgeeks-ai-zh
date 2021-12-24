# Python | tensorflow . math . angle()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-angle-method/](https://www.geeksforgeeks.org/python-tensorflow-math-angle-method/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。

angle()是张量流数学模块中的方法。这种方法被用来寻找张量的元素态参数。默认情况下，所有元素都被视为复数(a+bi)。对于实数，复数部分(b)被认为是零。atan2(b，a)是由这个函数计算的参数。

```py
Syntax:
tensorflow.math.angle(
    input, name
)

Argument:
1\. input: It is a tensor. Allowed dtype for this tensor are  float, double, complex64, complex128.
2\. name: It is an optional argument that defines the name for the operation.

Return:
It returns a tensor of type float32 or float64.
```

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the constant tensor
a = tf.constant([-1.5 + 7.8j, 3 + 5.75j], dtype=tf.complex64)

# calculating the arguments
b = tf.math.angle(a)

# printing the argument tensor
print('Tensor: ',b)
```

**输出:**

```py
Tensor:  tf.Tensor([1.7607845 1.0899091], shape=(2,), dtype=float32)
```

**例 2:**

在实数的情况下，计算参数总是零。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the constant tensor
a = tf.constant([-1.5, 3 ], dtype=tf.float64)

# calculating the arguments
b = tf.math.angle(a)

# printing the argument tensor
print('Tensor: ',b)
```

**输出:**

```py
Tensor:  tf.Tensor([0\. 0.], shape=(2,), dtype=float64)
```