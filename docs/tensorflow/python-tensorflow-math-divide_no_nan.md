# Python–tensorflow . math . divide _ no _ nan()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-divide _ no _ nan/](https://www.geeksforgeeks.org/python-tensorflow-math-divide_no_nan/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**divide_no_nan()** 用于计算 x 除以 y 的元素安全除法，即如果 y 为零，则返回 0

> **语法:**tensorflow . math . divide _ no _ nan(x，y，name)
> 
> **参数:**
> 
> *   **x:** 它是张量。
> *   **y:** 它是张量。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([6, 8, 12, 15], dtype = tf.float64)
b = tf.constant([2, 3, 4, 5],  dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating safe division
res = tf.math.divide_no_nan(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 6\.  8\. 12\. 15.], shape=(4, ), dtype=float64)
b:  tf.Tensor([2\. 3\. 4\. 5.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([3\.         2.66666667 3\.         3\.        ], shape=(4, ), dtype=float64)
```

**示例 2:** 在本示例中，第二张量中的一个值取为 0。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([6, 8, 12, 15], dtype = tf.float64)
b = tf.constant([2, 3, 4, 0],  dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating safe division
res = tf.math.divide_no_nan(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 6\.  8\. 12\. 15.], shape=(4, ), dtype=float64)
b:  tf.Tensor([2\. 3\. 4\. 0.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([3\.         2.66666667 3\.                0], shape=(4, ), dtype=float64)
```