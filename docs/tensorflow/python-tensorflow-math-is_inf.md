# python–tensorlow . math . is _ INF()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-is _ INF/](https://www.geeksforgeeks.org/python-tensorflow-math-is_inf/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**is_inf()** 返回 true 如果元素是无限的，则返回 false。

> **语法:** tensorflow.math.is_inf( x，name)
> 
> **参数:**
> 
> *   **x:** 它是张量。允许的数据类型有 bfloat16、half、float32、float64。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**返回数据类型布尔的张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf
import numpy as np

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11, np.inf], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.is_inf(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11\. inf], shape=(5, ), dtype=float64)
Result:  tf.Tensor([False False False False  True], shape=(5, ), dtype=bool)
```

**示例 2:** 本示例使用 numpy nan 并检查其无限性。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf
import numpy as np

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11, np.nan], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.is_inf(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11\. nan], shape=(5, ), dtype=float64)
Result:  tf.Tensor([False False False False False], shape=(5, ), dtype=bool)
```