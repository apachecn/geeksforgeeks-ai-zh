# Python–tensorflow . math . L2 _ normalize()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-L2 _ normalize/](https://www.geeksforgeeks.org/python-tensorflow-math-l2_normalize/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**l2_normalize()** 用于使用 l2 范数对沿轴的张量进行归一化。

> **语法:**tensorflow . math . L2 _ normalize(x，轴，ε，名称)
> 
> **参数:**
> 
> *   **x:** 是输入张量。
> *   **轴:**定义张量归一化的维度。
> *   **ε:**定义范数的下界值。默认值为 1e-12。它使用 sqrt(ε)作为除数如果范数< sqrt(除数)。
> *   **名称:**定义操作名称的可选参数。
> 
> **返回:**
> 
> 它返回一个与 x 形状相同的张量。

**例 1:**

## 蟒蛇 3

```py
# Importing the libraray
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.l2_normalize(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([0.34869484 0.39850839 0.64757613 0.54794903], shape=(4, ), dtype=float64)

```

**示例 2:** 本示例使用二维张量。

## 蟒蛇 3

```py
# Importing the libraray
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([[7, 8], [13, 11]], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.l2_normalize(x = a, axis = 1)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor(
[[ 7\.  8.]
 [13\. 11.]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[0.65850461 0.75257669]
 [0.76338629 0.64594224]], shape=(2, 2), dtype=float64)
```