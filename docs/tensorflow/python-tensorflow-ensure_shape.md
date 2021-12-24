# Python–tensorflow . survey _ shape()

> 原文:[https://www . geeksforgeeks . org/python-tensorflow-success _ shape/](https://www.geeksforgeeks.org/python-tensorflow-ensure_shape/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**保证 _shape()** 用于更新和检查 Tensor 的形状。

> **语法:**tensorflow . success _ shape(x，shape，name)
> 
> **参数:**
> 
> *   **x:** 是输入 Tensor。
> *   **形状:**代表输入张量形状的是张量形状。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> 如果形状不兼容，它将返回一个与 x 相同的张量或引发**TF . errors . invalidargumenterror**。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
x = tf.constant([[2, 3, 6], [4, 8, 15]])

# Printing the input
print('x:', x)

# Calculating result
res = tf.ensure_shape(x, (2, 3))

# Printing the result
print('res: ', res)
```

**输出:**

```py
x: tf.Tensor(
[[ 2  3  6]
 [ 4  8 15]], shape=(2, 3), dtype=int32)
res:  tf.Tensor(
[[ 2  3  6]
 [ 4  8 15]], shape=(2, 3), dtype=int32)

```

**示例 2:** 在此示例中，形状与 x 的形状不兼容，因此会出现错误。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
x = tf.constant([[2, 3, 6], [4, 8, 15]])

# Printing the input
print('x:', x)

# Calculating result
res = tf.ensure_shape(x, (2, 4))

# Printing the result
print('res: ', res)
```

**输出:**

```py
x: tf.Tensor(
[[ 2  3  6]
 [ 4  8 15]], shape=(2, 3), dtype=int32)

---------------------------------------------------------------------------

InvalidArgumentError                      Traceback (most recent call last)

<ipython-input-1-ab1be364fadb> in <module>()
      9 
     10 # Calculating result
---> 11 res = tf.ensure_shape(x, (2, 4))
     12 
     13 # Printing the result

3 frames

/usr/local/lib/python3.6/dist-packages/six.py in raise_from(value, from_value)

InvalidArgumentError: Shape of tensor dummy_input [2, 3] is not compatible with expected shape [2, 4]. [Op:EnsureShape]

```