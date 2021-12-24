# python–tensorlow . constant()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-constant/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**常量()**用于从像列表一样的张量对象创建张量。

> **语法:** tensorflow.constant(值、数据类型、形状、名称)
> 
> **参数:**
> 
> *   **值:**是需要转换为 Tensor 的值。
> *   **数据类型(可选):**定义输出张量的类型。
> *   **形状(可选):**定义输出张量的维度。
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
x = tf.constant(l)

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
x = tf.constant(l, dtype = tf.float64)

# Printing the result
print('x: ', x)
```

**输出:**

```py
l:  (1, 2, 3, 4)
x:  tf.Tensor([1\. 2\. 3\. 4.], shape=(4, ), dtype=float64)

```