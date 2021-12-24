# python–tensorlow . guarantee _ const()

> 原文:[https://www . geesforgeks . org/python-tensorflow-guarance _ const/](https://www.geeksforgeeks.org/python-tensorflow-guarantee_const/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**保证 _const()** 用于保证 TensorFlow 运行时输入张量恒定。

> **语法:**tensorflow . guard _ const(输入，名称)
> 
> **参数:**
> 
> *   **输入:**是张量。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**返回与输入张量相同的张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the Tensor
x = tf.guarantee_const(5)

# Printing the result
print("x: ", x)
```

**输出:**

```
x:  tf.Tensor(5, shape=(), dtype=int32)
```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the Tensor
x = tf.Variable(2.0, name ="x")
z = tf.Variable(4.0, name ="z")

# Using guarantee_const
y = tf.guarantee_const([x, z])

# Printing the result
print("y: ", y)
```

**输出:**

```
y:  tf.Tensor([2\. 4.], shape=(2, ), dtype=float32)
```