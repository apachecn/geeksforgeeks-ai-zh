# Python–tensorflow . convert _ to _ tensor()

> 原文:[https://www . geesforgeks . org/python-tensorflow-convert _ to _ tensor/](https://www.geeksforgeeks.org/python-tensorflow-convert_to_tensor/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**convert_to_tensor()** 用于将给定值转换为 tensor

> **语法:**tensorflow . convert _ to _ tensor(值、数据类型、数据类型提示、名称)
> 
> **参数:**
> 
> *   **值:**是需要转换为 Tensor 的值。
> *   **数据类型(可选):**定义输出张量的类型。
> *   **dtype_hint(可选):**当 dtype 为 None 时使用。在某些情况下，当转换为张量时，调用者可能没有记住 dtype，因此 dtype_hint 可以用作软首选项。如果无法转换为 dtype_hint，则此参数无效。
> *   **名称(选项 a):** 定义操作的名称。
> 
> **返回:**返回张量。

**示例 1:** 来自 Python 列表

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
l = [1, 2, 3, 4]

# Printing the input
print('l: ', l)

# Calculating result
x = tf.convert_to_tensor(l)

# Printing the result
print('x: ', x)
```

**输出:**

```py
l:  [1, 2, 3, 4]
x:  tf.Tensor([1 2 3 4], shape=(4, ), dtype=int32)

```

**示例 2:** 来自 Python 元组

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
l = (1, 2, 3, 4)

# Printing the input
print('l: ', l)

# Calculating result
x = tf.convert_to_tensor(l, dtype = tf.float64)

# Printing the result
print('x: ', x)
```

**输出:**

```py
l:  (1, 2, 3, 4)
x:  tf.Tensor([1\. 2\. 3\. 4.], shape=(4, ), dtype=float64)

```