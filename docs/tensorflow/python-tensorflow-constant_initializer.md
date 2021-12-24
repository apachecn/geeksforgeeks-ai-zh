# python–tensorlow . constant _ initialize()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-constant _ initialize/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**constant_initializer()** 是生成常数值张量的初始值设定项。

> **语法:**tensorflow . constant _ initializer(值)
> 
> **参数:**
> 
> *   **值:**是需要转换为 Tensor 的值。它可以是 Python 标量、值列表或元组，或者 N 维 numpy 数组
> 
> **返回:**它返回一个初始值设定项实例。

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
x = tf.constant_initializer(l)

# Printing the result
print('x: ', x)
```

**输出:**

```py
l:  [1, 2, 3, 4]
x:  tensorflow.python.ops.init_ops_v2.Constant object at 0x7fa7f2e1ab00

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
x = tf.constant_initializer(l )

# Printing the result
print('x: ', x)
```

**输出:**

```py
l:  (1, 2, 3, 4)
x:  tensorflow.python.ops.init_ops_v2.Constant object at 0x7fa7f2e1ab00

```